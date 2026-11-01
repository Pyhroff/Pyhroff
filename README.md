# Praising Y Harris Ratnam (@Pyhroff)

<div align="center">

### Backend Systems Engineer · AI Gateway & AppSec Researcher
**Indian Institute of Information Technology Kottayam (IIIT Kottayam)**  
*B.Tech Computer Science & Engineering (Specialization: Cybersecurity) · Batch of 2024–2028*  
**Target:** Summer 2027 Engineering Internships (PPO Track)

[![IIIT Kottayam · B.Tech Cybersecurity](assets/badges/badge_iiitk.svg)](https://www.iiitkottayam.ac.in)
[![4 Merged Upstream PRs](assets/badges/badge_merged_prs.svg)](#verified-merged-prs)
[![12 In Review](assets/badges/badge_active_prs.svg)](#active-review-prs)
[![4 PyPI Packages](assets/badges/badge_pypi_packages.svg)](#published-pypi-packages)  
[![72.7% Real-World Precision](assets/badges/badge_mcpaudit_precision.svg)](https://pypi.org/project/pyhroff-mcpaudit/)
[![48.1% Held-Out Recall @ 0.03% FPR](assets/badges/badge_aisec_recall.svg)](https://pypi.org/project/aisec-suite/)
[![Sub-50ms CI/CD Gate](assets/badges/badge_sub50ms_ci.svg)](https://pypi.org/project/pyhroff-mcpaudit/)

[GitHub Profile](https://github.com/Pyhroff) · [LinkedIn](https://www.linkedin.com/in/praising-harris-8a3320330) · [Security Advisories](https://github.com/Pyhroff/security-advisories) · [Email Contact](mailto:praisingharris@gmail.com) · [Pinned Repos Guide](PINNED_REPOSITORIES.md)

</div>

---

## 🧭 Executive Overview

I am an engineering undergraduate specializing in **high-throughput backend systems**, **AST compiler internals**, and **AI infrastructure security**. My core philosophy is grounded in defense-in-depth and empirical verification: treating the model layer as inherently untrusted, enforcing strict host-level invariants, and optimizing data processing pipelines at the storage engine level.

- **Upstream Open-Source Contributions:** **4 merged production PRs** in foundational data/AI runtimes ([SQLGlot](https://github.com/tobymao/sqlglot), [LiteLLM](https://github.com/BerriAI/litellm), [SQLFluff](https://github.com/sqlfluff/sqlfluff)) and **12 active PRs** under maintainer review across [LiteLLM](https://github.com/BerriAI/litellm), [CrewAI](https://github.com/crewAIInc/crewAI), [FastMCP](https://github.com/PrefectHQ/fastmcp), and [Graphene](https://github.com/graphql-python/graphene).
- **Published Security Packages on PyPI:** Author of 4 production packages ([`pyhroff-mcpaudit`](https://pypi.org/project/pyhroff-mcpaudit/), [`aisec-suite`](https://pypi.org/project/aisec-suite/), [`memsentry`](https://pypi.org/project/memsentry/), [`pyhroff-ragsentry`](https://pypi.org/project/pyhroff-ragsentry/)).
- **High-Throughput Storage & Concurrency:** Designed streaming ingestion pipelines processing **10,000+ msg/s** ($O(1)$ RAM streaming JSON via `ijson`, unlogged PostgreSQL staging tables, binary `COPY`, GIN `jsonb_path_ops`) and implemented a 5-node Raft consensus engine with leader lease fencing.
- **Empirical Rigor:** Grounded all security evaluations in reproducible, real-world benchmarks: elevated `pyhroff-mcpaudit` from an empirical **37.5% baseline** to **72.7% precision** across 135 public repositories using C-level token filters and AST reachability analysis.

---

## 🚀 Verified Upstream Contributions Matrix (16 Total)

Every pull request listed below represents genuine upstream engineering work submitted to production open-source codebases, verified via the GitHub CLI.

<a id="verified-merged-prs"></a>
### ✅ Verified Upstream Production PRs (4 Merged)

| Project | PR & Status | Component & Scope | Root Cause & Concrete Architectural Fix | Live Verification Command |
|---|:---:|---|---|---|
| **[tobymao/sqlglot](https://github.com/tobymao/sqlglot)** | [PR #8780](https://github.com/tobymao/sqlglot/pull/8780)<br>`MERGED` | `sqlglot/parser.py`<br>(`_replace_lambda`) | **AST parent pointer corruption:** Snowflake typed lambdas bound a single uncopied `exp.DataType` AST node across multiple `exp.Cast` nodes, violating the unique parent invariant (`child.parent = self`) and breaking in-place tree transforms (`expression.transform(copy=False)`). Fixed by injecting `typ.copy()` for every cast. | `gh pr view 8780 --repo tobymao/sqlglot --json state,mergedAt,title` |
| **[BerriAI/litellm](https://github.com/BerriAI/litellm)** | [PR #47091](https://github.com/BerriAI/litellm/pull/47091)<br>`MERGED` | `litellm/llms/cohere`<br>(`transformation.py`) | **Schema validation 400 rejection:** Cohere API requires `stop_sequences` as a `List[str]`. Single-string inputs like `stop="END"` were passed unparsed, causing API rejections. Normalized parameter into `[stop] if isinstance(stop, str) else stop`. | `gh pr view 47091 --repo BerriAI/litellm --json state,mergedAt,title` |
| **[sqlfluff/sqlfluff](https://github.com/sqlfluff/sqlfluff)** | [PR #8901](https://github.com/sqlfluff/sqlfluff/pull/8901)<br>`MERGED` | `sqlfluff/dialects`<br>(`dialect_doris.py`) | **Grammar hierarchy false positive:** Doris dialect inherited `FlushStatementSegment` from base MySQL grammar despite Apache Doris not supporting `FLUSH TABLES`, triggering erroneous syntax errors in CI. Excised segment from grammar tree. | `gh pr view 8901 --repo sqlfluff/sqlfluff --json state,mergedAt,title` |
| **[sqlfluff/sqlfluff](https://github.com/sqlfluff/sqlfluff)** | [PR #8902](https://github.com/sqlfluff/sqlfluff/pull/8902)<br>`MERGED` | `sqlfluff/dialects`<br>(`dialect_starrocks.py`) | **Grammar hierarchy false positive:** StarRocks dialect inherited `FlushStatementSegment` from base MySQL grammar despite StarRocks not supporting `FLUSH TABLES`. Excised segment from grammar tree. | `gh pr view 8902 --repo sqlfluff/sqlfluff --json state,mergedAt,title` |

---

<a id="active-review-prs"></a>
### ⏳ Active Upstream Contributions Under Review (12 PRs)

| Project | PR & Status | Component & Scope | Root Cause & Technical Resolution | Live Verification Command |
|---|:---:|---|---|---|
| **[BerriAI/litellm](https://github.com/BerriAI/litellm)** | [PR #47105](https://github.com/BerriAI/litellm/pull/47105)<br>`IN REVIEW` | `litellm/proxy/auth`<br>(`auth_checks.py`) | **BOLA Access Control Bypass (CVSS 7.5, PYHROFF-ADV-2026-001):** When a key had `access_group_ids` but `models: []`, authorization logic treated empty models list as a wildcard, granting unauthorized access to all backend models. Enforced access group scoping on empty lists. | `gh pr view 47105 --repo BerriAI/litellm --json state,title` |
| **[BerriAI/litellm](https://github.com/BerriAI/litellm)** | [PR #47106](https://github.com/BerriAI/litellm/pull/47106)<br>`IN REVIEW` | `proxy/management_helpers`<br>(`object_update_helpers.py`) | **Duplicate kwarg crash:** Passing `budget_id` both directly and in kwargs triggered fatal `TypeError` during entity updates. Stripped `budget_id` from entity settings dictionary. | `gh pr view 47106 --repo BerriAI/litellm --json state,title` |
| **[BerriAI/litellm](https://github.com/BerriAI/litellm)** | [PR #47107](https://github.com/BerriAI/litellm/pull/47107)<br>`IN REVIEW` | `litellm/proxy/auth`<br>(`auth_checks.py`) | **Permission evaluation failure:** Access group checks evaluated model names or model IDs in isolation, incorrectly blocking valid virtual keys. Applied dual-evaluation with deduplication. | `gh pr view 47107 --repo BerriAI/litellm --json state,title` |
| **[BerriAI/litellm](https://github.com/BerriAI/litellm)** | [PR #47311](https://github.com/BerriAI/litellm/pull/47311)<br>`IN REVIEW` | `proxy/key_management`<br>(`key_management_endpoints.py`) | **Unauthorized budget tier manipulation:** Missing admin-level authorization checks on key budget updates allowed privilege escalation. Enforced caller role verification. | `gh pr view 47311 --repo BerriAI/litellm --json state,title` |
| **[BerriAI/litellm](https://github.com/BerriAI/litellm)** | [PR #47312](https://github.com/BerriAI/litellm/pull/47312)<br>`IN REVIEW` | `litellm/proxy`<br>(`mcp_endpoints.py`) | **Configuration data leak:** `/v1/mcp/access_groups` returned global MCP server configurations to unauthorized virtual keys. Scoped output strictly to caller-authorized servers. | `gh pr view 47312 --repo BerriAI/litellm --json state,title` |
| **[crewAIInc/crewAI](https://github.com/crewAIInc/crewAI)** | [PR #8240](https://github.com/crewAIInc/crewAI/pull/8240)<br>`IN REVIEW` | `crewai/utilities/mcp`<br>(`mcp_client.py`) | **MCP tool truncation:** Server tool/prompt responses were truncated after page 1 due to missing cursor iteration. Implemented full `nextCursor` / `next_cursor` pagination traversal. | `gh pr view 8240 --repo crewAIInc/crewAI --json state,title` |
| **[crewAIInc/crewAI](https://github.com/crewAIInc/crewAI)** | [PR #8242](https://github.com/crewAIInc/crewAI/pull/8242)<br>`IN REVIEW` | `crewai/task.py`<br>(`Task.execute`) | **Task context loss:** Upstream dependent task execution context was wiped during guardrail retry evaluation loops. Wrapped retry logic with context preservation. | `gh pr view 8242 --repo crewAIInc/crewAI --json state,title` |
| **[crewAIInc/crewAI](https://github.com/crewAIInc/crewAI)** | [PR #8243](https://github.com/crewAIInc/crewAI/pull/8243)<br>`IN REVIEW` | `crewai/utilities`<br>(`logger.py`) | **Logger level pollution:** Errors during execution permanently mutated logger hierarchy levels away from configured settings. Restored original levels and preserved `NOTSET` inheritance. | `gh pr view 8243 --repo crewAIInc/crewAI --json state,title` |
| **[crewAIInc/crewAI](https://github.com/crewAIInc/crewAI)** | [PR #8244](https://github.com/crewAIInc/crewAI/pull/8244)<br>`IN REVIEW` | `crewai/utilities`<br>(`redis.py`) | **Connection failure on encoded passwords:** Special characters in Redis URLs (`%40`, `%23`) caused authentication crashes. Added URL percent-decoding in `_parse_redis_url`. | `gh pr view 8244 --repo crewAIInc/crewAI --json state,title` |
| **[crewAIInc/crewAI](https://github.com/crewAIInc/crewAI)** | [PR #8245](https://github.com/crewAIInc/crewAI/pull/8245)<br>`IN REVIEW` | `crewai/tools`<br>(`tool_output.py`) | **Windows line ending artifact bug:** Raw splitlines failed on Windows `\r\n` boundaries, corrupting line counting. Replaced with universal newlines normalization. | `gh pr view 8245 --repo crewAIInc/crewAI --json state,title` |
| **[PrefectHQ/fastmcp](https://github.com/PrefectHQ/fastmcp)** | [PR #6063](https://github.com/PrefectHQ/fastmcp/pull/6063)<br>`IN REVIEW` | `fastmcp/experimental`<br>(`code_mode.py`) | **Async callback starvation (CVSS 5.3, PYHROFF-ADV-2026-002):** Monty sandbox bytecode execution decoupled host-side asynchronous callbacks, allowing long-running host tasks to bypass timeout. Enforced global wall-clock timeout wrapper and callback dispatch limit. | `gh pr view 6063 --repo PrefectHQ/fastmcp --json state,title` |
| **[graphql-python/graphene](https://github.com/graphql-python/graphene)** | [PR #1610](https://github.com/graphql-python/graphene/pull/1610)<br>`IN REVIEW` | `graphene/relay`<br>(`connection.py`) | **Circular schema import crash (#1566):** Definition-time `issubclass(node, ...)` crashed when `node = lambda: MyObjectType` was supplied. Replaced with `callable(node) and not isclass(node)` to support lazy evaluation thunks. | `gh pr view 1610 --repo graphql-python/graphene --json state,title` |

---

<a id="published-pypi-packages"></a>
## 📦 Published PyPI Security Packages

All packages below are actively published to the Python Package Index ([PyPI](https://pypi.org/user/Pyhroff/)) and can be installed via `pip`:

| Package | Version | Install Command | Primary Technical Role | Verified Empirical Metric | Repository Link |
|---|:---:|---|---|---|:---:|
| **`pyhroff-mcpaudit`** | `v0.8.0` | `pip install pyhroff-mcpaudit==0.8.0` | Model Context Protocol AST Static Security Analyzer | **72.7% precision** across 135 repos · Sub-50ms CI/CD gate · 94% file pruning via token-hash index | [GitHub](https://github.com/Pyhroff/pyhroff-mcpaudit) |
| **`aisec-suite`** | `v0.3.0` | `pip install aisec-suite==0.3.0` | Empirical Security Evaluation Harness for Agentic Workflows | **48.1% held-out recall @ 0.03% FPR** across 3,974 tools · Z3 SMT policy reachability (0 false refutations on 120 findings) | [GitHub](https://github.com/Pyhroff/aisec-suite) |
| **`memsentry`** | `v1.2.0` | `pip install memsentry==1.2.0` | Runtime Context Protection & Memory Integrity Guardrail | Detects cross-session state corruption and memory poison overwrites across vector and key-value stores | [GitHub](https://github.com/Pyhroff/memsentry) |
| **`pyhroff-ragsentry`** | `v1.1.0` | `pip install pyhroff-ragsentry==1.1.0` | RAG Context Injection Sanitizer & Chunk Boundary Guard | Sub-millisecond chunk boundary validation and embedding anomaly scoring for retrieval pipelines | [GitHub](https://github.com/Pyhroff/pyhroff-ragsentry) |

---

## 🏗️ Core Technical Pillars

### 1. High-Throughput Backend & Storage Engines
- **Streaming JSON Ingestion ($O(1)$ RAM):** Designed high-volume data ingestion pipelines for vulnerability telemetry (e.g. 50,000+ SARIF records) using Python's `ijson` iterative parser, preventing Out-Of-Memory (OOM) crashes and maintaining flat memory consumption regardless of payload size.
- **PostgreSQL Internals & MVCC:** Utilized unlogged staging tables, binary `COPY` protocol, and deterministic conflict resolution (`ON CONFLICT (asset_id, rule_hash) DO UPDATE`) to eliminate deadlock conditions under concurrent writes.
- **Database Indexing & Query Tuning:** Optimized B+ Tree index design (fan-out calculations $\approx 512$, height 3 indexing 134M keys), GIN indexing on semi-structured JSONB attributes (`jsonb_path_ops`), and transaction-level connection pooling via PgBouncer (supporting 10,000 client connections over 50 backend workers).

### 2. AI Gateway & Application Security
- **AST Static Analysis:** Engineered single-pass AST visitors with 64-bit token-hash inverted indices to detect command execution, unvalidated file system operations, and dangerous serialization in MCP server tools prior to invocation.
- **Authorization & Reverse Proxy Hardening:** Identified and remediated Broken Object-Level Authorization (BOLA / CWE-863) vulnerabilities in AI reverse proxies (e.g. LiteLLM Proxy), ensuring access groups enforce strict model authorization even when model configuration arrays are empty.
- **Sandbox Boundary Defense:** Audited WebAssembly and Python bytecode sandboxes (Monty sandbox), establishing wall-clock watchdog timers and decoupled callback limits to prevent host resource starvation attacks.

### 3. Distributed Systems, Concurrency & State Machines
- **Distributed Consensus (Raft):** Built a 5-node Raft consensus engine (`Kronos-KV`) featuring leader lease convergence, randomized election timeouts ($150\text{--}300\text{ms}$), and monotonic fencing tokens to protect against split-brain scenarios and network partitions.
- **Thread-Safe Low-Level Design:** Implemented lock-free and thread-safe data structures in Python and Go, including $O(1)$ LRU caches with read-write mutexes, Token Bucket rate limiters with token leak prevention, and Kleppmann fencing tokens for distributed locks over Redis.

---

## 🔬 Empirical Integrity & Transparency Standard

In an industry often crowded with unverified marketing numbers, I adhere to a strict empirical standard:

1. **Honest Baseline Disclosure:** When auditing `pyhroff-mcpaudit` v0.6 across 90 public Model Context Protocol repositories, I disclosed an initial **37.5% baseline precision** (95% Wilson CI: 24–53%) caused by keyword regex false alarms. Rather than masking the data, this benchmark served as the engineering specification for v0.8, which achieved **72.7% precision** across 135 repositories by implementing C-level token filters and AST reachability analysis.
2. **Realistic Benchmark Grounding:** In `aisec-suite` v0.3.0, the tool-poisoning detection benchmark evaluates 3,974 real-world tool descriptions, establishing **48.1% held-out recall at a 0.03% false-positive rate** (1 false positive in 3,974 evaluations). Policy reachability verification using Microsoft's Z3 SMT solver confirmed zero false refutations across 120 labelled security findings.
3. **Verifiable Proof of Work:** I do not make claims that cannot be independently reproduced. All cited PRs are live on GitHub, all published packages are live on PyPI, and reproducible benchmark suites are provided with zero external network dependencies.

---

## 🛠️ Verification & Interactive Portfolio

- **Pinned Repositories Setup Guide:** Inspect [`PINNED_REPOSITORIES.md`](PINNED_REPOSITORIES.md) for full metadata configurations and tag taxonomies.
- **Interactive Showcase Web Application:** Open `showcase/index.html` in any browser to explore dynamic PR filtering, live AST precision sliders, and embedded PostgreSQL/Raft visualizers.
- **Technical Architecture Reports:** In-depth engineering write-ups covering AST compiler theory, BOLA security advisories, and streaming ingestion are available in `showcase/reports/`.
- **Reproducible Benchmark Script:** Run `python showcase/benchmarks/reproduce_benchmarks.py` to regenerate all Wilson confidence intervals and empirical telemetry tables.
