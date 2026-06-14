# Typesense GraphQL Schema

## Overview

This GraphQL schema provides a conceptual type system for the [Typesense](https://typesense.org) open-source search engine REST API. Typesense is a fast, typo-tolerant search engine built for developer productivity, supporting full-text search, faceting, filtering, vector search, and conversational AI search.

The schema covers all major Typesense resource domains:

- **Collections** — schema management (create, update, delete, list)
- **Documents** — indexing, upserting, updating, deleting, bulk import
- **Search** — full-text, faceted, grouped, vector, and multi-search
- **Overrides / Curations** — promoted and hidden result rules
- **Synonyms** — one-way and multi-way synonym sets
- **Aliases** — collection alias pointers
- **API Keys** — scoped, time-limited key management
- **Cluster / Nodes** — health, raft state, node status
- **Analytics** — query, click, and conversion event tracking plus aggregation rules

## Source

- REST API Reference: <https://typesense.org/docs/latest/api/>
- Developer Guide: <https://typesense.org/docs/guide/>
- GitHub: <https://github.com/typesense/typesense>

## Schema File

[typesense-schema.graphql](typesense-schema.graphql)

## Named Types (62)

### Scalars (2)
| Type | Description |
|------|-------------|
| `JSON` | Arbitrary JSON value for untyped document fields and search params |
| `DateTime` | ISO-8601 date-time string |

### Enumerations (4)
| Type | Description |
|------|-------------|
| `FieldType` | All Typesense field data types (string, int32, float, bool, geopoint, object, auto, …) |
| `SynonymType` | `ONE_WAY` or `MULTI_WAY` synonym relationship |
| `APIKeyAction` | Permission actions that can be granted to an API key |
| `OverrideRuleMatch` | `EXACT` or `CONTAINS` query matching for override triggers |
| `NodeStatus` | Node states: `OK`, `INITIALIZING`, `NOT_READY`, `CANDIDATE`, `LEADER` |

### Collection Types (3)
| Type | Description |
|------|-------------|
| `Collection` | Minimal collection reference (name only) |
| `CollectionDetails` | Full collection metadata including fields, document count, and settings |
| `CollectionSchema` | Schema definition used when creating a collection |

### Field Types (6)
| Type | Description |
|------|-------------|
| `FieldDetails` | A field as returned by the API, including runtime stats |
| `FieldInput` | Input object for creating or altering fields |
| `FieldFacet` | Facet toggle for a field |
| `FieldOptional` | Optional toggle for a field |
| `FieldSort` | Sort toggle for a field |
| `FieldIndex` | Index toggle for a field |

### Document Types (3)
| Type | Description |
|------|-------------|
| `Document` | A raw stored document (typed ID, untyped data) |
| `DocumentDetails` | A document with collection context returned after indexing |
| `DocumentUpdate` | Result of a partial document update |

### Search Types (12)
| Type | Description |
|------|-------------|
| `Highlight` | A highlighted text snippet with matched tokens |
| `HighlightDetails` | Extended highlight with value, position indices, and multiple snippets |
| `Hit` | A single search hit with document and highlights |
| `HitDetails` | Full hit with ranking scores, vector distance, and geo distance |
| `SearchResult` | A complete result set for one query |
| `SearchHit` | A hit as it appears inside a grouped result |
| `GroupedResult` | A group of hits sharing a group-by field value |
| `GroupDetails` | Grouped result with found/outOf counts |
| `FacetCount` | A single facet value and its document count |
| `FacetDetails` | All counts for a single facet field |
| `SortField` | A sort specification (field, order, missing-value handling) |
| `PinnedHit` | A document pinned to a specific position in results |
| `HiddenHit` | A document suppressed from search results |

### Query / Filter Helpers (3)
| Type | Description |
|------|-------------|
| `SearchQuery` | A fully-formed search query mirroring the Typesense search API params |
| `SearchFilter` | A filter expression and its parsed form |
| `FacetQuery` | A per-field facet query for narrowing facet value counts |

### Override / Curation Types (6)
| Type | Description |
|------|-------------|
| `OverrideRule` | Condition (query/filter/tags) that triggers an override |
| `OverrideInclude` | A document to promote to a specific position |
| `OverrideExclude` | A document to hide from results |
| `SearchOverride` | A search override (curation rule) |
| `OverrideDetails` | Full override with effective time window and collection context |
| `Curate` | Alternate name for a curation/override rule |
| `CurateDetails` | Full curation details |

### Synonym Types (2)
| Type | Description |
|------|-------------|
| `Synonym` | A synonym set (id + synonyms list) |
| `SynonymDetails` | Full synonym with type, root word, and locale |

### Alias Types (2)
| Type | Description |
|------|-------------|
| `Alias` | A collection alias pointer |
| `AliasDetails` | Full alias details |

### API Key Types (3)
| Type | Description |
|------|-------------|
| `APIKey` | A Typesense API key with actions and collections |
| `APIKeyDetails` | Full key with expiry, value prefix, and embedded search params |
| `APIKeyScope` | A scoped filter attached to an API key |

### Cluster / Node Types (4)
| Type | Description |
|------|-------------|
| `Node` | A node definition (host, port, protocol) |
| `NodeStatus` | A node with its current raft state |
| `Cluster` | A Typesense cluster |
| `ClusterDetails` | Full cluster details with raft state, memory, and version |

### Analytics Types (5)
| Type | Description |
|------|-------------|
| `QueryEvent` | A search query analytics event |
| `ClickEvent` | A click analytics event |
| `ConversionEvent` | A conversion analytics event |
| `AnalyticsRule` | An analytics aggregation rule reference |
| `AnalyticsRuleDetails` | Full analytics rule with source/destination and params |
| `Analytics` | Top-level analytics container |

### Pagination / Error (2)
| Type | Description |
|------|-------------|
| `PageInfo` | Cursor-based pagination info for list responses |
| `Error` | A structured API error with code, message, and optional field |

### Root Types (3)
| Type | Description |
|------|-------------|
| `Query` | Read operations: list/get collections, documents, search, overrides, synonyms, aliases, keys, cluster health, analytics rules |
| `Mutation` | Write operations: create/update/delete all resources, import documents, send analytics events |

## Design Notes

- All untyped document fields use the `JSON` scalar to preserve Typesense's schema-flexible document model.
- `SearchQuery` mirrors the Typesense search API parameter set; actual queries are passed as `JSON` to the `search` mutation to support the full dynamic parameter surface.
- `FieldInput` is the input counterpart to `FieldDetails` and includes the `drop: Boolean` flag used when altering a collection schema.
- Override / Curate types are modeled twice under both Typesense naming conventions (`SearchOverride`/`OverrideDetails` and `Curate`/`CurateDetails`).
- Analytics event mutations map directly to the Typesense Analytics Events API endpoints.
