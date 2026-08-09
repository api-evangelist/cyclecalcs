---
name: Check whether an eclipse is visible from a place
description: >-
  Find the next solar or lunar eclipses and get an explicit, per-location answer to
  "can I see it from here", with local contact times — instead of a global map the
  user has to interpret.
api: openapi/cyclecalcs-astronomy-openapi-original.json
mcp: https://www.cyclecalcs.com/mcp
operations: [getEclipses, getPlaces]
mcp_tools: [astro_eclipses, astro_find_place]
generated: '2026-08-09'
method: generated
---

# Eclipse visibility from a place

## Step 1 — pin the observer (`getPlaces`, optional)

`GET /v2/places?q=Reykjavik,IS&limit=1` → `latitude`, `longitude`, `timezone`.
Or pass `place=Reykjavik,IS` directly in step 2 and let the API resolve it.

## Step 2 — the eclipses (`getEclipses`)

`GET /v2/eclipses?lat=<lat>&lon=<lon>&tz=<tz>&count=5&direction=next`

Key parameters:

- `type=` filters to `solar` or `lunar`; `direction=next|previous`.
- `count=` or `start`/`end` bound the search. `visible_only=true` drops eclipses that miss
  this observer entirely.
- `include=` pulls in the extra geometry blocks.
- **Without `lat`/`lon` you get global geometry only.** Local circumstances and the
  visible-from-here answer require an observer.

The response gives, per eclipse: type, peak instant, Saros series (the *member number* is
withheld pending a licence review — do not claim one), global geometry, and — with a location
— local contact times and an explicit visibility verdict.

## Step 3 — say it plainly

Report the verdict first ("partial, 62% obscured, from 09:14 to 11:41 local"), then the
contacts. If the eclipse is not visible from there, say so and offer the next one that is
(`visible_only=true`).

Never infer visibility yourself from a global map: the API answers it directly, and a
hand-derived answer will disagree at the edges.

## Safety

For solar eclipses, pass the provider's own guidance through: never look at the partial phases
without a certified solar filter. The API returns positions; it is not observing advice.

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
