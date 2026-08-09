---
name: Track planet visibility, retrogrades and apparitions
description: >-
  Answer "which planets can I see tonight", "when is Mercury retrograde", and
  "when do these two planets meet" from the planet board, the station catalogue
  and the conjunction search.
api: openapi/cyclecalcs-astronomy-openapi-original.json
mcp: https://www.cyclecalcs.com/mcp
operations: [getPlanetBoard, getPlanetEvents, getRetrogrades, getConjunctions]
mcp_tools: [astro_planet_board, astro_planet_events]
generated: '2026-08-09'
method: generated
---

# Planets: visibility, stations and meetings

## "What can I see tonight" — `getPlanetBoard`

`GET /v2/planet-board?lat=<lat>&lon=<lon>&tz=<tz>`

All eight planets in one request: sky place, brightness, apparent size, retrograde state, next
station, and whether it is worth looking tonight. `sort=` orders the board, `bodies=` narrows it
(max 20 bodies per request), `frames=minimal|standard|all` controls how much position detail
comes back, `refraction=normal|none`.

Use the published `visibility_phrases` vocabulary (`glare`, `most_of_night`, `morning_sky`,
`evening_sky`) rather than inventing wording.

## "Is Mercury retrograde" — `getRetrogrades`

`GET /v2/retrogrades?start=2026-01-01&end=2027-12-31`

Every retrograde and direct station of every planet in the window, with the loop length, its
arc, and the triple-crossing interval. This is geometry, not influence — the provider is
explicit that the API "attaches no meaning" to any of it, and so should you.

## "When is Venus the morning star" — `getPlanetEvents`

`GET /v2/planet-events?body=venus&count=10`

The apparition cycle of Mercury and Venus as events: inferior/superior conjunctions, greatest
elongations, peak brightness, transits, plus the current cycle state.

## "When do Jupiter and Saturn meet" — `getConjunctions`

`GET /v2/conjunctions?pairs=jupiter,saturn&start=2026-01-01&end=2030-12-31`

Close approaches between body pairs, ranked, with the separation and whether the pair is
observable or lost in twilight. For a single instant use `getSeparation` instead.

Event-search cap: 100 events per list on the free tier.

## Bodies

Only the 11 codes in the published `bodies` set are accepted. Minor planets (Ceres, Pallas,
Chiron, …) are refused **on purpose** — the MIT-licensed engine has no minor-planet ephemeris
and the provider lists this as a permanent non-goal. Do not substitute another source and
present it as a CycleCalcs answer.

## Rules that apply to every CycleCalcs call

- **No key, no signup.** Every request to `https://www.cyclecalcs.com/v2/...` is a plain `GET`
  served at the free Basic tier. Never put a `key=` in the URL — it is recognised, ignored, and
  earns a `parameter_ignored` warning. (The MCP server at `https://www.cyclecalcs.com/mcp` is the
  exception: `tools/call` needs `Authorization: Bearer <RapidAPI key>` or `X-Api-Key`.)
- **Every call is safe to retry.** All 29 operations are `GET`. Identical requests return identical
  bytes, so a retry costs nothing and changes nothing. Use `ETag` / `If-None-Match` to get a `304`.
- **Prefer one ranged request over N single requests.** Most operations take `start`, `end` and
  `step` (or `count`). One ranged call consumes one rate-limit unit; a loop consumes one per day.
- **Read the envelope, not just `data`.** Every 200 is the nine-key envelope
  `{endpoint, computed_at, query, data, warnings, links, meta, attribution, docs}`.
  - `query.ignored` tells you which parameters were dropped.
  - `warnings[]` is advisory and NEVER changes the HTTP status — read it before trusting a value.
  - `meta` carries the frame, epoch, time scale, refraction model and `contract_version`.
  - `attribution` must be shown verbatim whenever a `place` was resolved (GeoNames CC BY 4.0).
- **Errors are RFC 9457.** Switch on `code`, not on prose. `type` dereferences to
  `https://www.cyclecalcs.com/api/errors.html#<slug>`. Honour the integer `Retry-After` on `429`
  (`RATE_LIMITED`) and `503`. Do not retry a `400` — fix the parameter named in `parameter` and
  follow `hint`.
- **Dates run 1700–2200.** Anything outside returns `400 DATE_OUT_OF_RANGE`. Send `at=` as ISO 8601;
  omit it for "now". Send `tz=` as an IANA zone to render local times.
- **Ranges are capped.** Over the cap is refused with `400 RANGE_TOO_LARGE` carrying a `cap`
  extension — it is never silently truncated. See `rate-limits/cyclecalcs-rate-limits.yml`.
