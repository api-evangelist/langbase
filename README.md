# Langbase (langbase)

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

Langbase is a serverless AI developer platform for building, deploying, and scaling AI agents and applications. Its composable primitives - Pipes (agents), Memory (managed RAG), Threads, Agent (one API over 100+ LLMs), Tools, Parser, Chunker, and Embed - are exposed through a single Bearer-authenticated REST API at api.langbase.com, with Server-Sent Events (SSE) streaming for generative endpoints.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/langbase/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/langbase/refs/heads/main/apis.yml)

## Tags

- AI
- Agents
- RAG
- LLM
- Serverless

## Timestamps

- **Created:** 2026-07-01
- **Modified:** 2026-07-01

## APIs

### Langbase Pipes API

Run, create, update, and list Pipes - composable, deployable AI agents with a system prompt, model, tools, variables, and memory. POST /v1/pipes/run executes a Pipe over a message array and streams token deltas as Server-Sent Events when stream is true.

- **Human URL:** [https://langbase.com/docs/api-reference/pipe](https://langbase.com/docs/api-reference/pipe)
- **Base URL:** `https://api.langbase.com/v1`

#### Tags

- Pipes
- Agents
- Completions

#### Properties

- [Documentation](https://langbase.com/docs/pipe)
- [API Reference](https://langbase.com/docs/api-reference/pipe)
- [OpenAPI](openapi/langbase-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/langbase.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/langbase.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Langbase Agent API

A single liquid AI mesh endpoint (POST /v1/agent/run) that runs a prompt against 100+ LLMs from all top providers using a provider:model_id string, with tools, generation controls, and SSE streaming. Bring-your-own LLM keys are supported via the LB-LLM-Key header.

- **Human URL:** [https://langbase.com/docs/api-reference/agent](https://langbase.com/docs/api-reference/agent)
- **Base URL:** `https://api.langbase.com/v1`

#### Tags

- Agent
- LLM
- Multi-Provider

#### Properties

- [Documentation](https://langbase.com/docs/agent)
- [API Reference](https://langbase.com/docs/api-reference/agent)
- [OpenAPI](openapi/langbase-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/langbase.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/langbase.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Langbase Memory API

Managed, serverless RAG. Create and list memory stores, upload and manage documents, and retrieve semantically similar chunks (POST /v1/memory/retrieve) with a topK control and metadata filters, without running your own vector database or embedding pipeline.

- **Human URL:** [https://langbase.com/docs/api-reference/memory](https://langbase.com/docs/api-reference/memory)
- **Base URL:** `https://api.langbase.com/v1`

#### Tags

- Memory
- RAG
- Vector Store

#### Properties

- [Documentation](https://langbase.com/docs/memory)
- [API Reference](https://langbase.com/docs/api-reference/memory)
- [OpenAPI](openapi/langbase-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/langbase.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/langbase.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Langbase Threads API

Persist and manage conversation state. Create, get, update, and delete threads, and append or list messages, so multi-turn agent conversations keep their history server-side and can be resumed via a thread identifier.

- **Human URL:** [https://langbase.com/docs/api-reference/threads](https://langbase.com/docs/api-reference/threads)
- **Base URL:** `https://api.langbase.com/v1`

#### Tags

- Threads
- Conversation
- State

#### Properties

- [Documentation](https://langbase.com/docs/threads)
- [API Reference](https://langbase.com/docs/api-reference/threads)
- [OpenAPI](openapi/langbase-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/langbase.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/langbase.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Langbase Tools API

Managed agent tools. POST /v1/tools/web-search runs a live web search (via providers such as Exa) returning URLs and extracted content, and POST /v1/tools/crawl fetches and extracts content from one or more web pages for agents to ground on.

- **Human URL:** [https://langbase.com/docs/api-reference/tools](https://langbase.com/docs/api-reference/tools)
- **Base URL:** `https://api.langbase.com/v1`

#### Tags

- Tools
- Web Search
- Crawl

#### Properties

- [Documentation](https://langbase.com/docs/tools)
- [API Reference](https://langbase.com/docs/api-reference/tools)
- [OpenAPI](openapi/langbase-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/langbase.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/langbase.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Langbase Parser API

Extract clean text from uploaded documents (PDF, CSV, XLSX, XLS, and more, up to 10 MB) via a multipart POST /v1/parser, as the ingestion front door for RAG and content pipelines.

- **Human URL:** [https://langbase.com/docs/api-reference/parser](https://langbase.com/docs/api-reference/parser)
- **Base URL:** `https://api.langbase.com/v1`

#### Tags

- Parser
- Documents
- Extraction

#### Properties

- [Documentation](https://langbase.com/docs/parser)
- [API Reference](https://langbase.com/docs/api-reference/parser)
- [OpenAPI](openapi/langbase-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/langbase.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/langbase.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Langbase Chunker API

Split large text into overlapping, retrieval-ready chunks (POST /v1/chunker) with configurable chunkMaxLength and chunkOverlap, for building RAG and search indexes.

- **Human URL:** [https://langbase.com/docs/api-reference/chunker](https://langbase.com/docs/api-reference/chunker)
- **Base URL:** `https://api.langbase.com/v1`

#### Tags

- Chunker
- RAG
- Preprocessing

#### Properties

- [Documentation](https://langbase.com/docs/chunker)
- [API Reference](https://langbase.com/docs/api-reference/chunker)
- [OpenAPI](openapi/langbase-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/langbase.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/langbase.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Langbase Embed API

Generate embedding vectors for up to 100 text chunks per request (POST /v1/embed) using OpenAI, Cohere, or Google embedding models, defaulting to openai:text-embedding-3-large.

- **Human URL:** [https://langbase.com/docs/api-reference/embed](https://langbase.com/docs/api-reference/embed)
- **Base URL:** `https://api.langbase.com/v1`

#### Tags

- Embeddings
- Vectors
- RAG

#### Properties

- [Documentation](https://langbase.com/docs/embed)
- [API Reference](https://langbase.com/docs/api-reference/embed)
- [OpenAPI](openapi/langbase-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/langbase.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/langbase.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Langbase Workflows API

Durable, step-based orchestration for composing agents, memory, and tools into multi-step AI workflows with retries and timeouts. Workflows compose the underlying Agent, Pipes, Memory, and Tools API calls into a single reliable execution.

- **Human URL:** [https://langbase.com/docs/workflows](https://langbase.com/docs/workflows)
- **Base URL:** `https://api.langbase.com/v1`

#### Tags

- Workflows
- Orchestration
- Agents

#### Properties

- [Documentation](https://langbase.com/docs/workflows)
- [OpenAPI](openapi/langbase-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/langbase.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/langbase.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/LangbaseInc)
- [LinkedIn](https://www.linkedin.com/company/langbase)
- [Website](https://langbase.com/)
- [Documentation](https://langbase.com/docs)
- [Plans](plans/langbase-plans-pricing.yml)
- [Rate Limits](rate-limits/langbase-rate-limits.yml)
- [Fin Ops](finops/langbase-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
