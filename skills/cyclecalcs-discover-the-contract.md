---
name: Discover the CycleCalcs contract before calling it
description: >-
  CycleCalcs publishes its routes, its conventions, its full controlled vocabulary
  and its source register as four live JSON endpoints. Read them instead of guessing
  parameter values, and instead of hard-coding anything that might move.
api: openapi/cyclecalcs-astronomy-openapi-original.json
operations: [getDiscovery, getConventions, getEnums, getAttribution]
generated: '2026-08-09'
method: generated
---

# Read the contract from the API itself

## `GET /v2` — the route table (`getDiscovery`)

Every endpoint, parameter, convention and limit as one document. Also carries
`contract_version`, `frozen_versions` (v1 is frozen, permanently), `capabilities`
(`timezone_resolution`, `place_lookup`, `api_keys`) and the global `limits`
(`max_rows_global` 10000, `max_bodies_per_request` 20, `max_compute_ms` 8000).

Check `data.contract_version` — or better, `meta.contract_version`, which is on **every** 2xx
from every endpoint — to detect additive change without polling.

## `GET /v2/conventions` — the physics (`getConventions`)

Time scales (UT1 treated as equal to UTC; TT from an Espenak–Meeus delta-T model; TAI from the
leap-second table and undefined before 1972), the six frames (`eqj`, `eqd`, `ect`, `ecl`,
`hor`, `gal`), which corrections are applied (aberration, light-travel time, nutation,
topocentric parallax — **not** proper motion, **not** polar motion), the refraction model
(Saemundsson, disable with `refraction=none`), and `range_caps_by_shape` for the caller's tier.

**Read this before comparing a CycleCalcs number to another source.** Most disagreements are a
frame or refraction difference, not an error.

## `GET /v2/enums` — the vocabulary (`getEnums`)

40 enumerated sets, each scoped to the endpoints that use it: bodies, refused body aliases and
why, moon-phase names (north and south emoji), rise/set statuses, 48 event kinds, zodiac signs,
compass points, visibility phrases, 74 warning codes, 117 error codes, formats, cache classes,
rights states, 21 tracked cycles, and the explicit `non_goals`.

Validate a parameter value against this rather than trial-and-error against `400`s.

## `GET /v2/attribution` — the source register (`getAttribution`)

Every dataset behind every endpoint with holder, version, role, licence, credit line and the
obligation it puts on a caller. Astronomy Engine is MIT and imposes nothing on output. GeoNames
is CC BY 4.0 and **does** — any response that resolved a `place` carries a required credit in
`meta.attribution.text`.

`meta.rights` on the response itself is authoritative for that response
(`unrestricted` | `attribution_required`); this endpoint describes what each endpoint *can*
draw on.

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
