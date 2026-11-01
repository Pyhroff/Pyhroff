# GitHub Profile Pinned Repositories Configuration Guide

**Candidate:** Praising Y Harris Ratnam ([@Pyhroff](https://github.com/Pyhroff))  
**Target:** Summer 2027 Engineering Internships (PPO Track)  
**Profile Location:** `https://github.com/Pyhroff`  
**Reference Specification:** `PROJECT.md` (Milestone 2) & `RESUME_HARDENING_PLAYBOOK.md`

---

## 1. Executive Strategy & Pin Layout

Technical recruiters, hiring managers, and senior systems interviewers spend an average of **60 to 90 seconds** evaluating a candidate's GitHub profile. The pinned repositories grid represents prime visual real estate. It must immediately communicate two synergistic capabilities:

1. **Pure Backend / Systems SDE Spine:** High-throughput streaming data ingestion, AST compiler optimization, lockless/deterministic concurrency, and distributed consensus.
2. **AI Gateway & Application Security Differentiator:** Production-grade Model Context Protocol (MCP) AST static analysis, runtime agent memory guardrails, and empirical security evaluation.

### Top 6 Curated Repository Grid

| Slot | Repository | Category | Core Proof-of-Work Metric |
|:---:|---|---|---|
| **1** | [`pyhroff-mcpaudit`](https://github.com/Pyhroff/pyhroff-mcpaudit) | Core Security Tooling (PyPI) | **72.7% precision** across 135 repos · **Sub-50ms CI/CD gate** |
| **2** | [`aisec-suite`](https://github.com/Pyhroff/aisec-suite) | Security Evaluation Harness (PyPI) | **48.1% held-out recall @ 0.03% FPR** on 3,974 tools · Z3 SMT solver |
| **3** | [`memsentry`](https://github.com/Pyhroff/memsentry) | Runtime Agent Memory Guard (PyPI) | Cross-session memory poison isolation & state-mutation detection |
| **4** | [`pyhroff-ragsentry`](https://github.com/Pyhroff/pyhroff-ragsentry) | RAG Security Gateway (PyPI) | Chunk boundary sanitizer & indirect prompt injection firewall |
| **5** | [`upstream-contributions`](https://github.com/Pyhroff/upstream-contributions) | Production OSS Contributions | **4 Merged Upstream PRs** (SQLGlot, LiteLLM, SQLFluff) + **12 in Review** |
| **6** | [`systems-showcase`](https://github.com/Pyhroff/systems-showcase) | High-Throughput Systems | **10k msg/s** streaming ingestion ($O(1)$ RAM `ijson`) + Raft consensus |

---

## 2. GitHub UI Setup Instructions

To configure these exact 6 repositories on the candidate's live GitHub profile:

1. Log into GitHub as **`@Pyhroff`** and navigate to your user profile: `https://github.com/Pyhroff`.
2. Locate the **"Pinned"** section below the profile README.
3. Click the **"Customize your pins"** link (or **"Edit pins"** button in the upper-right corner of the pinned grid).
4. In the modal dialog:
   - Uncheck any outdated or experimental repositories.
   - Search for and check the 6 repositories listed below:
     - [x] `pyhroff-mcpaudit`
     - [x] `aisec-suite`
     - [x] `memsentry`
     - [x] `pyhroff-ragsentry`
     - [x] `upstream-contributions`
     - [x] `systems-showcase`
5. Drag and reorder the cards to match the exact 1–6 slot sequence specified in Section 3.
6. Click **"Save pins"**.

---

## 3. Detailed Repository Specifications

For each pinned repository, configure the exact GitHub metadata (Description, Website URL, Topics, and Key Invariants) as specified below.

---

### Slot 1: `pyhroff-mcpaudit` (v0.8.0)

- **Repository:** `https://github.com/Pyhroff/pyhroff-mcpaudit`
- **PyPI Package:** `https://pypi.org/project/pyhroff-mcpaudit/`
- **One-Line Description (≤ 350 chars):**  
  `Fast, deterministic AST static security analyzer for Model Context Protocol (MCP) servers. Single-pass visitor with C-level token-hash filtering; prunes 94% of uncompromised files in O(1) time. 72.7% real-world precision across 135 repos with sub-50ms CI/CD gating.`
- **Website URL:** `https://pypi.org/project/pyhroff-mcpaudit/`
- **Topic Tags:**  
  `mcp` · `model-context-protocol` · `ast` · `static-analysis` · `security` · `python` · `pypi` · `ci-cd` · `fastmcp`
- **Key Technical Invariants:**
  - Single-pass Python `ast.NodeVisitor` combined with a 64-bit token-hash inverted index that prunes 94% of files in $O(1)$ time.
  - Empirical precision elevation: Disclosed 37.5% real-world baseline precision (95% CI: 24–53%) on 90 public servers in v0.6; elevated to 72.7% precision on 135 public repositories in v0.8 via AST reachability analysis.
  - Sub-50ms execution ceiling designed specifically as a pre-commit / CI gatekeeper.
- **Verification Command:**
  ```bash
  pip install pyhroff-mcpaudit==0.8.0
  mcpaudit --scan ./mcp-servers --format sarif
  ```

---

### Slot 2: `aisec-suite` (v0.3.0)

- **Repository:** `https://github.com/Pyhroff/aisec-suite`
- **PyPI Package:** `https://pypi.org/project/aisec-suite/`
- **One-Line Description (≤ 350 chars):**  
  `Empirical security evaluation harness and guard proxy for agentic workflows. Evaluates tool-poisoning and policy reachability via Z3 SMT constraint solving. Achieves 48.1% held-out recall at 0.03% FPR across 3,974 real-world tools with 0 false refutations on 120 findings.`
- **Website URL:** `https://pypi.org/project/aisec-suite/`
- **Topic Tags:**  
  `ai-security` · `agent-security` · `z3-solver` · `formal-verification` · `tool-poisoning` · `guardrails` · `pypi` · `python`
- **Key Technical Invariants:**
  - Automated security evaluation harness benchmarking agentic tool definitions against multi-stage injection encodings (NFKC, base64, unicode tags).
  - Empirical benchmark: 48.1% held-out recall at 0.03% false-positive rate across 3,974 real-world tool descriptions.
  - Policy reachability analyzer (`aisec/reach.py`) using Microsoft's Z3 SMT solver: verified zero false refutations on 120 labelled findings.
- **Verification Command:**
  ```bash
  pip install aisec-suite==0.3.0
  python -m unittest discover -s tests -p "test_*.py"
  ```

---

### Slot 3: `memsentry` (v1.2.0)

- **Repository:** `https://github.com/Pyhroff/memsentry`
- **PyPI Package:** `https://pypi.org/project/memsentry/`
- **One-Line Description (≤ 350 chars):**  
  `Runtime context protection and memory integrity guardrail for agentic memory stores. Detects cross-session state corruption, unauthorized memory overwrite, and indirect prompt injection attacks before vector or key-value persistence.`
- **Website URL:** `https://pypi.org/project/memsentry/`
- **Topic Tags:**  
  `agentic-memory` · `context-hygiene` · `runtime-security` · `vector-db` · `prompt-injection` · `pypi` · `python`
- **Key Technical Invariants:**
  - Intercepts agent memory read/write streams to enforce cryptographic integrity hashes and semantic drift thresholds.
  - Isolates cross-session memory poisoning attacks attempting to compromise long-term agent memory stores (Redis, Mem0, LangGraph checkpointers).
- **Verification Command:**
  ```bash
  pip install memsentry==1.2.0
  python -c "import memsentry; print(memsentry.__version__)"
  ```

---

### Slot 4: `pyhroff-ragsentry` (v1.1.0)

- **Repository:** `https://github.com/Pyhroff/pyhroff-ragsentry`
- **PyPI Package:** `https://pypi.org/project/pyhroff-ragsentry/`
- **One-Line Description (≤ 350 chars):**  
  `Retrieval-Augmented Generation (RAG) security gateway and context injection sanitizer. Performs chunk boundary validation, embedding anomaly detection, and prompt extraction filtering with sub-millisecond overhead.`
- **Website URL:** `https://pypi.org/project/pyhroff-ragsentry/`
- **Topic Tags:**  
  `rag-security` · `prompt-injection` · `retrieval-security` · `embedding-guard` · `llm-security` · `pypi` · `python`
- **Key Technical Invariants:**
  - Token-level chunk boundary enforcement preventing delimiter escape and context injection attacks in RAG pipelines.
  - Fast, zero-network embedding drift scoring for untrusted document chunks before synthesis.
- **Verification Command:**
  ```bash
  pip install pyhroff-ragsentry==1.1.0
  python -c "import ragsentry; print(ragsentry.__version__)"
  ```

---

### Slot 5: `upstream-contributions`

- **Repository:** `https://github.com/Pyhroff/upstream-contributions`
- **One-Line Description (≤ 350 chars):**  
  `Verified upstream open-source contributions across production AI and data infrastructure: SQLGlot (#8780 merged), LiteLLM (#47091 merged, #47105 BOLA advisory under review), SQLFluff (#8901, #8902 merged), CrewAI (#8240, #8242-#8245), and FastMCP (#6063).`
- **Website URL:** `https://github.com/Pyhroff/security-advisories`
- **Topic Tags:**  
  `open-source` · `contributions` · `sqlglot` · `litellm` · `sqlfluff` · `crewai` · `fastmcp` · `compilers` · `security`
- **Key Technical Invariants:**
  - Direct upstream patches merged into main releases of foundational repositories: `tobymao/sqlglot` (Snowflake lambda AST mutation), `BerriAI/litellm` (Cohere stop sequence normalization), and `sqlfluff/sqlfluff` (Doris/StarRocks grammar tree excision).
  - High-impact security disclosures: LiteLLM BOLA access control bypass on empty models list (#47105, self-assessed CVSS 7.5, PYHROFF-ADV-2026-001) and FastMCP Monty sandbox timer decoupling (#6063, self-assessed CVSS 5.3, PYHROFF-ADV-2026-002).
- **Verification Command:**
  ```bash
  gh pr view 8780  --repo tobymao/sqlglot   --json state,mergedAt,title
  gh pr view 47091 --repo BerriAI/litellm    --json state,mergedAt,title
  gh pr view 8901  --repo sqlfluff/sqlfluff  --json state,mergedAt,title
  gh pr view 8902  --repo sqlfluff/sqlfluff  --json state,mergedAt,title
  ```

---

### Slot 6: `systems-showcase`

- **Repository:** `https://github.com/Pyhroff/systems-showcase`
- **One-Line Description (≤ 350 chars):**  
  `High-throughput backend systems lab: 10,000 msg/s streaming vulnerability ingestion into PostgreSQL using O(1) RAM ijson and binary COPY, paired with a 5-node Raft distributed consensus engine with leader lease fencing and split-brain resilience.`
- **Website URL:** `https://github.com/Pyhroff`
- **Topic Tags:**  
  `postgresql` · `streaming` · `distributed-systems` · `raft-consensus` · `concurrency` · `mvcc` · `high-throughput` · `python`
- **Key Technical Invariants:**
  - Streaming JSON parser using `ijson` processing 50,000+ SARIF vulnerability records in strictly $O(1)$ memory, staged via unlogged PostgreSQL tables and binary `COPY`.
  - Deterministic lock ordering: `ON CONFLICT (asset_id, rule_hash) DO UPDATE` to prevent concurrent transaction deadlocks under high write pressure.
  - 5-node Raft distributed state machine (`Kronos-KV`) implementing leader leases, randomized election timers, monotonic fencing tokens, and split-brain network partition recovery.
- **Verification Command:**
  ```bash
  python gym/run_drills.py --test all
  python gym/sql_gym.py --test all
  ```

---

## 4. Quality & Audit Safeguards

When configuring and maintaining these pinned repositories, adhere strictly to the following standards established in `Argon/19_RESUME_CLAIMS_AUDIT.md`:

1. **Strict Version Parity:**
   - Always display the audited PyPI release tags: `pyhroff-mcpaudit v0.8.0`, `aisec-suite v0.3.0`, `memsentry v1.2.0`, `pyhroff-ragsentry v1.1.0`.
   - Never cite unreleased version numbers or unreleased internal packages.
2. **Empirical Honesty Over Marketing:**
   - Maintain the transparent disclosure of `pyhroff-mcpaudit`'s 37.5% baseline precision on 90 public servers; interviewers consider the engineering evolution to 72.7% via AST reachability a major hiring signal.
   - Ground all evaluation claims in real-world benchmark corpora with disclosed false positive rates.
3. **Formal Verification Framing:**
   - Formulate verification claims around automated policy reachability and constraint validation using the **Z3 SMT solver**.
   - Do not claim manual interactive theorem prover proof certificates.
4. **Active PR Status:**
   - Clearly delineate the 4 merged PRs from the 12 active PRs currently under maintainer review.
