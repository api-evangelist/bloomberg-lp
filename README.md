# Bloomberg L.P. (bloomberg-lp)

Bloomberg L.P. is a privately held financial, software, data, and media company founded by Michael Bloomberg in 1981 and headquartered in New York City. The company is best known for the Bloomberg Terminal, which delivers real-time market data, news, analytics, and trading tools to roughly 325,000 subscribers worldwide, and for Bloomberg News, Bloomberg.com, Bloomberg Television, and Bloomberg Industry Group (formerly Bloomberg BNA). On the developer side, Bloomberg exposes the BLPAPI (Bloomberg API) family across the Desktop API, Server API, B-PIPE, and Data License products via SDKs in C++, Java, Python and .NET, and operates OpenFIGI — the free, public Financial Instrument Global Identifier (FIGI) symbology API and the most openly accessible Bloomberg API surface for the general developer audience.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/bloomberg-lp/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/bloomberg-lp/refs/heads/main/apis.yml)

## Tags

- Financial Services
- Market Data
- News
- Reference Data
- Symbology
- Terminal

## Timestamps

- **Created:** 2024-01-01
- **Modified:** 2026-05-23

## APIs

### OpenFIGI API

OpenFIGI is the free, public REST API operated by Bloomberg as the FIGI Registration Authority for the Object Management Group (OMG) Financial Instrument Global Identifier standard. It maps third-party identifiers (TICKER, ISIN, CUSIP, SEDOL, BBGID, COMMON, etc.) to FIGIs and exposes search and filter endpoints across hundreds of millions of active and inactive instruments spanning equities, fixed income, derivatives, currencies, commodities, indices, and crypto. The /v3 API is JSON over HTTPS at api.openfigi.com, with optional X-OPENFIGI-APIKEY authentication that lifts rate limits.

