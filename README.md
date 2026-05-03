# Typesense

Typesense is a fast, typo-tolerant, open-source search engine designed for developer productivity. It provides instant search experiences with support for full-text search, faceting, filtering, sorting, geo-based search, vector search, and conversational AI search (RAG). Available as an open-source self-hosted solution or as a managed cloud service.

**URL:** [https://typesense.org](https://typesense.org)

## Tags

Full-Text Search, Open Source, Search Engine, Typo Tolerance, Vector Search

## Timestamps

- **Created:** 2026-05-03
- **Modified:** 2026-05-03

## APIs

### Typesense Search API

Core REST API for managing collections, indexing documents, and performing full-text, faceted, filtered, sorted, geo-based, and multi-search queries.

**Human URL:** [https://typesense.org/docs/](https://typesense.org/docs/)
**Base URL:** http://localhost:8108

**Tags:** Collections, Documents, Full-Text Search, Search

**Properties**
- [Documentation](https://typesense.org/docs/)
- [OpenAPI](openapi/typesense-search-api-openapi.yml)
- [API Reference](https://typesense.org/docs/latest/api/)

### Typesense Vector Search API

Vector and hybrid search using dense embeddings with HNSW indexing, supporting semantic similarity search combined with keyword search.

**Human URL:** [https://typesense.org/docs/guide/vector-search.html](https://typesense.org/docs/guide/vector-search.html)

**Tags:** Embeddings, Hybrid Search, Semantic Search, Vector Search

**Properties**
- [Documentation](https://typesense.org/docs/guide/vector-search.html)
- [OpenAPI](openapi/typesense-vector-search-api-openapi.yml)

### Typesense Conversational Search API

AI-powered RAG search using conversation models (OpenAI, Cloudflare Workers AI) for natural language Q&A over indexed data.

**Human URL:** [https://typesense.org/docs/guide/conversational-search-rag.html](https://typesense.org/docs/guide/conversational-search-rag.html)

**Tags:** AI, Conversational Search, LLM, RAG

**Properties**
- [Documentation](https://typesense.org/docs/guide/conversational-search-rag.html)
- [OpenAPI](openapi/typesense-conversational-search-api-openapi.yml)

### Typesense Analytics API

Search analytics for tracking events, popular queries, no-result queries, and click analytics with rule-based aggregation.

**Human URL:** [https://typesense.org/docs/guide/analytics-query-suggestions.html](https://typesense.org/docs/guide/analytics-query-suggestions.html)

**Tags:** Analytics, Events, Query Insights, Search Analytics

**Properties**
- [Documentation](https://typesense.org/docs/guide/analytics-query-suggestions.html)
- [OpenAPI](openapi/typesense-analytics-api-openapi.yml)

### Typesense Cloud Management API

Programmatic provisioning and management of Typesense Cloud clusters, configuration changes, and API key generation.

**Human URL:** [https://typesense.org/docs/cloud-management-api/v1/cluster-management.html](https://typesense.org/docs/cloud-management-api/v1/cluster-management.html)

**Tags:** Cluster Management, Cloud, Infrastructure, Provisioning

**Properties**
- [Documentation](https://typesense.org/docs/cloud-management-api/v1/cluster-management.html)
- [OpenAPI](openapi/typesense-cloud-management-api-openapi.yml)

## Common Properties

- [Website](https://typesense.org)
- [Documentation](https://typesense.org/docs/)
- [GitHub Organization](https://github.com/typesense)
- [Blog](https://typesense.org/blog/)
- [npm](https://www.npmjs.com/package/typesense)
- [Docker Hub](https://hub.docker.com/r/typesense/typesense)
- [Pricing](https://typesense.org/pricing/)
- [Terms of Service](https://typesense.org/terms/)
- [Privacy Policy](https://typesense.org/privacy/)

## Artifacts

### JSON Schemas

| Schema | Description |
|---|---|
| [Collection](json-schema/typesense-collection-schema.json) | Collection schema definition |
| [Search Result](json-schema/typesense-search-result-schema.json) | Search response object |
| [Analytics Event](json-schema/typesense-analytics-event-schema.json) | Analytics event payload |

### JSON Structures

| Structure | Description |
|---|---|
| [Collection](json-structure/typesense-collection-structure.json) | Collection field documentation |
| [Search Result](json-structure/typesense-search-result-structure.json) | Search response field documentation |

### JSON-LD Context

- [Typesense Context](json-ld/typesense-context.jsonld)

### Examples

| Example | Description |
|---|---|
| [Search](examples/typesense-search-example.json) | Full-text search with faceting |
| [Create Collection](examples/typesense-create-collection-example.json) | Collection schema creation |
| [Index Document](examples/typesense-index-document-example.json) | Document indexing |
| [Multi-Search](examples/typesense-multi-search-example.json) | Multi-collection search |

### Spectral Rules

- [Typesense Rules](rules/typesense-rules.yml) — Enforces Typesense API naming, security, and schema conventions

### Naftiko Capabilities

**Shared API Definitions**
- [Search API](capabilities/shared/search-api.yaml) — Core search and collection management
- [Vector Search API](capabilities/shared/vector-search-api.yaml) — Vector and hybrid search

**Workflow Capabilities**
- [Search and Discovery](capabilities/search-and-discovery.yaml) — Full-text, vector, and hybrid search (8 tools)

### Vocabulary

- [Typesense Vocabulary](vocabulary/typesense-vocabulary.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
