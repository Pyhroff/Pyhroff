<div align="center">

# Praising Harris Ratnam
### AI Systems Security Researcher & Runtime Defense Engineer
**B.Tech CSE (Cybersecurity), IIIT Kottayam** · *Target: AI Systems / Security / Agent Engineering Internship*

[![GitHub Profile](https://img.shields.io/badge/GitHub-Pyhroff-181717?style=flat-square&logo=github)](https://github.com/Pyhroff)
[![Merged Tier-1 PR](https://img.shields.io/badge/SQLGlot-Merged%20by%20Toby%20Mao-purple?style=flat-square&logo=git)](https://github.com/tobymao/sqlglot/pull/8780)
[![Upstream PRs](https://img.shields.io/badge/Upstream%20PRs-27%20Tier--1-brightgreen?style=flat-square&logo=github)](https://github.com/Pyhroff)
[![MCP Benchmark](https://img.shields.io/badge/MCP%20Benchmark-48.1%25%20%40%200.03%25%20FPR-blue?style=flat-square)](https://github.com/Pyhroff/mcpaudit)
[![Security Advisories](https://img.shields.io/badge/Advisories-Repository-critical?style=flat-square&logo=github)](https://github.com/Pyhroff/security-advisories)
[![Latest Research Release](https://img.shields.io/badge/Release-v2026.10.1-blue?style=flat-square&logo=github)](https://github.com/Pyhroff/security-advisories/releases/tag/v2026.10.1)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Praising_Harris-0A66C2?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/praising-harris-8a3320330)
[![Email](https://img.shields.io/badge/Email-praisingharris%40gmail.com-D14836?style=flat-square&logo=gmail)](mailto:praisingharris@gmail.com)

</div>



---


### 🛡️ Core Focus & Research

AI Systems Security Researcher & Runtime Defense Engineer building formal verification provers, spectral weight forensics, and runtime defense proxies for autonomous agent architectures and large-scale model serving infrastructure. Active contributor to open-source AI infrastructure (`LiteLLM`, `FastMCP`, `CrewAI`).


---



### 🛡️ Featured AI Systems Security & Agent Tooling

```
  ┌────────────────────────────────────────────────────────────────────────────┐
  │                 AISEC-SUITE v2.2 (5-PLANE ARCHITECTURE)                    │
  ├────────────────────────────────────┬───────────────────────────────────────┤
  │ Plane 1: Formal Tool Graphs        │ Plane 2: Weight Spectral Forensics    │
  │ specprove-sec (Z3 SMT + Lean 4)    │ weightspecter v2.0 (RMT + SVD Exise)  │
  ├────────────────────────────────────┼───────────────────────────────────────┤
  │ Plane 3: Verifiable Inference      │ Plane 4: Activation Refusal Firewall  │
  │ attestinfer v2.0 (Freivalds P≤2⁻¹⁶)│ circuitshield v2.0 (SAE + Kalman)     │
  ├────────────────────────────────────┴───────────────────────────────────────┤
  │ Plane 5: Network Side-Channel Defense + Red-vs-Blue Wargame Arena          │
  │ tokenspecter v2.0 (Viterbi HMM + Ring Buffer Shaper: MI 1.985 → 0.000 bits)│
  └────────────────────────────────────────────────────────────────────────────┘
```

* **[aisec-suite v2.2](https://github.com/Pyhroff/aisec-suite)** *(12 Modules across 5 Mathematical Planes · 99/99 Tests · 4 SLSA-Signed PyPI Packages)*  
  *Unified AI security suite, live Guard Proxy (`aisec guard-proxy`), and autonomous Red-vs-Blue Wargame Arena (`aisec wargame`) combining **[specprove-sec](https://github.com/Pyhroff/specprove-sec)** (Z3 SMT + Lean 4 non-interference certificates), **[weightspecter](https://github.com/Pyhroff/weightspecter)** (Marchenko-Pastur RMT & BBP rank-1 backdoor excision), **[attestinfer](https://github.com/Pyhroff/attestinfer)** (16-round Rademacher Freivalds matmul prover + Wald $z$-test speculative decoding audit), **[circuitshield](https://github.com/Pyhroff/circuitshield)** (SAE monosemantic feature disentanglement + 2D Kalman Crescendo trajectory forecaster), **[tokenspecter](https://github.com/Pyhroff/tokenspecter)** (Viterbi HMM + Ring-Buffer token pacer), plus **[mcpaudit](https://github.com/Pyhroff/mcpaudit)**, **[memsentry](https://github.com/Pyhroff/memsentry)**, **[ragsentry](https://github.com/Pyhroff/ragsentry)**, and **[trainsentry](https://github.com/Pyhroff/trainsentry)**.*
* **[PromptStrike](https://github.com/Pyhroff/promptstrike)**  
  *Automated adversarial red-teaming CLI for LLMs — PAIR/TAP/Crescendo/GCG jailbreak algorithms, live WebSocket dashboard, multi-model sweep comparison, and CI/CD safety gate.*
* **[ModelHawk](https://github.com/Pyhroff/ModelHawk)**  
  *Static opcode-stream analyzer detecting code-execution backdoors (pickle-deserialization RCE) in PyTorch/pickle ML model files without loading weights.*
* **[loopcheck](https://github.com/Pyhroff/loopcheck)** & **[OSIRIS](https://github.com/Pyhroff/osiris)**  
  *Zero-instrumentation waste auditor for agent loops (115 tests, on PyPI) and model-agnostic 8-provider agent runtime with automatic failover and profiled 10× local-model latency fix (100 tests).*



---



### ⚛️ Standalone Research: Quantum Machine Learning, Verifiable Compilation, QEC & Post-Quantum Cryptography

* **[Q-MIND: Autonomous Quantum ML & Verifiable Fault-Tolerant Circuit Compilation Engine](https://github.com/Pyhroff/Q-MIND)** *(20 SQLite Empirical DBs · 5,060 Verified Trials · 172 Passing Tests · 27 300-DPI Figures)*  
  *Standalone empirical research framework investigating Fault-Tolerant Quantum Compilation, Variational Quantum Circuits, Riemannian geometry, and NISQ hardware noise:*
  - **Verifiable Fault-Tolerant Quantum Circuit Compilation (Kickmix Engine):** Multi-pass compiler combining Gidney Measurement-Based Uncomputation ($4T$ compute / $0T$ uncompute), Low-Chuang SelectSwap QROM synthesis ($\lambda = 2^k$), and phase-polynomial fusion with a **64-bit SIMD bit-parallel Kickmix equivalence fuzz verifier** ($486\text{M}$ gate-states/s, $100\%$ pass rate), reducing fault-tolerant **$T$-count by 58.5%** and **Toffoli count by 48.7%** across Fusion Energy ($1/\sqrt{x}$ stopping power), Decoded Quantum Interferometry ($\mathrm{GF}(2^m)$ Berlekamp-Massey decoder), and FeMoCo Quantum Chemistry (DF-QROM).
  - **Fubini-Study Quantum Natural Gradient (QNG):** Pullback metric tensor $g_{ij}(\theta) = \text{Re}[\langle \partial_i \psi | \partial_j \psi \rangle - \langle \partial_i \psi | \psi \rangle \langle \psi | \partial_j \psi \rangle]$ converges in **15 steps vs 80+** for Euclidean Adam (**5.3× speedup**) and escapes 8-qubit barren plateaus ($p = 0.0079$).
  - **Barren Plateau Scaling & Mitigation:** Verified McClean et al. exponential gradient decay from $N=4 \to 12$ qubits (slope $-0.822\text{ bits/qubit}, R^2 = 0.9968$) and restored **13.6× gradient variance** via Grant et al. identity-block + layerwise pretraining (**94.19% loss reduction**).
  - **Tri-Mitigation Pipeline (REM + Richardson ZNE + Clifford Data Regression):** Suppresses NISQ depolarizing + readout errors by **31.0%** across $p \in [0.005, 0.05]$.
  - **Honest Quantum-vs-Classical Boundary:** Classical RBF-SVM beats VQC on 4D tabular data (96.0% vs 91.3%) due to $\mathcal{O}(1/\sqrt{S})$ shot noise, while Quantum Kernel SVM, QCNN, and $S_N$-Equivariant QGNN reach **99.33% and 100%** on 8-qubit Transverse-Field Ising (TFIM) and $\mathbb{Z}_2 \times \mathbb{Z}_2$ SPT quantum phases.
* **[QEC Lab](https://github.com/Pyhroff/qec-lab)** & **[pqc-scanner](https://github.com/Pyhroff/pqc-scanner)**  
  *Rotated surface-code simulator (Stim + PyMatching v2 reproducing the $p \approx 1\%$ threshold and lattice surgery) and NIST FIPS 203/204/205 post-quantum cryptography static migration analyzer.*



---



### 🔬 Engineering Philosophy

$$\text{Threat / Physical Model} \longrightarrow \text{Formal / Spectral Analysis} \longrightarrow \text{Empirical Harness} \longrightarrow \text{Regression Test} \longrightarrow \text{Upstream Patch}$$

- **Defense-in-Depth**: I evaluate systems assuming the model layer is inherently untrusted. Security boundaries must live in the host process, AST/Z3 verifier, spectral weight auditor, and kernel/sandbox isolation layer.
- **Empirical Rigor**: Report exact $p$-values, confidence intervals, and honest negative results backed by reproducible SQLite telemetry.



---



### 🛠️ Technical Arsenal

- **Languages:** Python (Advanced AST/Asyncio/SciPy), Go, C/C++, Rust, TypeScript, SQL, Bash  
- **AI Infrastructure & Security:** LiteLLM, CrewAI, FastMCP, LangGraph, Z3 SMT Prover, Lean 4, Marchenko-Pastur RMT, Sparse Autoencoders (SAE), SARIF, OpenTelemetry, MITRE ATT&CK & ATLAS  
- **Quantum Computing & Cryptography:** PennyLane, Qiskit, Stim, PyMatching v2, Fubini-Study QNG, ZNE/CDR/REM Error Mitigation, NIST FIPS 203/204/205 (ML-KEM, ML-DSA, SLH-DSA), Schnorr ZKP  
- **Cloud & Databases:** AWS, GCP, Docker, Redis, PostgreSQL, SQLite, Neo4j  



---

### 🛡️ Selected Upstream Security Contributions & Open PRs

Authored upstream security advisories, vulnerability disclosures, and runtime defense patches across production AI infrastructure (`LiteLLM`, `FastMCP`, `CrewAI`):

| Project | PR / Advisory | Focus / Impact | Status |
|---|---|---|:---:|
| **SQLGlot** | [PR #8780](https://github.com/tobymao/sqlglot/pull/8780) | **AST Node Mutation in Lambda Rewrites** | 🟣 **Merged by Toby Mao** |
| **SQLFluff** | [PR #8900](https://github.com/sqlfluff/sqlfluff/pull/8900) | ANSI Access Schema Plural Keywords (FORMATS, POLICIES) | 🟢 **Approved by Danny Jones** |
| **SQLFluff** | [PR #8899](https://github.com/sqlfluff/sqlfluff/pull/8899) | StarRocks Fixed Range Partition Bracket Grammar | 🟢 **Verified by Duo-ee** |
| **SQLFluff** | [PR #8901](https://github.com/sqlfluff/sqlfluff/pull/8901) | Apache Doris StatementSegment FLUSH grammar isolation | 🟢 **Open** *(Tests Passing)* |
| **SQLFluff** | [PR #8902](https://github.com/sqlfluff/sqlfluff/pull/8902) | StarRocks StatementSegment FLUSH grammar isolation | 🟢 **Open** *(Tests Passing)* |
| **LiteLLM** | [Branch `fix/mcp-guardrails-fail-closed`](https://github.com/BerriAI/litellm/compare/main...Pyhroff:litellm:fix/mcp-guardrails-fail-closed) | **Fail-Closed Tool Resolution & External Server Check** (CWE-285/862) | 🟢 **Committed** *(28 Tests + Lean 4 Cert)* |
| **LiteLLM** | [PR #47312](https://github.com/BerriAI/litellm/pull/47312) | **BFLA Access Control Bypass** on /v1/mcp/access_groups (CVSS 7.5) | 🟢 **Open** *(Tests Passing)* |
| **LiteLLM** | [PR #47311](https://github.com/BerriAI/litellm/pull/47311) | Budget duration update authorization bypass (CVSS 6.5) | 🟢 **Open** *(Tests Passing)* |
| **Qualtran** | [PR #1986](https://github.com/quantumlib/Qualtran/pull/1986) | Fault-Tolerant Reversible Adder Bloq call graph CNOT cost | 🟢 **Open** *(Tested)* |
| **PennyLane** | [PR #10391](https://github.com/PennyLaneAI/pennylane/pull/10391) | Evolution operator pytree leaves & parameter-shift bindings | 🟢 **Open** *(Tested)* |
| **LiteLLM** | [PR #47105](https://github.com/BerriAI/litellm/pull/47105) | **BOLA Access Control Bypass** with empty models list (CVSS 7.5) | **Open** *(CI Passed)* |
| **LiteLLM** | [PR #47119](https://github.com/BerriAI/litellm/compare/main...Pyhroff:litellm:fix/allow-requests-db-unavailable-unconfigured-db?expand=1) | Fail-Open Prevention: Reject calls on unconfigured DB (CVSS 7.5) | **Open** *(Tested)* |
| **LiteLLM** | [PR #46916](https://github.com/BerriAI/litellm/compare/main...Pyhroff:litellm:fix/key-budget-duration-tier-auth?expand=1) | Budget reset & tier escalation prevention on key update (CVSS 6.5) | **Open** *(Tested)* |
| **LiteLLM** | [PR #47107](https://github.com/BerriAI/litellm/pull/47107) | Dual support & deduplication for `model_names` / `model_ids` | **Open** *(CI Passed)* |
| **FastMCP** | [PR #5786](https://github.com/PrefectHQ/fastmcp/pull/5786) | SSRF error handling in `validate_url` to stop 500 crashes | **Open** |
| **FastMCP** | [PR #6063](https://github.com/PrefectHQ/fastmcp/pull/6063) | **Enforce wall-clock timeout & callback limit in Monty & CodeMode** | 🟢 **Open** *(65/65 Tests Pass)* |
| **FastMCP** | [ADV-2026-002](https://github.com/Pyhroff/security-advisories/blob/main/GHSA_FASTMCP_SANDBOX_AUDIT.md) | Async Monty sandbox boundary analysis & callback decoupling | **Audited** |
| **CrewAI** | [PR #8240](https://github.com/crewAIInc/crewAI/pull/8240) | Native MCP pagination cursor handling (`nextCursor`) | **Open** |
| **CrewAI** | [PR #8244](https://github.com/crewAIInc/crewAI/pull/8244) | Percent-encoded password decoding in `REDIS_URL` | **Open** |
| **Presidio** | [PR #2418](https://github.com/data-privacy-stack/presidio/pull/2418) | Docker anonymizer container port forwarding fix (`5001:3000`) | **Open** |

> *Full list of 20+ upstream advisories & patches available at [security-advisories](https://github.com/Pyhroff/security-advisories).*

---



### 📬 Connect With Me

- **Email:** [praisingharris@gmail.com](mailto:praisingharris@gmail.com)  
- **LinkedIn:** [linkedin.com/in/Praising_Harris](https://www.linkedin.com/in/Praising_Harris)  
- **Security Advisories:** [github.com/Pyhroff/security-advisories](https://github.com/Pyhroff/security-advisories)
