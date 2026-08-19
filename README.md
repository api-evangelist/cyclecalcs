# CycleCalcs (cyclecalcs)

CycleCalcs publishes a read-only positional-astronomy engine as both a REST API and a hosted MCP server over the same core: sun and moon rise/set and twilight, moon phases and libration, planet positions and a visibility board, eclipses with per-observer local circumstances, seasons, apsides, lunar nodes, retrograde stations, conjunctions and angular separation, sidereal time, the equation of time, Jupiter's Galilean moons, sky quality and dark-sky windows, place lookup, and a one-call whole-sky snapshot. It returns the named answer and the numbers behind it rather than raw ephemeris, and every response states its frame, epoch, time scale and refraction model. Computed live with the MIT-licensed Astronomy Engine, arcminute class for the Sun, Moon and planets from 1700 to 2200. Twenty-nine GET endpoints, JSON/CSV/TXT, RFC 9457 problem documents, open CORS, and a free tier that needs no key, no signup and no card; paid volume tiers sell through RapidAPI. Pure astronomy — no astrology and no claims that sky events affect people or Earth.

**APIs.json:** [https://cyclecalcs.apievangelist.com/apis.yml](https://cyclecalcs.apievangelist.com/apis.yml)

## Tags

- Astronomy
- Space
- Science
- Ephemeris
- Sun
- Moon
- Planets
- Eclipses
- Time
- Calendar
- Geolocation
- MCP
- Agent-native

## Timestamps

- **Created:** 2026-08-09
- **Modified:** 2026-08-09

## APIs

### CycleCalcs MCP Server

Hosted stateless Streamable HTTP MCP server exposing 11 astronomy tools backed by the v2 REST endpoints. Requires Bearer RapidAPI key on every call; basic plan free. Works with Claude Code, custom connectors, and OpenAI Responses API mcp tool.

- **Human URL:** [https://www.cyclecalcs.com/api/mcp.html](https://www.cyclecalcs.com/api/mcp.html)
- **Base URL:** `https://www.cyclecalcs.com/mcp`

#### Tags

- Astronomy
- Space
- Science
- Ephemeris
- Sun
- Moon
- Planets
- Eclipses
- Time
- Calendar
- Geolocation
- MCP
- Agent-native

#### Properties

- [M C P Server](https://www.cyclecalcs.com/mcp)
- [M C P Server](mcp/cyclecalcs-mcp.yml)
- [Tool Crosswalk](mcp/cyclecalcs-tool-crosswalk.yml)
- [Documentation](https://www.cyclecalcs.com/api/mcp.html)
- [Postman Collection](collections/cyclecalcs-apsides-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-apsides-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cyclecalcs-attribution-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-attribution-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cyclecalcs-conjunctions-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-conjunctions-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cyclecalcs-conventions-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-conventions-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cyclecalcs-cyclecalcs-astronomy-api-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-cyclecalcs-astronomy-api-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cyclecalcs-cycles-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-cycles-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cyclecalcs-dark-window-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-dark-window-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cyclecalcs-eclipses-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-eclipses-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cyclecalcs-enums-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-enums-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cyclecalcs-equation-of-time-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-equation-of-time-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cyclecalcs-jupiter-moons-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-jupiter-moons-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cyclecalcs-libration-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-libration-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cyclecalcs-moon-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-moon-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cyclecalcs-moon-nodes-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-moon-nodes-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cyclecalcs-phases-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-phases-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cyclecalcs-places-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-places-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cyclecalcs-planet-board-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-planet-board-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cyclecalcs-planet-events-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-planet-events-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cyclecalcs-positions-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-positions-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cyclecalcs-retrogrades-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-retrogrades-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cyclecalcs-rise-set-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-rise-set-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cyclecalcs-seasons-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-seasons-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cyclecalcs-separation-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-separation-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cyclecalcs-sidereal-time-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-sidereal-time-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cyclecalcs-sky-quality-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-sky-quality-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cyclecalcs-sun-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-sun-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cyclecalcs-time-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-time-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cyclecalcs-today-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-today-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cyclecalcs-twilight-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-twilight-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### CycleCalcs Apsides API

The Apsides API from CycleCalcs — 1 operation(s) for apsides.

- **Human URL:** [https://www.cyclecalcs.com/api.html](https://www.cyclecalcs.com/api.html)
- **Base URL:** `https://www.cyclecalcs.com/v2`

#### Tags

- Apsides

#### Properties

- [OpenAPI](openapi/cyclecalcs-apsides-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cyclecalcs-apsides-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-apsides-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://www.cyclecalcs.com/api/reference.html)
- [Documentation](https://www.cyclecalcs.com/api/keys.html)
- [Documentation](https://www.cyclecalcs.com/api/errors.html)
- [Documentation](https://www.cyclecalcs.com/api/status.html)
- [Documentation](https://www.cyclecalcs.com/api/accuracy.html)
- [L L Ms Txt](https://www.cyclecalcs.com/llms.txt)
- [L L Ms Txt](https://www.cyclecalcs.com/v2/llms-full.txt)

### CycleCalcs Attribution API

The Attribution API from CycleCalcs — 1 operation(s) for attribution.

- **Human URL:** [https://www.cyclecalcs.com/api.html](https://www.cyclecalcs.com/api.html)
- **Base URL:** `https://www.cyclecalcs.com/v2`

#### Tags

- Attribution

#### Properties

- [OpenAPI](openapi/cyclecalcs-attribution-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cyclecalcs-attribution-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-attribution-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://www.cyclecalcs.com/api/reference.html)
- [Documentation](https://www.cyclecalcs.com/api/keys.html)
- [Documentation](https://www.cyclecalcs.com/api/errors.html)
- [Documentation](https://www.cyclecalcs.com/api/status.html)
- [Documentation](https://www.cyclecalcs.com/api/accuracy.html)
- [L L Ms Txt](https://www.cyclecalcs.com/llms.txt)
- [L L Ms Txt](https://www.cyclecalcs.com/v2/llms-full.txt)

### CycleCalcs Conjunctions API

The Conjunctions API from CycleCalcs — 1 operation(s) for conjunctions.

- **Human URL:** [https://www.cyclecalcs.com/api.html](https://www.cyclecalcs.com/api.html)
- **Base URL:** `https://www.cyclecalcs.com/v2`

#### Tags

- Conjunctions

#### Properties

- [OpenAPI](openapi/cyclecalcs-conjunctions-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cyclecalcs-conjunctions-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-conjunctions-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://www.cyclecalcs.com/api/reference.html)
- [Documentation](https://www.cyclecalcs.com/api/keys.html)
- [Documentation](https://www.cyclecalcs.com/api/errors.html)
- [Documentation](https://www.cyclecalcs.com/api/status.html)
- [Documentation](https://www.cyclecalcs.com/api/accuracy.html)
- [L L Ms Txt](https://www.cyclecalcs.com/llms.txt)
- [L L Ms Txt](https://www.cyclecalcs.com/v2/llms-full.txt)

### CycleCalcs Conventions API

The Conventions API from CycleCalcs — 1 operation(s) for conventions.

- **Human URL:** [https://www.cyclecalcs.com/api.html](https://www.cyclecalcs.com/api.html)
- **Base URL:** `https://www.cyclecalcs.com/v2`

#### Tags

- Conventions

#### Properties

- [OpenAPI](openapi/cyclecalcs-conventions-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cyclecalcs-conventions-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-conventions-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://www.cyclecalcs.com/api/reference.html)
- [Documentation](https://www.cyclecalcs.com/api/keys.html)
- [Documentation](https://www.cyclecalcs.com/api/errors.html)
- [Documentation](https://www.cyclecalcs.com/api/status.html)
- [Documentation](https://www.cyclecalcs.com/api/accuracy.html)
- [L L Ms Txt](https://www.cyclecalcs.com/llms.txt)
- [L L Ms Txt](https://www.cyclecalcs.com/v2/llms-full.txt)

### CycleCalcs CycleCalcs Astronomy API API

The CycleCalcs Astronomy API API from CycleCalcs — 1 operation(s) for cyclecalcs astronomy api.

- **Human URL:** [https://www.cyclecalcs.com/api.html](https://www.cyclecalcs.com/api.html)
- **Base URL:** `https://www.cyclecalcs.com/v2`

#### Tags

- CycleCalcs Astronomy API

#### Properties

- [OpenAPI](openapi/cyclecalcs-cyclecalcs-astronomy-api-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cyclecalcs-cyclecalcs-astronomy-api-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-cyclecalcs-astronomy-api-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://www.cyclecalcs.com/api/reference.html)
- [Documentation](https://www.cyclecalcs.com/api/keys.html)
- [Documentation](https://www.cyclecalcs.com/api/errors.html)
- [Documentation](https://www.cyclecalcs.com/api/status.html)
- [Documentation](https://www.cyclecalcs.com/api/accuracy.html)
- [L L Ms Txt](https://www.cyclecalcs.com/llms.txt)
- [L L Ms Txt](https://www.cyclecalcs.com/v2/llms-full.txt)

### CycleCalcs Cycles API

The Cycles API from CycleCalcs — 1 operation(s) for cycles.

- **Human URL:** [https://www.cyclecalcs.com/api.html](https://www.cyclecalcs.com/api.html)
- **Base URL:** `https://www.cyclecalcs.com/v2`

#### Tags

- Cycles

#### Properties

- [OpenAPI](openapi/cyclecalcs-cycles-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cyclecalcs-cycles-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-cycles-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://www.cyclecalcs.com/api/reference.html)
- [Documentation](https://www.cyclecalcs.com/api/keys.html)
- [Documentation](https://www.cyclecalcs.com/api/errors.html)
- [Documentation](https://www.cyclecalcs.com/api/status.html)
- [Documentation](https://www.cyclecalcs.com/api/accuracy.html)
- [L L Ms Txt](https://www.cyclecalcs.com/llms.txt)
- [L L Ms Txt](https://www.cyclecalcs.com/v2/llms-full.txt)

### CycleCalcs Dark Window API

The Dark Window API from CycleCalcs — 1 operation(s) for dark window.

- **Human URL:** [https://www.cyclecalcs.com/api.html](https://www.cyclecalcs.com/api.html)
- **Base URL:** `https://www.cyclecalcs.com/v2`

#### Tags

- Dark Window

#### Properties

- [OpenAPI](openapi/cyclecalcs-dark-window-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cyclecalcs-dark-window-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-dark-window-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://www.cyclecalcs.com/api/reference.html)
- [Documentation](https://www.cyclecalcs.com/api/keys.html)
- [Documentation](https://www.cyclecalcs.com/api/errors.html)
- [Documentation](https://www.cyclecalcs.com/api/status.html)
- [Documentation](https://www.cyclecalcs.com/api/accuracy.html)
- [L L Ms Txt](https://www.cyclecalcs.com/llms.txt)
- [L L Ms Txt](https://www.cyclecalcs.com/v2/llms-full.txt)

### CycleCalcs Eclipses API

The Eclipses API from CycleCalcs — 1 operation(s) for eclipses.

- **Human URL:** [https://www.cyclecalcs.com/api.html](https://www.cyclecalcs.com/api.html)
- **Base URL:** `https://www.cyclecalcs.com/v2`

#### Tags

- Eclipses

#### Properties

- [OpenAPI](openapi/cyclecalcs-eclipses-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cyclecalcs-eclipses-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-eclipses-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://www.cyclecalcs.com/api/reference.html)
- [Documentation](https://www.cyclecalcs.com/api/keys.html)
- [Documentation](https://www.cyclecalcs.com/api/errors.html)
- [Documentation](https://www.cyclecalcs.com/api/status.html)
- [Documentation](https://www.cyclecalcs.com/api/accuracy.html)
- [L L Ms Txt](https://www.cyclecalcs.com/llms.txt)
- [L L Ms Txt](https://www.cyclecalcs.com/v2/llms-full.txt)

### CycleCalcs Enums API

The Enums API from CycleCalcs — 1 operation(s) for enums.

- **Human URL:** [https://www.cyclecalcs.com/api.html](https://www.cyclecalcs.com/api.html)
- **Base URL:** `https://www.cyclecalcs.com/v2`

#### Tags

- Enums

#### Properties

- [OpenAPI](openapi/cyclecalcs-enums-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cyclecalcs-enums-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-enums-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://www.cyclecalcs.com/api/reference.html)
- [Documentation](https://www.cyclecalcs.com/api/keys.html)
- [Documentation](https://www.cyclecalcs.com/api/errors.html)
- [Documentation](https://www.cyclecalcs.com/api/status.html)
- [Documentation](https://www.cyclecalcs.com/api/accuracy.html)
- [L L Ms Txt](https://www.cyclecalcs.com/llms.txt)
- [L L Ms Txt](https://www.cyclecalcs.com/v2/llms-full.txt)

### CycleCalcs Equation Of Time API

The Equation Of Time API from CycleCalcs — 1 operation(s) for equation of time.

- **Human URL:** [https://www.cyclecalcs.com/api.html](https://www.cyclecalcs.com/api.html)
- **Base URL:** `https://www.cyclecalcs.com/v2`

#### Tags

- Equation Of Time

#### Properties

- [OpenAPI](openapi/cyclecalcs-equation-of-time-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cyclecalcs-equation-of-time-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-equation-of-time-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://www.cyclecalcs.com/api/reference.html)
- [Documentation](https://www.cyclecalcs.com/api/keys.html)
- [Documentation](https://www.cyclecalcs.com/api/errors.html)
- [Documentation](https://www.cyclecalcs.com/api/status.html)
- [Documentation](https://www.cyclecalcs.com/api/accuracy.html)
- [L L Ms Txt](https://www.cyclecalcs.com/llms.txt)
- [L L Ms Txt](https://www.cyclecalcs.com/v2/llms-full.txt)

### CycleCalcs Jupiter Moons API

The Jupiter Moons API from CycleCalcs — 1 operation(s) for jupiter moons.

- **Human URL:** [https://www.cyclecalcs.com/api.html](https://www.cyclecalcs.com/api.html)
- **Base URL:** `https://www.cyclecalcs.com/v2`

#### Tags

- Jupiter Moons

#### Properties

- [OpenAPI](openapi/cyclecalcs-jupiter-moons-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cyclecalcs-jupiter-moons-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-jupiter-moons-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://www.cyclecalcs.com/api/reference.html)
- [Documentation](https://www.cyclecalcs.com/api/keys.html)
- [Documentation](https://www.cyclecalcs.com/api/errors.html)
- [Documentation](https://www.cyclecalcs.com/api/status.html)
- [Documentation](https://www.cyclecalcs.com/api/accuracy.html)
- [L L Ms Txt](https://www.cyclecalcs.com/llms.txt)
- [L L Ms Txt](https://www.cyclecalcs.com/v2/llms-full.txt)

### CycleCalcs Libration API

The Libration API from CycleCalcs — 1 operation(s) for libration.

- **Human URL:** [https://www.cyclecalcs.com/api.html](https://www.cyclecalcs.com/api.html)
- **Base URL:** `https://www.cyclecalcs.com/v2`

#### Tags

- Libration

#### Properties

- [OpenAPI](openapi/cyclecalcs-libration-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cyclecalcs-libration-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-libration-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://www.cyclecalcs.com/api/reference.html)
- [Documentation](https://www.cyclecalcs.com/api/keys.html)
- [Documentation](https://www.cyclecalcs.com/api/errors.html)
- [Documentation](https://www.cyclecalcs.com/api/status.html)
- [Documentation](https://www.cyclecalcs.com/api/accuracy.html)
- [L L Ms Txt](https://www.cyclecalcs.com/llms.txt)
- [L L Ms Txt](https://www.cyclecalcs.com/v2/llms-full.txt)

### CycleCalcs Moon API

The Moon API from CycleCalcs — 1 operation(s) for moon.

- **Human URL:** [https://www.cyclecalcs.com/api.html](https://www.cyclecalcs.com/api.html)
- **Base URL:** `https://www.cyclecalcs.com/v2`

#### Tags

- Moon

#### Properties

- [OpenAPI](openapi/cyclecalcs-moon-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cyclecalcs-moon-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-moon-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://www.cyclecalcs.com/api/reference.html)
- [Documentation](https://www.cyclecalcs.com/api/keys.html)
- [Documentation](https://www.cyclecalcs.com/api/errors.html)
- [Documentation](https://www.cyclecalcs.com/api/status.html)
- [Documentation](https://www.cyclecalcs.com/api/accuracy.html)
- [L L Ms Txt](https://www.cyclecalcs.com/llms.txt)
- [L L Ms Txt](https://www.cyclecalcs.com/v2/llms-full.txt)

### CycleCalcs Moon Nodes API

The Moon Nodes API from CycleCalcs — 1 operation(s) for moon nodes.

- **Human URL:** [https://www.cyclecalcs.com/api.html](https://www.cyclecalcs.com/api.html)
- **Base URL:** `https://www.cyclecalcs.com/v2`

#### Tags

- Moon Nodes

#### Properties

- [OpenAPI](openapi/cyclecalcs-moon-nodes-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cyclecalcs-moon-nodes-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-moon-nodes-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://www.cyclecalcs.com/api/reference.html)
- [Documentation](https://www.cyclecalcs.com/api/keys.html)
- [Documentation](https://www.cyclecalcs.com/api/errors.html)
- [Documentation](https://www.cyclecalcs.com/api/status.html)
- [Documentation](https://www.cyclecalcs.com/api/accuracy.html)
- [L L Ms Txt](https://www.cyclecalcs.com/llms.txt)
- [L L Ms Txt](https://www.cyclecalcs.com/v2/llms-full.txt)

### CycleCalcs Phases API

The Phases API from CycleCalcs — 1 operation(s) for phases.

- **Human URL:** [https://www.cyclecalcs.com/api.html](https://www.cyclecalcs.com/api.html)
- **Base URL:** `https://www.cyclecalcs.com/v2`

#### Tags

- Phases

#### Properties

- [OpenAPI](openapi/cyclecalcs-phases-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cyclecalcs-phases-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-phases-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://www.cyclecalcs.com/api/reference.html)
- [Documentation](https://www.cyclecalcs.com/api/keys.html)
- [Documentation](https://www.cyclecalcs.com/api/errors.html)
- [Documentation](https://www.cyclecalcs.com/api/status.html)
- [Documentation](https://www.cyclecalcs.com/api/accuracy.html)
- [L L Ms Txt](https://www.cyclecalcs.com/llms.txt)
- [L L Ms Txt](https://www.cyclecalcs.com/v2/llms-full.txt)

### CycleCalcs Places API

The Places API from CycleCalcs — 1 operation(s) for places.

- **Human URL:** [https://www.cyclecalcs.com/api.html](https://www.cyclecalcs.com/api.html)
- **Base URL:** `https://www.cyclecalcs.com/v2`

#### Tags

- Places

#### Properties

- [OpenAPI](openapi/cyclecalcs-places-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cyclecalcs-places-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-places-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://www.cyclecalcs.com/api/reference.html)
- [Documentation](https://www.cyclecalcs.com/api/keys.html)
- [Documentation](https://www.cyclecalcs.com/api/errors.html)
- [Documentation](https://www.cyclecalcs.com/api/status.html)
- [Documentation](https://www.cyclecalcs.com/api/accuracy.html)
- [L L Ms Txt](https://www.cyclecalcs.com/llms.txt)
- [L L Ms Txt](https://www.cyclecalcs.com/v2/llms-full.txt)

### CycleCalcs Planet Board API

The Planet Board API from CycleCalcs — 1 operation(s) for planet board.

- **Human URL:** [https://www.cyclecalcs.com/api.html](https://www.cyclecalcs.com/api.html)
- **Base URL:** `https://www.cyclecalcs.com/v2`

#### Tags

- Planet Board

#### Properties

- [OpenAPI](openapi/cyclecalcs-planet-board-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cyclecalcs-planet-board-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-planet-board-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://www.cyclecalcs.com/api/reference.html)
- [Documentation](https://www.cyclecalcs.com/api/keys.html)
- [Documentation](https://www.cyclecalcs.com/api/errors.html)
- [Documentation](https://www.cyclecalcs.com/api/status.html)
- [Documentation](https://www.cyclecalcs.com/api/accuracy.html)
- [L L Ms Txt](https://www.cyclecalcs.com/llms.txt)
- [L L Ms Txt](https://www.cyclecalcs.com/v2/llms-full.txt)

### CycleCalcs Planet Events API

The Planet Events API from CycleCalcs — 1 operation(s) for planet events.

- **Human URL:** [https://www.cyclecalcs.com/api.html](https://www.cyclecalcs.com/api.html)
- **Base URL:** `https://www.cyclecalcs.com/v2`

#### Tags

- Planet Events

#### Properties

- [OpenAPI](openapi/cyclecalcs-planet-events-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cyclecalcs-planet-events-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-planet-events-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://www.cyclecalcs.com/api/reference.html)
- [Documentation](https://www.cyclecalcs.com/api/keys.html)
- [Documentation](https://www.cyclecalcs.com/api/errors.html)
- [Documentation](https://www.cyclecalcs.com/api/status.html)
- [Documentation](https://www.cyclecalcs.com/api/accuracy.html)
- [L L Ms Txt](https://www.cyclecalcs.com/llms.txt)
- [L L Ms Txt](https://www.cyclecalcs.com/v2/llms-full.txt)

### CycleCalcs Positions API

The Positions API from CycleCalcs — 1 operation(s) for positions.

- **Human URL:** [https://www.cyclecalcs.com/api.html](https://www.cyclecalcs.com/api.html)
- **Base URL:** `https://www.cyclecalcs.com/v2`

#### Tags

- Positions

#### Properties

- [OpenAPI](openapi/cyclecalcs-positions-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cyclecalcs-positions-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-positions-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://www.cyclecalcs.com/api/reference.html)
- [Documentation](https://www.cyclecalcs.com/api/keys.html)
- [Documentation](https://www.cyclecalcs.com/api/errors.html)
- [Documentation](https://www.cyclecalcs.com/api/status.html)
- [Documentation](https://www.cyclecalcs.com/api/accuracy.html)
- [L L Ms Txt](https://www.cyclecalcs.com/llms.txt)
- [L L Ms Txt](https://www.cyclecalcs.com/v2/llms-full.txt)

### CycleCalcs Retrogrades API

The Retrogrades API from CycleCalcs — 1 operation(s) for retrogrades.

- **Human URL:** [https://www.cyclecalcs.com/api.html](https://www.cyclecalcs.com/api.html)
- **Base URL:** `https://www.cyclecalcs.com/v2`

#### Tags

- Retrogrades

#### Properties

- [OpenAPI](openapi/cyclecalcs-retrogrades-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cyclecalcs-retrogrades-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-retrogrades-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://www.cyclecalcs.com/api/reference.html)
- [Documentation](https://www.cyclecalcs.com/api/keys.html)
- [Documentation](https://www.cyclecalcs.com/api/errors.html)
- [Documentation](https://www.cyclecalcs.com/api/status.html)
- [Documentation](https://www.cyclecalcs.com/api/accuracy.html)
- [L L Ms Txt](https://www.cyclecalcs.com/llms.txt)
- [L L Ms Txt](https://www.cyclecalcs.com/v2/llms-full.txt)

### CycleCalcs Rise Set API

The Rise Set API from CycleCalcs — 1 operation(s) for rise set.

- **Human URL:** [https://www.cyclecalcs.com/api.html](https://www.cyclecalcs.com/api.html)
- **Base URL:** `https://www.cyclecalcs.com/v2`

#### Tags

- Rise Set

#### Properties

- [OpenAPI](openapi/cyclecalcs-rise-set-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cyclecalcs-rise-set-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-rise-set-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://www.cyclecalcs.com/api/reference.html)
- [Documentation](https://www.cyclecalcs.com/api/keys.html)
- [Documentation](https://www.cyclecalcs.com/api/errors.html)
- [Documentation](https://www.cyclecalcs.com/api/status.html)
- [Documentation](https://www.cyclecalcs.com/api/accuracy.html)
- [L L Ms Txt](https://www.cyclecalcs.com/llms.txt)
- [L L Ms Txt](https://www.cyclecalcs.com/v2/llms-full.txt)

### CycleCalcs Seasons API

The Seasons API from CycleCalcs — 1 operation(s) for seasons.

- **Human URL:** [https://www.cyclecalcs.com/api.html](https://www.cyclecalcs.com/api.html)
- **Base URL:** `https://www.cyclecalcs.com/v2`

#### Tags

- Seasons

#### Properties

- [OpenAPI](openapi/cyclecalcs-seasons-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cyclecalcs-seasons-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-seasons-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://www.cyclecalcs.com/api/reference.html)
- [Documentation](https://www.cyclecalcs.com/api/keys.html)
- [Documentation](https://www.cyclecalcs.com/api/errors.html)
- [Documentation](https://www.cyclecalcs.com/api/status.html)
- [Documentation](https://www.cyclecalcs.com/api/accuracy.html)
- [L L Ms Txt](https://www.cyclecalcs.com/llms.txt)
- [L L Ms Txt](https://www.cyclecalcs.com/v2/llms-full.txt)

### CycleCalcs Separation API

The Separation API from CycleCalcs — 1 operation(s) for separation.

- **Human URL:** [https://www.cyclecalcs.com/api.html](https://www.cyclecalcs.com/api.html)
- **Base URL:** `https://www.cyclecalcs.com/v2`

#### Tags

- Separation

#### Properties

- [OpenAPI](openapi/cyclecalcs-separation-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cyclecalcs-separation-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-separation-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://www.cyclecalcs.com/api/reference.html)
- [Documentation](https://www.cyclecalcs.com/api/keys.html)
- [Documentation](https://www.cyclecalcs.com/api/errors.html)
- [Documentation](https://www.cyclecalcs.com/api/status.html)
- [Documentation](https://www.cyclecalcs.com/api/accuracy.html)
- [L L Ms Txt](https://www.cyclecalcs.com/llms.txt)
- [L L Ms Txt](https://www.cyclecalcs.com/v2/llms-full.txt)

### CycleCalcs Sidereal Time API

The Sidereal Time API from CycleCalcs — 1 operation(s) for sidereal time.

- **Human URL:** [https://www.cyclecalcs.com/api.html](https://www.cyclecalcs.com/api.html)
- **Base URL:** `https://www.cyclecalcs.com/v2`

#### Tags

- Sidereal Time

#### Properties

- [OpenAPI](openapi/cyclecalcs-sidereal-time-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cyclecalcs-sidereal-time-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-sidereal-time-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://www.cyclecalcs.com/api/reference.html)
- [Documentation](https://www.cyclecalcs.com/api/keys.html)
- [Documentation](https://www.cyclecalcs.com/api/errors.html)
- [Documentation](https://www.cyclecalcs.com/api/status.html)
- [Documentation](https://www.cyclecalcs.com/api/accuracy.html)
- [L L Ms Txt](https://www.cyclecalcs.com/llms.txt)
- [L L Ms Txt](https://www.cyclecalcs.com/v2/llms-full.txt)

### CycleCalcs Sky Quality API

The Sky Quality API from CycleCalcs — 1 operation(s) for sky quality.

- **Human URL:** [https://www.cyclecalcs.com/api.html](https://www.cyclecalcs.com/api.html)
- **Base URL:** `https://www.cyclecalcs.com/v2`

#### Tags

- Sky Quality

#### Properties

- [OpenAPI](openapi/cyclecalcs-sky-quality-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cyclecalcs-sky-quality-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-sky-quality-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://www.cyclecalcs.com/api/reference.html)
- [Documentation](https://www.cyclecalcs.com/api/keys.html)
- [Documentation](https://www.cyclecalcs.com/api/errors.html)
- [Documentation](https://www.cyclecalcs.com/api/status.html)
- [Documentation](https://www.cyclecalcs.com/api/accuracy.html)
- [L L Ms Txt](https://www.cyclecalcs.com/llms.txt)
- [L L Ms Txt](https://www.cyclecalcs.com/v2/llms-full.txt)

### CycleCalcs Sun API

The Sun API from CycleCalcs — 1 operation(s) for sun.

- **Human URL:** [https://www.cyclecalcs.com/api.html](https://www.cyclecalcs.com/api.html)
- **Base URL:** `https://www.cyclecalcs.com/v2`

#### Tags

- Sun

#### Properties

- [OpenAPI](openapi/cyclecalcs-sun-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cyclecalcs-sun-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-sun-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://www.cyclecalcs.com/api/reference.html)
- [Documentation](https://www.cyclecalcs.com/api/keys.html)
- [Documentation](https://www.cyclecalcs.com/api/errors.html)
- [Documentation](https://www.cyclecalcs.com/api/status.html)
- [Documentation](https://www.cyclecalcs.com/api/accuracy.html)
- [L L Ms Txt](https://www.cyclecalcs.com/llms.txt)
- [L L Ms Txt](https://www.cyclecalcs.com/v2/llms-full.txt)

### CycleCalcs Time API

The Time API from CycleCalcs — 1 operation(s) for time.

- **Human URL:** [https://www.cyclecalcs.com/api.html](https://www.cyclecalcs.com/api.html)
- **Base URL:** `https://www.cyclecalcs.com/v2`

#### Tags

- Time

#### Properties

- [OpenAPI](openapi/cyclecalcs-time-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cyclecalcs-time-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-time-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://www.cyclecalcs.com/api/reference.html)
- [Documentation](https://www.cyclecalcs.com/api/keys.html)
- [Documentation](https://www.cyclecalcs.com/api/errors.html)
- [Documentation](https://www.cyclecalcs.com/api/status.html)
- [Documentation](https://www.cyclecalcs.com/api/accuracy.html)
- [L L Ms Txt](https://www.cyclecalcs.com/llms.txt)
- [L L Ms Txt](https://www.cyclecalcs.com/v2/llms-full.txt)

### CycleCalcs Today API

The Today API from CycleCalcs — 1 operation(s) for today.

- **Human URL:** [https://www.cyclecalcs.com/api.html](https://www.cyclecalcs.com/api.html)
- **Base URL:** `https://www.cyclecalcs.com/v2`

#### Tags

- Today

#### Properties

- [OpenAPI](openapi/cyclecalcs-today-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cyclecalcs-today-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-today-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://www.cyclecalcs.com/api/reference.html)
- [Documentation](https://www.cyclecalcs.com/api/keys.html)
- [Documentation](https://www.cyclecalcs.com/api/errors.html)
- [Documentation](https://www.cyclecalcs.com/api/status.html)
- [Documentation](https://www.cyclecalcs.com/api/accuracy.html)
- [L L Ms Txt](https://www.cyclecalcs.com/llms.txt)
- [L L Ms Txt](https://www.cyclecalcs.com/v2/llms-full.txt)

### CycleCalcs Twilight API

The Twilight API from CycleCalcs — 1 operation(s) for twilight.

- **Human URL:** [https://www.cyclecalcs.com/api.html](https://www.cyclecalcs.com/api.html)
- **Base URL:** `https://www.cyclecalcs.com/v2`

#### Tags

- Twilight

#### Properties

- [OpenAPI](openapi/cyclecalcs-twilight-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cyclecalcs-twilight-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cyclecalcs-twilight-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://www.cyclecalcs.com/api/reference.html)
- [Documentation](https://www.cyclecalcs.com/api/keys.html)
- [Documentation](https://www.cyclecalcs.com/api/errors.html)
- [Documentation](https://www.cyclecalcs.com/api/status.html)
- [Documentation](https://www.cyclecalcs.com/api/accuracy.html)
- [L L Ms Txt](https://www.cyclecalcs.com/llms.txt)
- [L L Ms Txt](https://www.cyclecalcs.com/v2/llms-full.txt)

## Common Properties

- [Overlay](overlays/cyclecalcs-astronomy-overlay.yaml)
- [Agentic Access](agentic-access/cyclecalcs-agentic-access.yml)
- [Domain Security](security/cyclecalcs-domain-security.yml)
- [Authentication](authentication/cyclecalcs-authentication.yml)
- [Developer Portal](https://www.cyclecalcs.com/api.html)
- [Documentation](https://www.cyclecalcs.com/api/reference.html)
- [API Reference](https://www.cyclecalcs.com/api/reference.html)
- [Getting Started](https://www.cyclecalcs.com/api.html)
- [Support](https://www.cyclecalcs.com/about.html)
- [Pricing](https://rapidapi.com/info-8KZIhinZ9/api/cyclecalcs-astronomy-api3)
- [Sign Up](https://rapidapi.com/info-8KZIhinZ9/api/cyclecalcs-astronomy-api3)
- [Terms of Service](https://www.cyclecalcs.com/api/terms.html)
- [Privacy Policy](https://www.cyclecalcs.com/privacy.html)
- [Status Page](https://stats.uptimerobot.com/b2ue50rVZI)
- [Deprecation](https://www.cyclecalcs.com/api/versioning.html)
- [Lifecycle](lifecycle/cyclecalcs-lifecycle.yml)
- [Conventions](conventions/cyclecalcs-conventions.yml)
- [Idempotency](conventions/cyclecalcs-conventions.yml)
- [Error Catalog](errors/cyclecalcs-problem-types.yml)
- [Conformance](conformance/cyclecalcs-conformance.yml)
- [Well Known](well-known/cyclecalcs-well-known.yml)
- [A P I Catalog](https://www.cyclecalcs.com/.well-known/api-catalog)
- [Packages](packages/cyclecalcs-packages.yml)
- [Vocabulary](vocabulary/cyclecalcs-vocabulary.yml)
- [Data Model](data-model/cyclecalcs-data-model.yml)
- [Sandbox](sandbox/cyclecalcs-sandbox.yml)
- [Components](components/cyclecalcs-components.yml)
- [Rate Limits](rate-limits/cyclecalcs-rate-limits.yml)
- [Plans](plans/cyclecalcs-plans.yml)
- [Examples](examples/_index.yml)
- [L L Ms Txt](llms/cyclecalcs-llms.txt)
- [Agent Skill](skills/_index.yml)
- [Arazzo](arazzo/cyclecalcs-tonights-sky.yml) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)
- [Arazzo](arazzo/cyclecalcs-eclipse-visibility.yml) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)
- [Arazzo](arazzo/cyclecalcs-sun-moon-calendar.yml) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)

## Maintainers

**FN:** CycleCalcs
**Email:** info@cyclecalcs.com
**URL:** https://www.cyclecalcs.com