- **Human URL:** [https://www.openfigi.com/api](https://www.openfigi.com/api)
- **Base URL:** `https://api.openfigi.com/v3`

#### Tags

- Symbology
- Reference Data
- FIGI
- Free API
- Open Standard

#### Properties

- [Documentation](https://www.openfigi.com/api/documentation)
- [API Reference](https://www.openfigi.com/api/documentation)
- [Getting Started](https://www.openfigi.com/api)
- [Sign Up](https://www.openfigi.com/user/signup)
- [A P I Key](https://www.openfigi.com/user/signup)
- [Rate Limits](https://www.openfigi.com/api/documentation)
- [Terms of Service](https://www.openfigi.com/about/terms)
- [GitHub Organization](https://github.com/OpenFIGI)
- [SDK](https://github.com/OpenFIGI/api-examples)
- [OpenAPI](openapi/openfigi-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/openfigi.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/openfigi.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Spectral Rules](rules/openfigi-rules.yml)
- [Naftiko Workflow Capability](capabilities/symbology-resolution.yaml)
- [JSON Schema](json-schema/openfigi-figi-record-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [J S O N Schema Mapping Job](json-schema/openfigi-mapping-job-schema.json)
- [JSON Structure](json-structure/openfigi-figi-record-structure.json)
- [J S O N L D Context](json-ld/bloomberg-lp-context.jsonld)
- [Examples](examples/)

### Bloomberg BLPAPI (Desktop API)

BLPAPI is Bloomberg's core programming interface for the Bloomberg Terminal Desktop API, Server API (SAPI), B-PIPE, and Platform products. It exposes a unified asynchronous session/event/subscription model for requesting reference data, historical data, intraday bars and ticks, market data subscriptions, instrument lookup, and field information via services such as //blp/refdata, //blp/mktdata, //blp/apiflds, and //blp/instruments. SDKs are published in C++, Java, Python, and .NET; the Python SDK alone has 39 releases and ships against version 3.26.4.

- **Human URL:** [https://bloomberg.github.io/blpapi-docs/](https://bloomberg.github.io/blpapi-docs/)

#### Tags

- BLPAPI
- Desktop API
- Reference Data
- Historical Data
- Market Data
- SDK

#### Properties

- [Documentation](https://bloomberg.github.io/blpapi-docs/)
- [API Reference](https://bloomberg.github.io/blpapi-docs/cpp/3.26/index.html)
- [Getting Started](https://bloomberg.github.io/blpapi-docs/)
- [Developer Guide](https://data.bloomberglp.com/professional/sites/10/2017/03/BLPAPI-Core-Developer-Guide.pdf)
- [GitHub Organization](https://github.com/bloomberg)
- [SDK](https://github.com/msitt/blpapi-python)
- [S D K Python](https://pypi.org/project/blpapi/)
- [S D K Java](https://bloomberg.github.io/blpapi-docs/java/3.26/index.html)
- [S D K Dot Net](https://bloomberg.github.io/blpapi-docs/dotnet/3.26/index.html)
- [S D K C P P](https://bloomberg.github.io/blpapi-docs/cpp/3.26/index.html)
- [Pricing](https://www.bloomberg.com/professional/pricing/)
- [License](https://github.com/msitt/blpapi-python/blob/master/License.txt)
- [Postman Collection](collections/openfigi.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/openfigi.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Bloomberg Server API (SAPI)

Server-side variant of BLPAPI that lets a single Bloomberg Terminal user serve real-time market data, historical data, reference data, and calculation-engine output to multiple in-house applications and end users from a Linux or Windows server. Uses the same BLPAPI SDKs (C, C++, .NET, Python, Java) as the Desktop API.

- **Human URL:** [https://www.bloomberg.com/professional/products/data/data-connectivity/server-api/](https://www.bloomberg.com/professional/products/data/data-connectivity/server-api/)

#### Tags

- Server API
- SAPI
- Enterprise
- Real-Time Data

#### Properties

- [Documentation](https://www.bloomberg.com/professional/products/data/data-connectivity/server-api/)
- [API Reference](https://bloomberg.github.io/blpapi-docs/)
- [Getting Started](https://bloomberg.github.io/blpapi-docs/)
- [Pricing](https://www.bloomberg.com/professional/pricing/)
- [Postman Collection](collections/openfigi.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/openfigi.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Bloomberg B-PIPE

Bloomberg's flagship enterprise market data feed, delivering normalized, consolidated, real-time and reference data across all asset classes with Bloomberg's entitlement and identifier infrastructure. Offered as Bloomberg-hosted B-PIPE and Managed B-PIPE, with access via BLPAPI.

- **Human URL:** [https://www.bloomberg.com/professional/products/data/enterprise-catalog/data-feeds/b-pipe/](https://www.bloomberg.com/professional/products/data/enterprise-catalog/data-feeds/b-pipe/)

#### Tags

- B-PIPE
- Market Data Feed
- Enterprise
- Real-Time Data

#### Properties

- [Documentation](https://www.bloomberg.com/professional/products/data/enterprise-catalog/data-feeds/b-pipe/)
- [API Reference](https://bloomberg.github.io/blpapi-docs/)
- [Pricing](https://www.bloomberg.com/professional/pricing/)
- [Postman Collection](collections/openfigi.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/openfigi.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Bloomberg Data License (DL / BEAP)

Bulk reference, pricing, regulatory, and alternative-data delivery service covering over 50 million securities and 30,000+ fields. Accessed via REST API (HAPI / Bloomberg Enterprise Access Point), SFTP, or cloud delivery (AWS, Azure, GCP). Suited to back-office, risk, compliance and research use cases that do not require streaming market data.

- **Human URL:** [https://www.bloomberg.com/professional/products/data/data-management/data-license/](https://www.bloomberg.com/professional/products/data/data-management/data-license/)

#### Tags

- Data License
- Reference Data
- Bulk Data
- Regulatory Data
- Alternative Data

#### Properties

- [Documentation](https://www.bloomberg.com/professional/products/data/data-management/data-license/)
- [API Reference](https://developer.bloomberg.com/)
- [Pricing](https://www.bloomberg.com/professional/pricing/)
- [Postman Collection](collections/openfigi.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/openfigi.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Bloomberg Terminal

Bloomberg's flagship subscription product — a desktop application delivering real-time market data, news, analytics, trading, messaging, and research to financial professionals globally. The Terminal is also the entitlement host for the Desktop BLPAPI.

- **Human URL:** [https://www.bloomberg.com/professional/products/bloomberg-terminal/](https://www.bloomberg.com/professional/products/bloomberg-terminal/)

#### Tags

- Terminal
- Subscription
- Workstation

#### Properties

- [Documentation](https://www.bloomberg.com/professional/products/bloomberg-terminal/)
- [Pricing](https://www.bloomberg.com/professional/pricing/)
- [Sign Up](https://www.bloomberg.com/professional/request-demo/)
- [Postman Collection](collections/openfigi.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/openfigi.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Landing Page](https://www.bloomberg.com/)
- [Company](https://www.bloomberg.com/company/)
- [Professional Portal](https://www.bloomberg.com/professional/)
- [Developer Portal](https://developer.bloomberg.com/)
- [Open F I G I Portal](https://www.openfigi.com/)
- [Documentation](https://bloomberg.github.io/blpapi-docs/)
- [Support](https://www.bloomberg.com/professional/support/)
- [Contact](https://www.bloomberg.com/professional/contact-menu/)
- [Pricing](https://www.bloomberg.com/professional/pricing/)
- [Login](https://bba.bloomberg.net/)
- [Terms of Service](https://www.bloomberg.com/notices/tos/)
- [Privacy Policy](https://www.bloomberg.com/notices/privacy/)
- [GitHub Organization](https://github.com/bloomberg)
- [Open F I G I Git Hub Organization](https://github.com/OpenFIGI)
- [LinkedIn](https://www.linkedin.com/company/bloomberg/)
- [X Twitter](https://twitter.com/business)
- [Blog](https://www.bloomberg.com/company/stories/)
- [Tech Blog](https://www.bloomberg.com/company/stories/category/tech-at-bloomberg/)
- [News](https://www.bloomberg.com/news/)
- [Plans](plans/bloomberg-lp-plans-pricing.yml)
- [Rate Limits](rate-limits/bloomberg-lp-rate-limits.yml)
- [Fin Ops](finops/bloomberg-lp-finops.yml)
- [Vocabulary](vocabulary/bloomberg-lp-vocabulary.yml)
- [J S O N L D Context](json-ld/bloomberg-lp-context.jsonld)
- [Features](undefined)
- [Use Cases](undefined)
- [Integrations](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
**URL:** https://apievangelist.com
