# Typesense (typesense)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Typesense is a fast, typo-tolerant, open-source search engine designed for developer productivity. It provides instant search experiences with support for full-text search, faceting, filtering, sorting, geo-based search, vector search, and conversational AI search. Typesense is available as an open-source self-hosted solution or as a managed cloud service via Typesense Cloud.

**APIs.json:** [https://typesense.org](https://typesense.org)

## Tags

- Full-Text Search
- Open Source
- Search Engine
- Typo Tolerance
- Vector Search

## Timestamps

- **Created:** 2026-05-03
- **Modified:** 2026-05-19

## APIs

### Typesense Search API

The core Typesense REST API for managing collections, indexing documents, and performing full-text, faceted, filtered, sorted, geo-based, and multi-search queries. Supports synonym sets, curation sets, collection aliases, stopwords, presets, stemming dictionaries, API keys, and cluster operations.

- **Human URL:** [https://typesense.org/docs/](https://typesense.org/docs/)
- **Base URL:** `http://localhost:8108`

#### Tags

- Collections
- Documents
- Full-Text Search
- Search

#### Properties

- [Documentation](https://typesense.org/docs/)
- [OpenAPI](openapi/typesense-search-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/typesense-search-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/typesense-search-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Getting Started](https://typesense.org/docs/guide/)
- [API Reference](https://typesense.org/docs/latest/api/)

### Typesense Vector Search API

The Typesense Vector Search API extends the core search capabilities with vector and hybrid search. It supports indexing embedding fields, querying by vector proximity, and combining semantic vector search with keyword search for superior relevance.

- **Human URL:** [https://typesense.org/docs/guide/vector-search.html](https://typesense.org/docs/guide/vector-search.html)
- **Base URL:** `http://localhost:8108`

#### Tags

- Embeddings
- Hybrid Search
- Semantic Search
- Vector Search

#### Properties

- [Documentation](https://typesense.org/docs/guide/vector-search.html)
- [OpenAPI](openapi/typesense-vector-search-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/typesense-vector-search-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/typesense-vector-search-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Typesense Conversational Search API

The Typesense Conversational Search API enables AI-powered question answering over your search index. It supports conversation models (OpenAI, Cloudflare Workers AI), NL search models, and stateful multi-turn conversations over indexed data.

- **Human URL:** [https://typesense.org/docs/guide/conversational-search-rag.html](https://typesense.org/docs/guide/conversational-search-rag.html)
- **Base URL:** `http://localhost:8108`

#### Tags

- AI
- Conversational Search
- LLM
- RAG

#### Properties

- [Documentation](https://typesense.org/docs/guide/conversational-search-rag.html)
- [OpenAPI](openapi/typesense-conversational-search-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/typesense-conversational-search-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/typesense-conversational-search-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Typesense Analytics API

The Typesense Analytics API tracks search events and provides insights into search behavior, popular queries, no-result queries, and click analytics. Supports rule-based aggregation and analytics data exports.

- **Human URL:** [https://typesense.org/docs/guide/analytics-query-suggestions.html](https://typesense.org/docs/guide/analytics-query-suggestions.html)
- **Base URL:** `http://localhost:8108`

#### Tags

- Analytics
- Events
- Query Insights
- Search Analytics

#### Properties

- [Documentation](https://typesense.org/docs/guide/analytics-query-suggestions.html)
- [OpenAPI](openapi/typesense-analytics-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/typesense-analytics-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/typesense-analytics-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Typesense Cloud Management API

The Typesense Cloud Management API enables provisioning and managing Typesense Cloud clusters programmatically. Supports creating, updating, terminating clusters, scheduling configuration changes, managing server configuration parameters, and generating API keys.

- **Human URL:** [https://typesense.org/docs/cloud-management-api/v1/cluster-management.html](https://typesense.org/docs/cloud-management-api/v1/cluster-management.html)
- **Base URL:** `https://cloud.typesense.org/api/v1`

#### Tags

- Cluster Management
- Cloud
- Infrastructure
- Provisioning

#### Properties

- [Documentation](https://typesense.org/docs/cloud-management-api/v1/cluster-management.html)
- [OpenAPI](openapi/typesense-cloud-management-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/typesense-cloud-management-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/typesense-cloud-management-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/typesense)
- [Website](https://typesense.org)
- [Documentation](https://typesense.org/docs/)
- [GitHub Organization](https://github.com/typesense)
- [Blog](https://typesense.org/blog/)
- [Slack  Community](https://join.slack.com/t/typesense-community/shared_invite/zt-2fetvh0pw-ft5y2YQlq4FS3fVDFTfWJA)
- [Docker  Hub](https://hub.docker.com/r/typesense/typesense)
- [npm](https://www.npmjs.com/package/typesense)
- [Pricing](https://typesense.org/pricing/)
- [Terms of Service](https://typesense.org/terms/)
- [Privacy Policy](https://typesense.org/privacy/)
- [JSON-LD](json-ld/typesense-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [JSON Schema](json-schema/typesense-collection-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/typesense-search-result-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/typesense-analytics-event-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/typesense-collection-structure.json)
- [JSON Structure](json-structure/typesense-search-result-structure.json)
- [Vocabulary](vocabulary/typesense-vocabulary.yml)
- [Spectral Rules](rules/typesense-rules.yml)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
