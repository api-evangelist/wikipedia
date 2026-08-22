# Wikipedia / MediaWiki (wikipedia)

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

Wikipedia is the free, multilingual online encyclopedia operated by the non-profit Wikimedia Foundation. The platform exposes its content and structured data through several public APIs: the original MediaWiki Action API (action=query|edit|parse|upload), the MediaWiki Core REST API (page CRUD, search, transforms), the Wikimedia REST API (page summaries, mobile HTML, math, citation, reading lists, recommendations), the Wikidata Query Service SPARQL endpoint (structured knowledge graph queries), and the Wikimedia Enterprise APIs (commercial Snapshot, On-demand, Realtime). All free APIs are governed by the Wikimedia API usage guidelines: contactable User-Agent, serial requests, maxlag for bots.

**URL:** [Visit APIs.json URL](https://api.wikimedia.org/wiki/Main_Page)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

 - Open Data, Public APIs, Open Knowledge, Encyclopedia, Knowledge Graph, Open Source, Non-Profit

## Timestamps

- **Created:** 2026-05-28
- **Modified:** 2026-05-29

## Type
- **x-type:** opensource
- **x-tier:** 1 (most prominent open-knowledge API in the world; non-profit Wikimedia Foundation)
- **source:** [public-apis/public-apis](https://github.com/public-apis/public-apis) - category: Open Data

## APIs

### MediaWiki Action API
The original programmatic interface to MediaWiki, exposed at `/w/api.php` on every MediaWiki installation. Operations are dispatched via the `action=` query parameter (`query`, `parse`, `edit`, `upload`, `login`, `patrol`, ...). JSON is the recommended format. Primary write surface for Wikimedia projects.

**Human URL:** [https://www.mediawiki.org/wiki/API:Main_page](https://www.mediawiki.org/wiki/API:Main_page)
**Base URL:** `https://en.wikipedia.org/w/api.php`

#### Properties
- [Documentation](https://www.mediawiki.org/wiki/API:Main_page)
- [Sandbox](https://en.wikipedia.org/wiki/Special:ApiSandbox)
- [OpenAPI](openapi/wikipedia-mediawiki-action-api-openapi.yaml)
- [Tutorials](https://www.mediawiki.org/wiki/API:Tutorial)
- [Etiquette](https://www.mediawiki.org/wiki/API:Etiquette)

### MediaWiki Core REST API
Modern REST surface on every MediaWiki installation under `/w/rest.php/v1/`. Provides page CRUD, full-text search, file metadata, history, individual revision retrieval, revision comparison, and wikitext <-> HTML transforms.

**Human URL:** [https://www.mediawiki.org/wiki/API:REST_API](https://www.mediawiki.org/wiki/API:REST_API)
**Base URL:** `https://en.wikipedia.org/w/rest.php/v1`

#### Properties
- [Documentation](https://www.mediawiki.org/wiki/API:REST_API/Reference)
- [OpenAPI](openapi/wikipedia-mediawiki-core-rest-openapi.yaml)
- [API Portal](https://api.wikimedia.org/wiki/Core_REST_API)

### Wikimedia REST API v1
Caching-optimized REST API for high-volume, anonymous read traffic. Provides page summaries, mobile-tailored HTML, media lists, citation extraction, math rendering, content transforms, page recommendations, and reading lists. Limit clients to no more than 200 requests/s and provide a contactable User-Agent.

**Human URL:** [https://en.wikipedia.org/api/rest_v1/](https://en.wikipedia.org/api/rest_v1/)
**Base URL:** `https://en.wikipedia.org/api/rest_v1`

#### Properties
- [Documentation](https://en.wikipedia.org/api/rest_v1/)
- [OpenAPI](openapi/wikipedia-rest-v1-openapi.yaml)
- [Specification](https://en.wikipedia.org/api/rest_v1/?spec)

### Wikidata Query Service (SPARQL)
SPARQL 1.1 endpoint for Wikidata - the structured knowledge graph behind Wikipedia infoboxes, Commons captions, and 100M+ items. Single endpoint `/sparql` accepts SELECT, ASK, CONSTRUCT, DESCRIBE queries. 60s query timeout, 5 concurrent queries per IP.

**Human URL:** [https://query.wikidata.org](https://query.wikidata.org)
**Base URL:** `https://query.wikidata.org`

#### Properties
- [Documentation](https://www.wikidata.org/wiki/Wikidata:SPARQL_query_service)
- [OpenAPI](openapi/wikipedia-wikidata-sparql-openapi.yaml)
- [Query Help](https://www.wikidata.org/wiki/Wikidata:SPARQL_query_service/Wikidata_Query_Help)
- [Editor](https://query.wikidata.org)

### Wikimedia Enterprise API
Commercial, SLA-backed Wikimedia data feed run by Wikimedia LLC (the Foundation's subsidiary). Provides Snapshot (bulk twice-monthly or daily), On-demand (per-article structured contents), and Realtime (streaming updates) APIs. Free developer tier includes 5,000 on-demand requests/month and 15 snapshot/month. Paid plans add unlimited usage and realtime streams.

**Human URL:** [https://enterprise.wikimedia.com/](https://enterprise.wikimedia.com/)
**Base URL:** `https://api.enterprise.wikimedia.com`

#### Properties
- [Documentation](https://enterprise.wikimedia.com/docs/)
- [OpenAPI](openapi/wikipedia-wikimedia-enterprise-openapi.yaml)
- [Data Dictionary](https://enterprise.wikimedia.com/docs/data-dictionary/)
- [Pricing](https://enterprise.wikimedia.com/pricing/)
- [Python SDK](https://github.com/wikimedia-enterprise/wme-sdk-python)
- [Go SDK](https://github.com/wikimedia-enterprise/wme-sdk-go)
- [Postman](https://github.com/wikimedia-enterprise/postman)

## Common Properties

- [Website](https://www.wikipedia.org)
- [API Portal](https://api.wikimedia.org/wiki/Main_Page)
- [API Catalog](https://api.wikimedia.org/wiki/API_catalog)
- [Foundation](https://wikimediafoundation.org/)
- [Governance](https://meta.wikimedia.org/wiki/Wikimedia_Foundation)
- License: [CC BY-SA 4.0 (article content)](https://creativecommons.org/licenses/by-sa/4.0/)
- License: [CC0 1.0 (Wikidata)](https://creativecommons.org/publicdomain/zero/1.0/)
- [API Usage Guidelines](https://foundation.wikimedia.org/wiki/Policy:Wikimedia_Foundation_API_Usage_Guidelines)
- [GitHub: wikimedia](https://github.com/wikimedia)
- [GitHub: wikimedia-enterprise](https://github.com/wikimedia-enterprise)
- [GitHub: wmde (Wikimedia Deutschland - Wikidata)](https://github.com/wmde)
- [Gerrit (canonical source)](https://gerrit.wikimedia.org/)
- [Status](https://www.wikimediastatus.net/)
- [Bulk Database Dumps](https://dumps.wikimedia.org/)
- [EventStreams (SSE)](https://stream.wikimedia.org/v2/stream)

### MCP Servers (community)

| Server | URL |
|---|---|
| Wikipedia MCP (Python, Rudra-ravi) | https://github.com/Rudra-ravi/wikipedia-mcp |
| Wikipedia MCP (TypeScript, timjuenemann) | https://github.com/timjuenemann/wikipedia-mcp |
| Wikipedia MCP (.NET, ajayindfw) | https://github.com/ajayindfw/WikipediaMcpServer |
| Wikipedia MCP (Vercel HTTP, Ravishka17) | https://github.com/Ravishka17/Wikipedia-MCP |
| Wikipedia MCP (caching+batch, 1999AZZAR) | https://github.com/1999AZZAR/wikipedia-mcp-server |
| MediaWiki MCP (multi-wiki, shiquda) | https://github.com/shiquda/mediawiki-mcp-server |
| MediaWiki MCP (search+edit, olgasafonova) | https://github.com/olgasafonova/mediawiki-mcp-server |
| MediaWiki MCP (authoring, mbruton) | https://github.com/mbruton/mediawiki-mcp |
| Wikidata MCP (Wikimedia Deutschland) | https://github.com/wmde/WikidataMCP |
| Wikidata MCP (SPARQL, cyanheads) | https://github.com/cyanheads/wikidata-mcp-server |

## Features

| Name | Description |
|------|-------------|
| 300+ Languages | Wikipedia exists in over 300 languages; every language edition exposes the same API surfaces under `{lang}.wikipedia.org`. |
| Page Summaries | Short, plain-text extracts plus thumbnail and Wikidata QID via the `/page/summary/{title}` endpoint - widely used by mobile clients, voice assistants, and search engines. |
| Wikitext To HTML Transforms | Convert wikitext to rendered HTML (and back) on-demand via `/transform/wikitext/to/html/{title}` - the same engine that powers VisualEditor. |
| SPARQL Over A Public Knowledge Graph | Query 100M+ Wikidata items with full SPARQL 1.1 including federated SERVICE clauses, label resolution, and geo queries. |
| Real-Time Edit Stream | Server-Sent Events stream at `stream.wikimedia.org/v2/stream` emits every edit, log, and revision-create across all projects. |
| Bulk Database Dumps | Full periodic XML and SQL dumps of every Wikimedia project at `dumps.wikimedia.org` - the canonical bulk-research format. |
| Cached Anonymous Reads At 200 RPS | The REST API v1 is heavily Varnish-cached, allowing anonymous reads up to ~200 requests/s per client with a contactable User-Agent. |
| OAuth 2.0 Write Access | Modern write access (page edits, file uploads) is authenticated via OAuth 2.0 bearer tokens issued at meta.wikimedia.org. |

## Use Cases

| Name | Description |
|------|-------------|
| AI Grounding And RAG | Ground LLM responses in encyclopedic content via page summaries, full HTML, or Wikimedia Enterprise structured contents - the primary use case for the proliferating community MCP servers. |
| Voice Assistants And Smart Speakers | Siri, Alexa, and Google Assistant resolve open-domain questions through Wikipedia page summaries and Wikidata. |
| Encyclopedia Mirrors And Offline Reading | Kiwix and the Wikipedia Apps consume the REST API plus periodic dumps to ship offline-readable copies. |
| Knowledge Graph Research | Researchers query the Wikidata SPARQL endpoint to study entity relationships, citation networks, and cross-language alignment. |
| Bot Workflows | Tens of thousands of community bots use the Action API to revert vandalism, fix references, and maintain categories. |
| News Aggregation | Realtime EventStream of edits feeds breaking-news detection. |
| Linked Data Publishing | Wikidata is the open-license source-of-truth for identifiers (ISBN, ORCID, GeoNames, MusicBrainz) used across linked-data publishers. |

## Integrations

| Name | Description |
|------|-------------|
| Wikidata | Structured-data sister project; every Wikipedia page links to a Wikidata QID consumable via the SPARQL endpoint. |
| Wikimedia Commons | Shared media repository accessed via the same Action API at `commons.wikimedia.org/w/api.php`. |
| schema.org | Page summaries align with `schema.org/Article`; Wikidata properties map to schema.org types. |
| DBpedia | Community knowledge graph built by extracting structured data from Wikipedia infoboxes. |
| Google Knowledge Graph | Major downstream consumer of Wikipedia + Wikidata content for search result panels. |
| ChatGPT / Claude / Gemini | All major LLMs were pre-trained on Wikipedia and retrieve via REST API or community MCPs at inference time. |
| VisualEditor / Parsoid | WYSIWYG editor and the parser that powers the Core REST transforms. |

## Solutions

| Name | Description |
|------|-------------|
| Open-Knowledge Foundation | A non-profit, donor-funded resource serving 1.5B+ unique devices/month while keeping every byte free to redistribute under CC BY-SA / CC0. |
| Commercial High-Volume Tier | Wikimedia Enterprise (Wikimedia LLC) offers SLA-backed Snapshot, On-demand, and Realtime APIs. |

## Artifacts

Machine-readable API specifications organized by format.

### OpenAPI

- [MediaWiki Action API](openapi/wikipedia-mediawiki-action-api-openapi.yaml) - 1 dispatch path, 3 schemas
- [MediaWiki Core REST API](openapi/wikipedia-mediawiki-core-rest-openapi.yaml) - 21 paths, 12 schemas
- [Wikimedia REST API v1](openapi/wikipedia-rest-v1-openapi.yaml) - 46 paths, 21 schemas (from spec endpoint)
- [Wikidata SPARQL API](openapi/wikipedia-wikidata-sparql-openapi.yaml) - 1 dispatch path, 1 schema
- [Wikimedia Enterprise API](openapi/wikipedia-wikimedia-enterprise-openapi.yaml) - 25 paths, 46 schemas (official)

### JSON Schema

81 standalone JSON Schemas in [`json-schema/`](json-schema/), one per OpenAPI components schema across all five APIs.

### JSON Structure

81 JSON Structure documents in [`json-structure/`](json-structure/), converted from the JSON Schemas using strict typing.

### JSON-LD

- [Top-level Wikipedia context](json-ld/wikipedia-context.jsonld) - schema.org alignments for Page, Revision, User
- [MediaWiki Action API context](json-ld/wikipedia-mediawiki-action-api-context.jsonld)
- [MediaWiki Core REST API context](json-ld/wikipedia-mediawiki-core-rest-context.jsonld)
- [Wikimedia REST API v1 context](json-ld/wikipedia-rest-v1-context.jsonld)
- [Wikidata SPARQL context](json-ld/wikipedia-wikidata-sparql-context.jsonld)
- [Wikimedia Enterprise context](json-ld/wikipedia-wikimedia-enterprise-context.jsonld)

### Examples

81 example payloads in [`examples/`](examples/), one per JSON Schema, deterministically generated.

## Capabilities

Self-contained Naftiko capabilities (REST + MCP exposers, no shared imports).

| Capability | APIs Combined | Tools | Persona |
|------------|--------------|-------|---------|
| [Wikipedia Knowledge Research](capabilities/wikipedia-knowledge-research.yaml) | MediaWiki Core REST + REST v1 | 10 | AI Researcher / RAG Builder |
| [Wikipedia Content Authoring](capabilities/wikipedia-content-authoring.yaml) | MediaWiki Core REST + Action API | 8 | Editor / Bot Operator |
| [Wikidata Knowledge Graph](capabilities/wikipedia-knowledge-graph.yaml) | Wikidata SPARQL | 2 | Knowledge-Graph Researcher |
| [Wikimedia Enterprise Snapshot](capabilities/wikipedia-enterprise-snapshot.yaml) | Wikimedia Enterprise | 17 | AI Lab / Enterprise Consumer |

## Vocabulary

- [Wikipedia Vocabulary](vocabulary/wikipedia-vocabulary.yaml) - Unified taxonomy mapping 20 resources, 13 actions, 4 workflows, and 10 personas across operational (OpenAPI) and capability (Naftiko) dimensions.

## Rules

- [Wikipedia Spectral Rules](rules/wikipedia-spectral-rules.yml) - 25 rules across metadata, paths, operations, parameters, responses, schemas, security, and general-quality categories enforcing Wikipedia/MediaWiki API conventions.

## Plans

- [Plans & Pricing](plans/wikipedia-plans-pricing.yml) - Wikimedia Foundation free APIs + Wikimedia Enterprise free developer + paid plans (data egress based, contact sales).

## Rate Limits

- [Rate Limits](rate-limits/wikipedia-rate-limits.yml) - 7 limit families across REST v1 (200 rps soft cap), Action API (serial, ratelimited error code), SPARQL (60s/5 concurrent), and Wikimedia Enterprise (monthly free quotas + per-plan QPS).

## FinOps

- [FinOps](finops/wikipedia-finops.yml) - FOCUS 1.3 aligned, covers Wikimedia Enterprise commercial tier (Snapshot, On-demand, Realtime meters with data-egress pricing).

## Notes

This entry was bulk-registered as part of a public-apis catalog sweep on 2026-05-28, then fully enriched on 2026-05-29 via the API Evangelist opensource pipeline. The Wikipedia / MediaWiki API surface is the most prominent open-knowledge API in the world; this repo profiles all five major endpoints together.

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
