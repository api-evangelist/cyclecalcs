---
name: Build a sun and moon calendar for a location
description: >-
  Produce a per-day sunrise/sunset/twilight table and the matching lunar phase calendar
  for a location and date range, in a small number of ranged requests rather than one
  request per day.
api: openapi/cyclecalcs-astronomy-openapi-original.json
mcp: https://www.cyclecalcs.com/mcp
operations: [getSun, getMoon, getPhases]
mcp_tools: [astro_sun, astro_moon, astro_moon_phases]
generated: '2026-08-09'
method: generated
---

# A sun and moon calendar

## Step 1 — the solar day, as a range (`getSun`)

`GET /v2/sun?lat=51.4778&lon=-0.0015&start=2026-09-01&end=2026-09-30&step=1d&tz=Europe/London`

- `lat` and `lon` are **required**. `start`/`end`/`step` return the whole month in ONE request.
- `depressions=` adds custom twilight depressions (e.g. `17,18`) alongside the standard three.
- `day_anchor=` chooses what "a day" means: `civil` (local midnight), `solar` (mean solar
  midnight from longitude alone), or `utc`.
- Cap: 366 daily rows for one body on the free tier. A longer span returns
  `400 RANGE_TOO_LARGE` with a `cap` extension — split the request, do not retry it.
- `format=csv` returns the same answer as a spreadsheet.

## Step 2 — daily moon state (`getMoon`)

`GET /v2/moon?lat=51.4778&lon=-0.0015&start=2026-09-01&end=2026-09-30&step=1d&tz=Europe/London`

Phase name, illuminated fraction, distance, bright limb and libration per day.
`hemisphere=north|south` picks the phase emoji set; it defaults from the sign of `lat`.
`next_phases=` appends the upcoming quarters.

## Step 3 — the quarter instants (`getPhases`)

`GET /v2/phases?start=2026-09-01&end=2026-12-31`

Every new / first quarter / full / last quarter with its exact instant, Earth–Moon distance,
apparent size, traditional name, supermoon classification **under both competing rules**, and
any eclipse attached to that quarter. `phases=` filters to the quarters you want; `include=`
adds detail blocks.

Cap: 100 events per list on the free tier.

## Assembling

Join step 1 and step 2 on the local date, then mark the rows that step 3 identifies as quarter
days. Do not recompute anything locally — `meta` states the refraction model and horizon
definitions each number was produced under, and a locally recomputed value will not match.

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
