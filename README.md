# Bloomberg L.P.

Bloomberg L.P. is a privately held financial, software, data, and media company founded by Michael Bloomberg in 1981 and headquartered in New York City. The company is best known for the **Bloomberg Terminal**, which delivers real-time market data, news, analytics, and trading tools to roughly 325,000 subscribers worldwide, and for **Bloomberg News**, **Bloomberg.com**, **Bloomberg Television**, and **Bloomberg Industry Group** (formerly Bloomberg BNA).

On the developer side, Bloomberg exposes two very different surfaces:

1. **BLPAPI** — the unified Bloomberg API across the Desktop API, Server API (SAPI), B-PIPE, and Data License products, with official SDKs in C++, Java, Python, and .NET. Access is entitled through a Bloomberg Terminal subscription or enterprise contract; Bloomberg does not publish list pricing.
2. **OpenFIGI** — the free, public Financial Instrument Global Identifier symbology API, operated by Bloomberg as Registration Authority for the OMG FIGI standard. OpenFIGI is the single most openly accessible Bloomberg API and is the focus of the artifacts in this repo.

This profile pipelines only what is publicly documented.

## APIs Documented

| API | Type | Auth | Pricing |
|---|---|---|---|
| OpenFIGI API (`/v3`) | REST / JSON | Optional `X-OPENFIGI-APIKEY` | Free |
| Bloomberg BLPAPI (Desktop API) | SDK (C++/Java/Python/.NET) | Terminal entitlement | Terminal subscription (custom-quoted) |
| Bloomberg Server API (SAPI) | SDK over BLPAPI | Terminal entitlement | Custom-quoted |
| Bloomberg B-PIPE | Enterprise feed via BLPAPI | Enterprise contract | Custom-quoted |
| Bloomberg Data License (HAPI / BEAP) | REST / SFTP / Cloud | Enterprise contract | Custom-quoted |
| Bloomberg Terminal | Subscription product | — | Custom-quoted |

The full machine-readable inventory is in [`apis.yml`](./apis.yml).

## Artifacts

| Folder | Contents |
|---|---|
| [`openapi/`](./openapi/) | OpenAPI 3.0 spec for OpenFIGI v3 (4 paths, 5 schemas, security scheme for `X-OPENFIGI-APIKEY`) |
| [`examples/`](./examples/) | OpenFIGI mapping / search / filter request and response examples |
| [`rules/`](./rules/) | Spectral ruleset enforcing OpenFIGI conventions (HTTPS, header name, error responses, Title Case, FIGI pattern) |
| [`capabilities/`](./capabilities/) | Naftiko shared capability (`shared/openfigi.yaml`) and the `symbology-resolution` workflow capability |
| [`json-schema/`](./json-schema/) | JSON Schemas for `FigiRecord` and `MappingJob` |
| [`json-structure/`](./json-structure/) | Portable JSON Structure for `FigiRecord` |
| [`json-ld/`](./json-ld/) | JSON-LD context bridging FIGI vocabulary to schema.org and FIBO |
| [`vocabulary/`](./vocabulary/) | Bloomberg / OpenFIGI domain vocabulary |
| [`plans/`](./plans/) | API Commons Plans 0.1 plans-and-pricing document |
| [`rate-limits/`](./rate-limits/) | API Commons Rate Limits 0.1 document (OpenFIGI ceilings + BLPAPI notes) |
| [`finops/`](./finops/) | FOCUS 1.3 / FinOps Framework alignment for Bloomberg's mixed free + commercial surfaces |

## OpenFIGI Quick Reference

Base URL: `https://api.openfigi.com/v3`

| Method | Path | Purpose |
|---|---|---|
| POST | `/mapping` | Map third-party identifiers (TICKER, ID_ISIN, ID_CUSIP, ID_SEDOL, ID_BB_GLOBAL, OCC_SYMBOL, …) to FIGIs |
| GET  | `/mapping/values/{key}` | List valid enum values for fields such as `idType`, `exchCode`, `currency`, `marketSecDes` |
| POST | `/search` | Keyword search across the FIGI universe with cursor pagination |
| POST | `/filter` | Filtered search returning records sorted by FIGI plus a total count |

Authentication: optional API key in the `X-OPENFIGI-APIKEY` header. Sign up at [openfigi.com/user/signup](https://www.openfigi.com/user/signup).

Rate limits (anonymous → with API key):
- `/mapping`: 25/min, 10 jobs per request → 25/6s, 100 jobs per request
- `/search` and `/filter`: 5/min → 20/min (15,000 record cap per query)

Note: OpenFIGI `/v2` is deprecated with a sunset date of **July 1, 2026**.

## Bloomberg GitHub Footprint

- [`github.com/bloomberg`](https://github.com/bloomberg) — 216 public repos. Top projects include `memray` (15k+ stars), `blazingmq` (3.2k), `bde` (1.8k), `pystack` (1.2k), `stricli` (1k). BLPAPI-named repos (`blpapi-node`, `blpapi-http`, `blpapi-hs`) are archived; the canonical SDKs ship on Bloomberg's website rather than as the primary GitHub home.
- [`github.com/OpenFIGI`](https://github.com/OpenFIGI) — one repo, `api-examples`, 212 stars, Apache 2.0, examples in C#, Java, Node, Python, shell, and Swift.

## Notable Absences

- No public OpenAPI/Swagger specification published by Bloomberg or OpenFIGI; the OpenAPI in this repo was authored from the OpenFIGI documentation.
- No public price list for Terminal, BLPAPI, B-PIPE, or Data License.
- `developer.bloomberg.com`, `data.bloomberg.com`, and most `bloomberg.com/professional/*` pages return 403 to anonymous fetchers — what is documented here was derived from the openly accessible OpenFIGI, GitHub, and `bloomberg.github.io/blpapi-docs/` surfaces.

## Maintainer

- Kin Lane — kin@apievangelist.com — [apievangelist.com](https://apievangelist.com)
