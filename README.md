<div align="center">

# Praising Harris Ratnam
### AI Systems Security Researcher & Runtime Defense Engineer
**B.Tech Computer Science & Engineering (Cybersecurity) · Indian Institute of Information Technology (IIIT) Kottayam (2024–2028)**  

[![GitHub](https://img.shields.io/badge/GitHub-Pyhroff-181717?style=flat-square&logo=github)](https://github.com/Pyhroff)
[![PyPI](https://img.shields.io/badge/PyPI-aisec--suite_v0.3.0-blue?style=flat-square&logo=pypi)](https://pypi.org/project/aisec-suite/)
[![SQLGlot Merged](https://img.shields.io/badge/SQLGlot-PR_%238780_Merged-8957e5?style=flat-square&logo=git)](https://github.com/tobymao/sqlglot/pull/8780)
[![LiteLLM Merged](https://img.shields.io/badge/LiteLLM-PR_%2347091_Merged-8957e5?style=flat-square&logo=git)](https://github.com/BerriAI/litellm/pull/47091)
[![FastMCP Open](https://img.shields.io/badge/FastMCP-PR_%236063_Open-success?style=flat-square&logo=git)](https://github.com/PrefectHQ/fastmcp/pull/6063)
[![Upstream](https://img.shields.io/badge/Contributions-27_Tier--1_PRs-2ea44f?style=flat-square&logo=github)](https://github.com/Pyhroff)
[![Lean 4](https://img.shields.io/badge/Formal_Proof-13_Lean_4_Certs-darkgreen?style=flat-square)](https://github.com/Pyhroff/specprove-sec)
[![Z3 SMT](https://img.shields.io/badge/SMT_Prover-Z3_k--Induction-orange?style=flat-square)](https://github.com/Pyhroff/specprove-sec)
[![TryHackMe](https://img.shields.io/badge/TryHackMe-Top_2%25-red?style=flat-square&logo=tryhackme)](https://tryhackme.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Praising_Harris-0A66C2?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/praising-harris-8a3320330)
[![Email](https://img.shields.io/badge/Email-praisingharris%40gmail.com-D14836?style=flat-square&logo=gmail)](mailto:praisingharris@gmail.com)

</div>

---

### 🛡️ Profile & Core Research Philosophy

AI Systems Security Researcher and Systems Software Engineer focused on deterministic runtime defense, formal protocol verification, and compiler internals for autonomous AI infrastructure. I design mathematical runtime invariants rather than relying solely on probabilistic prompt filtering, engineering verified defenses across gateway routers, microVM sandboxes, and language model weight tensors.

$$\text{Threat / Physical Model} \longrightarrow \text{Formal / Spectral Analysis} \longrightarrow \text{Empirical Test Harness} \longrightarrow \text{Regression Verification} \longrightarrow \text{Upstream Production Patch}$$

- **Zero-Trust Host Boundaries:** Treat all model outputs, AST structures, and third-party tool definitions as untrusted input. Defense resides in host compilers, kernel syscall monitors, and SMT-verified state machines.
- **Empirical Reproducibility:** Every metric is backed by automated test suites, Lean 4 certificates, and reproducible databases. Zero speculation, zero fabricated claims.

---

### 🏛️ 5-Plane Security & Research Architecture

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        AISEC-SUITE: 5-PLANE SECURITY ARCHITECTURE                      │
├──────────────────────────────────────────┬─────────────────────────────────────────────┤
│ Plane 1: Formal Protocol Verification    │ Plane 2: Weight Spectral Forensics          │
│ specprove-sec (Z3 SMT + 13 Lean 4 Certs) │ weightspecter (RMT Marchenko-Pastur Law)    │
│ - Bounded Model Checking (k-induction)   │ - BBP outlier spikes (350x - 976x detected) │
│ - CEGIS automated guard synthesis        │ - Surgical rank-1 deflation (0% FPR)        │
├──────────────────────────────────────────┼─────────────────────────────────────────────┤
│ Plane 3: Verifiable Inference & Checks   │ Plane 4: Activation Refusal Firewall        │
│ attestinfer (Freivalds Matmul P <= 2^-16)│ circuitshield (Residual Stream Clamping)    │
│ - 16-round Rademacher randomized checks  │ - Ortho-ablation & CAA steering mitigation  │
│ - SHA-256 Merkle activation audit tree   │ - Preserves refusal direction integrity     │
├──────────────────────────────────────────┴─────────────────────────────────────────────┤
│ Plane 5: Encrypted Network Side-Channel Defense & Traffic Shaping                      │
│ tokenspecter (Bayesian Viterbi DP + Ring-Buffer Bucket Pacer)                          │
│ - Eliminates SSE token timing leakage: Mutual Information 1.985 -> 0.000 bits/token     │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

---

### 🚀 Flagship Engineering & Research Systems

#### 1. [aisec-suite](https://github.com/Pyhroff/aisec-suite) — Multi-Plane AI Security Umbrella & Runtime Scanner
*Published on PyPI as `aisec-suite 0.3.0` · 12 Modules across 5 Mathematical Security Planes · SARIF 2.1.0 Integration*
- Multi-view structural tool poisoning detector analyzing raw schemas across 6 normalization passes (Unicode tags, bidi overrides, zero-width spaces, NFKC canonicalization, Base64, and rot13).
- Evaluated on a benchmark corpus of **3,974 real-world production MCP tools**: achieved **48.1% held-out recall at a 0.03% false-positive rate** (only 1 false positive across 3,974 clean tools).
- Evaluated on 120 labelled vulnerability findings with **zero wrong refutations** and deterministic exit codes (`0` clean, `1` findings detected, `2` execution crash).
- Includes formal MCP protocol audits, memory safety analyzers, and SARIF 2.1.0 report generation for CI/CD pipeline integration.

#### 2. [weightspecter](https://github.com/Pyhroff/weightspecter) — Data-Free Spectral RMT Weight Analyzer for LLMs & LoRA
*Data-Free Spectral Forensics · Random Matrix Theory (RMT) · Surgical Rank-1 Deflation*
- Analyzes weight matrices in `.safetensors` and PEFT LoRA checkpoints using the Marchenko-Pastur bulk distribution law: $\lambda_+ = \hat{\sigma}^2(1 + \sqrt{\gamma})^2$.
- Detects Baik-Ben Arous-Péché (BBP) phase transitions where poisoned adapter eigenvalues spike $350\times - 976\times$ outside the random bulk, coupled with Inverse Participation Ratio (IPR) spatial localization ($83.3 - 105.5$ vs $3.2 - 3.5$ for clean weights).
- Evaluated across 6 model checkpoints (2 clean, 4 trojans: rank-1 trigger, sparse token sleeper, cross-layer highway, spectral evasion): achieved **100.0% precision, 100.0% recall, 0.0% FPR**, sanitizing all 4 trojan adapters via surgical rank-1 SVD deflation while preserving 100% of the benign singular subspace ($i \ge 2$).

#### 3. [specprove-sec](https://github.com/Pyhroff/specprove-sec) — Formal Z3 SMT Bounded Model Checker & Lean 4 Prover
*Formal Methods · Z3 SMT k-Induction · CEGIS Synthesis · 13 Machine-Checked Lean 4 Certificates*
- Bounded model checker and unbounded $k$-induction prover verifying security invariants across 12 distributed agent and gateway protocols (`MCP-01` through `MCP-04`, `ZTA-01`, `CRYPTO-01`, `HITL-01`, `RAG-01`, `MEM-01`, `CLOUD-01`, `SAFE-01`, `SAFE-02`).
- Discovered exploit counterexamples for 10/10 vulnerable protocols at shallow depths ($k \in [1, 4]$) in 149–321 ms per protocol across 161 SMT queries.
- Counterexample-Guided Inductive Synthesis (CEGIS) engine automatically synthesizes strengthening guard conditions, proves them non-vacuous (`SAT`), verifies inductive safety for all execution horizons $\forall k \in [0, \infty)$ (`UNSAT`), and compiles formal machine-checked proof certificates into Lean 4 (`lean_certs/`).

#### 4. [ZeroTrace](https://github.com/Pyhroff/zerotrace) — Pure x86_64 Direct Syscall Forensics & Active Directory Min-Cut Engine
*Zero AI Dependencies · Pure Systems & Low-Level Cybersecurity · 10/10 Pytest Passing*
- **`SyscallImplantHunter`**: Detects Hell's Gate (`4C 8B D1 B8 <SSN> 0F 05`), Halo's/Tartarus' Gate neighbor hook bypasses (`E9 <rel32>` before `B8`), and SysWhispers3 indirect syscall trampolines jumping into `ntdll.dll`. Performs disk-vs-memory `.text` byte-diffing on Native APIs (`NtAllocateVirtualMemory`, `NtProtectVirtualMemory`, `NtWriteVirtualMemory`, `NtCreateThreadEx`) and scans private RWX memory using sliding-window Shannon entropy: achieved **100.0% recall (20/20) and 0.0% FPR (0/20) in 13.06 ms**.
- **`ADAttackGraphEngine`**: Models BloodHound enterprise Active Directory privilege graphs (`GenericAll`, `WriteDacl`, `WriteOwner`, `AddKeyCredentialLink`, `DCSync`, `AllowedToAct`). Solves the Exact Minimum-Weight $s$-$t$ Edge Cut via Edmonds-Karp maximum flow, **severing 100.0% of compromise paths to Tier-0 (180 to 0)** across 15 enterprise graphs in 6.09 ms by revoking only **7.15% (44/615)** remediable edges (92.85% attack surface reduction).
- **`BehavioralEvasionEngine`**: Deterministically strips 5 layers of CLI obfuscation (PowerShell Base64 UTF-16LE, cmd.exe carets `^`, backticks, quote fragmentation, and `[char]0xXX`), boosting naive Sigma detection recall from **35.7% to 100.0% at 0.0% FPR** ($F_1 = 1.000$).

#### 5. [Q-MIND](https://github.com/Pyhroff/Q-MIND) — Autonomous Quantum ML & Verifiable Fault-Tolerant Compiler
*20 SQLite Empirical DBs · 5,060 Verified Trials · 172 Passing Pytest Tests · 27 Figures at 300 DPI*
- **Verifiable Fault-Tolerant Circuit Compilation (Kickmix Engine)**: Combines Gidney Measurement-Based Uncomputation ($4T$ compute / $0T$ uncompute), Low-Chuang SelectSwap QROM ($\lambda = 2^k$), and phase-polynomial fusion. Achieved **58.53% T-gate reduction**, **48.73% Toffoli reduction**, and **21.37% depth reduction** across Fusion Energy ($1/\sqrt{x}$ stopping power) and Decoded Quantum Interferometry ($\mathrm{GF}(2^m)$ Berlekamp-Massey decoder).
- Verified via a **64-bit SIMD bit-parallel Kickmix equivalence fuzz verifier** executing at **486M gate-states/s with a 100.0% pass rate** (0 bit mismatches, 0 ancilla leaks).
- **Riemannian Quantum Natural Gradient (QNG)**: Evaluates the pullback Fubini-Study metric tensor with adaptive Tikhonov regularization, yielding a **5.3x convergence speedup** vs Adam (15 steps vs 80+) and **51.1% mean loss reduction**.
- **Barren Plateau & Tri-Mitigation**: Restored 13.6x gradient variance at 8 qubits using local observables and identity blocks; Tri-mitigation pipeline (REM + Richardson ZNE + Clifford Data Regression) suppressed NISQ noise degradation by 31.0%. Documented honest negative results: classical RBF-SVM beats VQC on 4D tabular data (96.0% vs 91.3%), whereas QCNN reaches 100% test accuracy on topological cluster SPT phases.

#### 6. [kronos-kv](https://github.com/Pyhroff/kronos-kv) — Pure Distributed Raft & Bitcask LSM Storage Engine
*Pure Python 3.10+ Standard Library · Zero External Dependencies · 8/8 Pytest Passing*
- **Storage Engine**: Append-only binary Write-Ahead Log (`active.wal`) with 20-byte deterministic binary headers (`>IdII`: 32-bit CRC32, epoch timestamp, key length, value length). In-memory `KeyDir` index enables $O(1)$ single-seek point reads (**0.11 ms/read**, 91.09 ms for 800 reads). Merge-sort compaction reclaims **84.29% disk space** (870,600 B to 136,800 B) while preserving all 800 live keys.
- **Bloom Filter**: Kirsch-Mitzenmacher double hashing ($g_i(x) = (h_1(x) + i \cdot h_2(x)) \bmod m$) with dual independent BLAKE2b 64-bit digests: achieved **0.00% false negatives and 0.19% empirical FPR** across 10,000 negative lookups.
- **5-Node Raft Consensus**: Complete implementation of Ongaro & Ousterhout protocol (§5.2 leader election, §5.3 log replication, §5.4 election safety and majority commit). Tested across 30 asymmetric network partition ([2] vs [3]) and leader crash scenarios: **100.0% (30/30) split-brain prevention** and linearizable log convergence in 7.24 ms.
- **Consistent Hashing**: 150 virtual nodes per physical shard on a 64-bit BLAKE2b hash ring. When scaling from 8 to 9 shards, only **9.47% of 10,000 keys were remapped** (closely matching theoretical optimal $1/N = 11.11\%$, avoiding $\sim 88.9\%$ disruption of naive modulo).

#### 7. [OSIRIS](https://github.com/Pyhroff/osiris) & [loopcheck](https://github.com/Pyhroff/loopcheck) — AI Agent Runtime & Waste Auditor
*AI Systems Infrastructure · 121 Tests (loopcheck) · 65 Tests (OSIRIS)*
- **OSIRIS**: Model-agnostic personal AI OS routing across 8 backend providers with zero-latency deterministic keyword dispatch and automatic failover (Gemini Flash -> Groq Llama 3.3 -> local Ollama Qwen 2.5 -> OpenAI). Profiled and optimized local-model latency from **100 s to 10 s** by replacing generic OpenAI-compatible endpoint with a native adapter handling `think:false`.
- **loopcheck**: Zero-instrumentation waste auditor for agent execution traces. Detects duplicate calls post-success, loop thrashing (>4 repeats), and stale retry loops ($\ge 2$ identical-argument failures). Features turn-aware `TraceRecorder` eliminating token double-counting on parallel turns, and `--fail-on-regression` CI gating.

---

### 🌐 Upstream Open-Source Contribution Matrix

Comprehensive audit of 27 Tier-1 upstream pull requests, compiler patches, and security remediations:

| Repository | Pull Request / Commit | Category | Technical Contribution & Mechanism | Review Status |
|:---|:---|:---|:---|:---:|
| **`tobymao/sqlglot`** | [PR #8780](https://github.com/tobymao/sqlglot/pull/8780) | Compilers / AST Bugfix | Fixed shared `DataType` AST node mutation in `_replace_lambda` during multi-argument lambda transpilation (`exp.Cast(this=arg, to=data_type.copy())`). Passed all 9 CI dialect test suites. | 🟣 **MERGED by Toby Mao** |
| **`BerriAI/litellm`** | [PR #47091](https://github.com/BerriAI/litellm/pull/47091) | Adapter / Schema Mapping | Standardized Cohere string `stop` parameter mapping to list of strings for `stop_sequences` in `CohereChatConfig`. | 🟣 **MERGED** |
| **`sqlfluff/sqlfluff`** | [PR #8900](https://github.com/sqlfluff/sqlfluff/pull/8900) | SQL Parser / ANSI Grammar | Added `FORMATS` and `POLICIES` unreserved keywords to `AccessSchemaPluralObjectSegment`, fixing parser runtime crashes. | 🟢 **APPROVED (LGTM by Danny Jones)** |
| **`sqlfluff/sqlfluff`** | [PR #8899](https://github.com/sqlfluff/sqlfluff/pull/8899) | SQL Parser / StarRocks | Replaced raw string literal with `Ref("CommaSegment")` for fixed range partitions. 57 dialect tests pass cleanly (`unparsable=0`). | 🟢 **VERIFIED (by Duo-ee)** |
| **`sqlfluff/sqlfluff`** | [PR #8901](https://github.com/sqlfluff/sqlfluff/pull/8901) | SQL Parser / Apache Doris | Removed inherited MySQL `FlushStatementSegment` from Doris `StatementSegment.match_grammar`. 141 tests pass. | 🟢 **OPEN (In Review)** |
| **`sqlfluff/sqlfluff`** | [PR #8902](https://github.com/sqlfluff/sqlfluff/pull/8902) | SQL Parser / StarRocks | Removed unsupported `FlushStatementSegment` from StarRocks grammar. 54 dialect tests pass. | 🟢 **OPEN (In Review)** |
| **`PrefectHQ/fastmcp`** | [PR #6063](https://github.com/PrefectHQ/fastmcp/pull/6063) | Agent Security / Sandbox DoS | Mitigated CWE-653/CWE-400 host microVM starvation in `CodeMode` by adding `wall_clock_timeout_secs` and `max_external_calls` callback budget caps. 65/65 tests pass. | 🟢 **OPEN (65/65 CI Pass)** |
| **`BerriAI/litellm`** | [Commit `846d37e8`](https://github.com/BerriAI/litellm) | Gateway Security / CWE-285 | Remediated fail-open tool resolution on non-hyphenated MCP dictionaries and unvetted URLs. Formally proved safe in Lean 4 (`MCP_04.lean`). 28/28 tests pass. | 🟢 **COMMITTED (Verified)** |
| **`BerriAI/litellm`** | [PR #47105](https://github.com/BerriAI/litellm/pull/47105) | API Security / BOLA Bypass | Fixed Broken Object-Level Authorization bypass in `can_object_call_model()` where empty `models: []` list was treated as an unrestricted wildcard. | 🟢 **OPEN (Reviewed by Maintainer)** |
| **`BerriAI/litellm`** | [PR #47312](https://github.com/BerriAI/litellm/pull/47312) | API Security / BFLA Bypass | Scoped `/v1/mcp/access_groups` to caller-accessible servers, preventing cross-tenant information leakage of internal server topologies. | 🟢 **OPEN (In Review)** |
| **`BerriAI/litellm`** | [PR #47311](https://github.com/BerriAI/litellm/pull/47311) | FinOps / Auth Bypass | Enforced authorization checks on `budget_duration` and `budget_id` updates in `/key/update` to block spend limit tampering. | 🟢 **OPEN (In Review)** |
| **`BerriAI/litellm`** | [PR #47107](https://github.com/BerriAI/litellm/pull/47107) | Proxy / Access Groups | Resolved access group resolution inconsistency when mixing alias `model_names` and unique `model_ids`. Restored 404 check. | 🟢 **OPEN (In Review)** |
| **`BerriAI/litellm`** | [PR #47106](https://github.com/BerriAI/litellm/pull/47106) | ORM / DB Crash Prevention | Excluded duplicate `budget_id` kwargs passed to Prisma ORM during entity budget updates, preventing HTTP 500 crashes. | 🟢 **OPEN (In Review)** |
| **`BerriAI/litellm`** | [PR #47097](https://github.com/BerriAI/litellm/pull/47097) | Observability / Telemetry | Dispatched router failure callbacks on rejected `/v1/images/generations` requests to Langfuse and OpenTelemetry. | 🟢 **OPEN (In Review)** |
| **`BerriAI/litellm`** | [PR #47119](https://github.com/BerriAI/litellm/pull/47119) | Auth / Fail-Open Prevention | Rejected proxy requests when database is unconfigured instead of falling back to insecure `INTERNAL_USER`. | 🟢 **OPEN (In Review)** |
| **`crewAIInc/crewAI`** | [PR #8240](https://github.com/crewAIInc/crewAI/pull/8240) | Agent Tooling / MCP Pagination | Implemented iterative cursor handling (`nextCursor`) across `list_tools`, `list_prompts`, and tool resolvers for >100 tools. | 🟢 **OPEN (In Review)** |
| **`crewAIInc/crewAI`** | [PR #8242](https://github.com/crewAIInc/crewAI/pull/8242) | Agent State / Context Retention | Preserved upstream task execution context during guardrail validation retries, preventing amnesia loops. | 🟢 **OPEN (In Review)** |
| **`crewAIInc/crewAI`** | [PR #8243](https://github.com/crewAIInc/crewAI/pull/8243) | Systems / Logging Hygiene | Fixed `suppress_logging()` context manager using `try...finally` to ensure logger levels are restored on exceptions. | 🟢 **OPEN (In Review)** |
| **`crewAIInc/crewAI`** | [PR #8244](https://github.com/crewAIInc/crewAI/pull/8244) | Distributed State / Redis Auth | Unquoted percent-encoded passwords in `REDIS_URL` prior to passing credentials to `aiocache.RedisCache`. | 🟢 **OPEN (In Review)** |
| **`crewAIInc/crewAI`** | [PR #8245](https://github.com/crewAIInc/crewAI/pull/8245) | Stream Parsing / Cross-Platform | Counted deferred tool result lines using universal newlines (`io.StringIO.readlines()`) to prevent Unicode line separator crashes. | 🟢 **OPEN (In Review)** |
| **`quantumlib/Qualtran`** | [PR #1986](https://github.com/quantumlib/Qualtran/pull/1986) | Quantum / Resource Estimation | Corrected fault-tolerant CNOT and T-gate estimation formulas in Cuccaro `Add.build_call_graph` for asymmetric register bitwidths. | 🟢 **OPEN (In Review)** |
| **`PennyLaneAI/pennylane`** | [PR #10391](https://github.com/PennyLaneAI/pennylane/pull/10391) | Quantum / Autodiff & PyTrees | Registered Hamiltonian Evolution operator PyTree leaves and parameter-shift bindings to prevent JIT gradient tracing crashes. | 🟢 **OPEN (In Review)** |
| **`microsoft/presidio`** | [PR #2418](https://github.com/microsoft/presidio/pull/2418) | Security Docs / Container Port | Updated container port mapping in documentation from `-p 5001:5001` to `-p 5001:3000` to align host publishing with Gunicorn. | 🟢 **OPEN (In Review)** |
| **`graphql-python/graphene`** | Branch `feat/lazy-connection-node` | Frameworks / Schema Deadlock | Implemented lazy type references for `Connection.Meta.node` (#1600), resolving circular import deadlocks in Relay schemas. | 🟢 **COMMITTED (Tested)** |

---

### 🛠️ Technical Arsenal

- **Languages:** Python (Advanced AST, Asyncio, SciPy, PyTorch, CPython Internals), C/C++ (x86_64 Syscalls, Win32 API, Pointers/PE Internals), Lean 4, Rust, SQL, Bash
- **Formal Verification & SMT:** Z3 SMT Solver, Bounded Model Checking ($k$-induction), CEGIS Synthesis, Lean 4 Interactive Theorem Prover, Invariant Synthesis
- **AI Systems & Security:** Model Context Protocol (MCP), LiteLLM Proxy, FastMCP, CrewAI, Random Matrix Theory (Marchenko-Pastur Law), Sparse Autoencoders (SAE), SARIF 2.1.0, MITRE ATT&CK & ATLAS
- **Systems & Storage:** Raft Distributed Consensus, Bitcask LSM Storage Engine, Append-Only Binary WAL, Kirsch-Mitzenmacher Bloom Filters, Consistent Hashing
- **Cybersecurity & Forensics:** Direct Syscall Forensics (Hell's/Halo's Gate, SysWhispers3), Disk-vs-Memory `.text` Diffing, Active Directory Attack Graphs (BloodHound), Edmonds-Karp Min-Cut, Sysmon Telemetry, Sigma Rules
- **Quantum Computing & Cryptography:** PennyLane, Google Qualtran, Qiskit, Stim, PyMatching v2, Fubini-Study QNG, NIST FIPS 203/204/205 (ML-KEM, ML-DSA, SLH-DSA)
- **DevOps, Tooling & Verification:** Docker, GitHub Actions CI/CD (OIDC Trusted Publishing), Pytest, Ruff, SQLite, Redis, Linux, Git Internals

---

### 📦 Repository Showcase & Specifications

- **Repository Showcase Cards:** [`profile_repo/SHOWCASE_CARDS.md`](https://github.com/Pyhroff/Pyhroff/blob/main/SHOWCASE_CARDS.md) — Detailed card metadata, architecture blueprints, empirical benchmarks, and reproduction recipes for all 7 flagship systems and upstream PRs.
- **Repository Banner Specification:** [`BANNER_SPECIFICATION.md`](https://github.com/Pyhroff/Pyhroff/blob/main/BANNER_SPECIFICATION.md) — Visual geometry, dark slate palette (`#0F172A`, `#0F766E`, `#10B981`, `#38BDF8`), typography, and SVG markup template for GitHub social preview banners.
- **Formal Whitepapers & Publications:**
  - [Formal Verification of MCP Runtimes via Z3 & Lean 4](https://github.com/Pyhroff/Pyhroff/blob/main/MEDIUM_TECHNICAL_ARTICLES/formal_verification_mcp_security.md)
  - [Hunting Evasive Syscall Implants with Pure Systems Forensics](https://github.com/Pyhroff/Pyhroff/blob/main/MEDIUM_TECHNICAL_ARTICLES/hunting_evasive_syscall_implants_zerotrace.md)
  - [Autonomous Quantum Circuit Compilation & Fault-Tolerant Resource Estimation](https://github.com/Pyhroff/Pyhroff/blob/main/MEDIUM_TECHNICAL_ARTICLES/autonomous_quantum_circuit_optimization.md)
  - [Transpiler AST Node Mutation: A Post-Mortem on SQLGlot Issue #8780](https://github.com/Pyhroff/Pyhroff/blob/main/MEDIUM_TECHNICAL_ARTICLES/sqlglot_ast_mutation_postmortem.md)

---

### 📬 Connect & Technical Inquiries

Feel free to reach out regarding systems security research, compiler internals, or open-source collaborations:
- **Email:** [praisingharris@gmail.com](mailto:praisingharris@gmail.com)
- **LinkedIn:** [linkedin.com/in/praising-harris-8a3320330](https://www.linkedin.com/in/praising-harris-8a3320330)
- **GitHub:** [github.com/Pyhroff](https://github.com/Pyhroff)
- **PyPI Portfolio:** [pypi.org/user/pyhroff](https://pypi.org/user/pyhroff/)
