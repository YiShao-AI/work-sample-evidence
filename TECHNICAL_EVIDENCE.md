# AI Business Analyst technical evidence index

This index maps the two work samples to inspectable requirements, workflows,
data decisions, implementation, validation, and delivery controls. It is the
technical companion to the concise recruiter packet.

## Evidence classes

| Class | What it means |
|---|---|
| Professional operating evidence | Firsthand workflow observations, stakeholder feedback, adoption, and operating changes from the deployed work. |
| Public implementation evidence | Repository source, testable rules, fictional or non-confidential data, automated checks, and live/static demonstrations. |
| Modeled planning evidence | Explicit assumptions and sensitivity analysis used for capacity, cost, and outcome planning. |

Keeping these classes distinct makes it possible to evaluate business impact,
technical behavior, and planning assumptions without treating them as the same
kind of proof.

## Full-lifecycle evidence map

| Capability | RAG knowledge system | ATM prospecting operations |
|---|---|---|
| Problem framing and stakeholder discovery | [Discovery synthesis and operating signals](https://github.com/YiShao-AI/contract-review-rag/blob/main/DELIVERY_AND_READINESS.md#discovery-synthesis) translate repeated questions, source constraints, and verification needs into system requirements. | [Discovery synthesis](https://github.com/YiShao-AI/ATM-Map-Public/blob/main/DELIVERY_AND_READINESS.md#discovery-synthesis) connects owner, BD, mailing, review, and CRM needs to derived requirements. |
| Current and future workflow | [Historical, system, and knowledge-pipeline flows](https://github.com/YiShao-AI/contract-review-rag/blob/main/REQUIREMENTS_AND_VALIDATION.md#current-and-target-workflow) show the decision and evidence path. | [Before/after workflow](https://github.com/YiShao-AI/ATM-Map-Public/blob/main/BUSINESS_CASE.md#before-and-after) and the [end-to-end operating flow](https://github.com/YiShao-AI/ATM-Map-Public/blob/main/DATA_HUB.md#end-to-end-workflow) show decisions, handoffs, and exceptions. |
| Requirements and user stories | [Functional, non-functional, and governance requirements](https://github.com/YiShao-AI/contract-review-rag/blob/main/REQUIREMENTS_AND_VALIDATION.md#functional-requirements) plus [user stories](https://github.com/YiShao-AI/contract-review-rag/blob/main/DELIVERY_AND_READINESS.md#user-stories-and-acceptance). | [Requirements that shaped the product](https://github.com/YiShao-AI/ATM-Map-Public/blob/main/BUSINESS_CASE.md#requirements-that-shaped-the-product) plus [user stories and acceptance conditions](https://github.com/YiShao-AI/ATM-Map-Public/blob/main/DELIVERY_AND_READINESS.md#user-stories-and-acceptance). |
| Business rules and decision logic | Source-grounding, abstention, deletion, precise citation, processing-boundary, and accessibility rules are traceable to implementation. | Unknown-state preservation, conservative deduplication, manual approval, monotonic funnel, revisit, campaign, and do-not-contact rules are explicit. |
| Data discovery and readiness | [Data inventory and ownership](https://github.com/YiShao-AI/contract-review-rag/blob/main/REQUIREMENTS_AND_VALIDATION.md#data-inventory-and-ownership) plus [format, OCR, metadata, index, and label readiness gates](https://github.com/YiShao-AI/contract-review-rag/blob/main/DELIVERY_AND_READINESS.md#data-readiness-gates). | [Entities, ownership, lineage, and integrity controls](https://github.com/YiShao-AI/ATM-Map-Public/blob/main/DATA_ARCHITECTURE.md) distinguish provider evidence, human decisions, historical identity, campaign state, and CRM ownership. |
| Business value and KPIs | Professional support evidence focuses on lookup access, shared knowledge, source verification, and operating coverage; technical measures isolate retrieval and citation behavior. | [Operating results and KPI plan](https://github.com/YiShao-AI/ATM-Map-Public/blob/main/BUSINESS_CASE.md#operating-results) connect candidate capacity to campaign conversion, cycle time, and total acquisition cost. |
| Pilot validation and UAT | [Acceptance scenarios with evidence class](https://github.com/YiShao-AI/contract-review-rag/blob/main/REQUIREMENTS_AND_VALIDATION.md#acceptance-scenarios-and-evidence-status), a [recorded validation run](https://github.com/YiShao-AI/contract-review-rag/blob/main/VALIDATION_RESULTS.md), a [fictional-corpus retrieval evaluation](https://github.com/YiShao-AI/contract-review-rag/tree/main/eval), and a [synthetic exact-locator concurrency/recovery run](https://github.com/YiShao-AI/contract-review-rag/blob/main/benchmarking/evidence/RELIABILITY_RUN_20260904.md). | [Operational acceptance criteria](https://github.com/YiShao-AI/ATM-Map-Public/blob/main/DATA_HUB.md#operational-acceptance-criteria), an [82-test active-service run](https://github.com/YiShao-AI/ATM-Map-Public/blob/main/VALIDATION_RESULTS.md), a Chromium Search History/formula-safe export flow, and a [bounded 1,856-Place-ID market run](https://github.com/YiShao-AI/ATM-Map-Public/blob/main/benchmarking/evidence/MARKET_RUN_20260904.md). |
| Risks, dependencies, and decisions | [Decision, ownership, risk, and release-gate record](https://github.com/YiShao-AI/contract-review-rag/blob/main/DELIVERY_AND_READINESS.md). | [Decision, ownership, risk, and release-gate record](https://github.com/YiShao-AI/ATM-Map-Public/blob/main/DELIVERY_AND_READINESS.md) plus a [protected deployment runbook](https://github.com/YiShao-AI/ATM-Map-Public/blob/main/DEPLOY.md). |
| Executive-ready communication | Repository README and requirements summary translate retrieval architecture into the business decision it supports. | [Business case](https://github.com/YiShao-AI/ATM-Map-Public/blob/main/BUSINESS_CASE.md) summarizes the operating problem, workflow change, adoption, value, and next measurement layer. |

## Applied technical fluency

| Area | Inspectable evidence |
|---|---|
| LLM document intelligence | Mixed-format ingestion, OCR, clause-aware chunking, vector embeddings, FTS5 keyword search, reciprocal-rank fusion, structured extraction, citations, abstention, focused evidence spans, and local/hosted provider configuration in the [RAG repository](https://github.com/YiShao-AI/contract-review-rag). |
| Evaluation design | Locked corpus and labels, separate document/passage/citation checks, per-question results, privacy regression, and explicit separation of retrieval from answer correctness under [`eval/`](https://github.com/YiShao-AI/contract-review-rag/tree/main/eval) and [`tests/`](https://github.com/YiShao-AI/contract-review-rag/tree/main/tests). |
| Data modeling and SQL | SQLite transactional entities, FTS5 indexes, append-only decisions, audit events, campaign membership, durable search runs and checkpoints, ownership rules, migrations, and incremental API boundaries in the [ATM data architecture](https://github.com/YiShao-AI/ATM-Map-Public/blob/main/DATA_ARCHITECTURE.md) and source. |
| API and integration design | Metered map/search APIs, caching, quota controls, authentication, CRM vocabulary adapter, campaign transitions, and protected deployment in the [ATM repository](https://github.com/YiShao-AI/ATM-Map-Public). |
| Reliability and operations | Thread-local concurrent retrieval, serialized writes, request correlation, fail-closed readiness, atomic index persistence, corrupt-index quarantine, deletion propagation, safe provider-outage behavior, and protected single-host runbooks are exercised in a [synthetic exact-locator concurrency and recovery check](https://github.com/YiShao-AI/contract-review-rag/blob/main/benchmarking/evidence/RELIABILITY_RUN_20260904.md). Durable ATM search checkpoints preserve completed and interrupted work for inspection and replay. |
| CI and security verification | Both repositories include commit-pinned GitHub Actions for unit and browser checks, CodeQL, Gitleaks, and Trivy. The RAG workflow also rebuilds its release container and reruns the 1,000-search reliability gate; current local scans report no secrets or HIGH/CRITICAL configuration findings and no HIGH/CRITICAL dependency findings requiring an available fix (`ignore-unfixed: true`). |
| Spreadsheet analysis | [ATM prospecting cost model](https://yishao-ai.github.io/work-sample-evidence/Yi-Shao-ATM-Prospecting-Cost-Model.xlsx) calibrates the base case to the completed 21-area run and includes source-linked inputs, formulas, sensitivity analysis, native PivotTable and chart support, 13 formula-driven controls plus two recorded-run checks, run-level validation rows, and closed-campaign outcome fields. |

## Primary validation results

| Project | Current public technical evidence |
|---|---|
| RAG | 22 / 22 expected documents retrieved; 20 / 22 expected passages retrieved; 8 / 8 citation annotations; 31 focused checks across citation precision, privacy, URL and upload boundaries, prompt separation, telemetry, concurrent retrieval, safe provider failure, deletion, readiness, and index recovery; plus two browser checks covering keyboard source review and automated accessibility. A synthetic exact-locator check over 500 documents and 2,000 chunks completed 1,000 / 1,000 expected-document top-1 searches through 25 workers with zero exceptions and 46.12 ms p95 local storage/retrieval latency, then passed restart, deletion, corruption quarantine, and restore checks. This isolates concurrency and recovery mechanics; it is not a representative retrieval-quality or production-capacity measure. Inputs, hashes, settings, runners, and machine-readable results are committed. |
| ATM | 79 stopped-service and 82 active-service automated checks across search geometry, price and spend accounting, cache controls, qualification, co-location, historical-location resolution, durable search history and recovery, decision history, manual approval, campaigns, funnel integrity, revisit logic, CRM boundaries, and HTTP access boundaries. A Chromium flow validates History, reopen, direct link, formula-safe CSV, filtering, terminal states, and a zero-call cached rerun. The bounded market run completed 21 / 21 started areas at application level, matched 224 application-ledger calls to an operator-recorded 224-request Cloud console count, reduced 1,961 observations to 1,856 unique returned primary Place IDs, and reproduced four fixed controls from cache with zero new calls. The same aggregate console view showed eight unclassified error events, so it does not independently establish upstream success for every request. |

## Evidence boundary

The public repositories contain fictional or non-confidential implementation
evidence. They exclude employer source code, active operational records,
credentials, access logs, and proprietary scoring criteria. The 33 historical
ATM serial numbers and decommissioned addresses are retained as the lineage
anchors for the existing-location layer.
