---
name: Answer "what is in the sky tonight" for a place
description: >-
  Resolve a plain-language place name to coordinates, pull the one-call whole-sky
  snapshot for that place and moment, then find tonight's genuinely dark moonless
  observing window. The three-step flow behind almost every consumer astronomy question.
api: openapi/cyclecalcs-astronomy-openapi-original.json
mcp: https://www.cyclecalcs.com/mcp
operations: [getPlaces, getToday, getDarkWindow]
mcp_tools: [astro_find_place, astro_sky_today, astro_dark_window]
generated: '2026-08-09'
method: generated
---

# Tonight's sky for a place

## Step 1 — resolve the place (`getPlaces`)

`GET /v2/places?q=Lisbon,PT&limit=1`

- `q` is `"City"` or `"City,CC"` with an ISO country code. `min_population`, `country`,
  `region` and `radius_km` narrow it.
- Take `data.results[0]` → `place_id`, `latitude`, `longitude`, `timezone`.
- If nothing matches you get `400 PLACE_NOT_FOUND`; if several do, `400 AMBIGUOUS_PLACE` —
  re-ask with a country code rather than guessing.
- **This response carries a GeoNames CC BY 4.0 obligation.** Copy `attribution` through to
  whatever you show the user.

You can skip this step entirely by passing `place=Lisbon,PT` straight to step 2 — the API
resolves it server-side and supplies the timezone. Do that when you do not need the `place_id`.

## Step 2 — the whole-sky snapshot (`getToday`)

`GET /v2/today?lat=<lat>&lon=<lon>&tz=<timezone>`

One call returns moon phase and illumination, which planets are up, the next notable events,
sun times, when true darkness begins, and a one-line plain-language `summary`. Use `include=`
(`sun`, `moon`, `planets`, `events`, `night`) to trim the payload.

Reach for this FIRST when the question is broad. Only drop to `getSun`, `getMoon`,
`getPositions` or `getPlanetBoard` when the user asks for one specific number.

## Step 3 — when is it actually dark (`getDarkWindow`)

`GET /v2/dark-window?lat=<lat>&lon=<lon>&tz=<timezone>&nights=7`

- `lat` and `lon` are **required** here (`LatitudeRequiredParam` / `LongitudeRequiredParam`);
  omitting them returns `400 INCOMPLETE_LOCATION` or `400 LOCATION_REQUIRED`.
- Astronomical night intersected with the Moon being down, ranked across up to 62 nights,
  with a trend. Tune with `sun_depression_deg`, `moon_altitude_max_deg`, `moon_illumination_max`.
- At high latitude expect `polar_day` / `polar_night` warnings and an empty window — that is a
  correct answer, not a failure.

## Reporting it back

Lead with `data.summary` from step 2, then the dark window as a local-time range. If a `place`
was resolved anywhere in the chain, print `attribution` verbatim.

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
