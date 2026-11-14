# Repository Showcase Cards Catalog

This catalog defines the official repository-level showcase cards, OpenGraph social preview metadata, architecture blueprints, empirical benchmarks, and verification recipes for Praising Harris Ratnam's (`@Pyhroff`) flagship systems and upstream open-source contributions.

---

## PART I: FLAGSHIP ENGINEERING & RESEARCH SYSTEMS

---

### Card 1: `aisec-suite` — Multi-Plane AI Security Umbrella & Runtime Scanner

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│ [REPOS] Pyhroff/aisec-suite           [PYPI] aisec-suite v0.3.0        [BUILD] passing │
│ [DOMAINS] AI Systems Security · MCP Runtimes · SARIF 2.1.0 · Static & Dynamic AST      │
│ [ALIGNMENT] Primary: Resume_AI_Security_v5  |  Secondary: Resume_AI_Engineer_v5      │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

#### Social Preview Metadata
- **Repository Title:** `aisec-suite`
- **Short Description (150 chars):** Unified CLI & multi-view scanner enforcing deterministic mathematical invariants across MCP tool schemas, memory, and LLM gateway routers.
- **Topics / Tags:** `ai-security`, `mcp`, `sarif`, `runtime-defense`, `tool-poisoning`, `python-ast`, `zero-trust`
- **Badges:**
  ```markdown
  [![PyPI](https://img.shields.io/pypi/v/aisec-suite.svg?style=flat-square&logo=pypi)](https://pypi.org/project/aisec-suite/)
  [![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square)](https://opensource.org/licenses/MIT)
  [![Tests](https://img.shields.io/badge/Pytest-65_passing-brightgreen.svg?style=flat-square)](https://github.com/Pyhroff/aisec-suite)
  [![SARIF 2.1.0](https://img.shields.io/badge/Output-SARIF_2.1.0-orange.svg?style=flat-square)](https://sarifweb.azurewebsites.net/)
  ```

#### Core Architecture
```
Raw Tool Definition / Schema
   │
   ▼
[6-Normalization Pipeline]
   ├── 01. NFKC Canonicalization
   ├── 02. Unicode Tag & Bidi Override Stripping (\u202E, \uE0000)
   ├── 03. Zero-Width Space & Homoglyph Normalization
   ├── 04. Multi-Layer Base64 & ROT13 Unpacking
   ├── 05. Structural AST Parameter Extraction
   └── 06. Levenshtein / Jaro-Winkler Shadowing Distance
   │
   ▼
[Multi-View Detection Matrix] ──► [SARIF 2.1.0 Engine] ──► Deterministic Exit Code (0, 1, 2)
```

#### Empirical Benchmark Numbers
- **Corpus Size:** Evaluated on **3,974 production Model Context Protocol (MCP) tool schemas**.
- **Recall & False Positive Rate:** Achieved **48.1% held-out recall at a 0.03% false-positive rate** (only 1 false positive across 3,974 clean schemas).
- **Labelled Findings:** Evaluated across **120 labelled vulnerability findings with zero wrong refutations**.
- **Exit Codes:** Strict deterministic contract: `0` (clean), `1` (vulnerability detected), `2` (parser crash / execution error).
- **AgentDojo Runtime Guard:** Halted **56.9% of AgentDojo attacks (99.3% banking, 95.2% Slack)** without reading prose intent.

#### Verification Command
```bash
cd oss_contributions/aisec-suite
pytest tests/ -v
python -m aisec.cli scan --help
```

---

### Card 2: `weightspecter` — Data-Free Spectral RMT Weight Forensics for LLMs

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│ [REPOS] Pyhroff/weightspecter         [VERSION] v1.0.0                 [TESTS] 10/10   │
│ [DOMAINS] Random Matrix Theory · Safetensors · LoRA PEFT · BBP Phase Transitions      │
│ [ALIGNMENT] Primary: Resume_AI_Security_v5  |  Secondary: Resume_AI_Engineer_v5      │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

#### Social Preview Metadata
- **Repository Title:** `weightspecter`
- **Short Description (150 chars):** Data-free spectral RMT analyzer detecting trojan spikes in safetensors/LoRA weights via Marchenko-Pastur bulk law and surgical rank-1 SVD deflation.
- **Topics / Tags:** `random-matrix-theory`, `llm-security`, `weightspecter`, `safetensors`, `lora-peft`, `svd-deflation`
- **Badges:**
  ```markdown
  [![Pytest](https://img.shields.io/badge/Pytest-10_passing-brightgreen?style=flat-square)](https://github.com/Pyhroff/weightspecter)
  [![Precision](https://img.shields.io/badge/Precision-100%25-brightgreen?style=flat-square)](https://github.com/Pyhroff/weightspecter)
  [![Recall](https://img.shields.io/badge/Recall-100%25-brightgreen?style=flat-square)](https://github.com/Pyhroff/weightspecter)
  [![FPR](https://img.shields.io/badge/FPR-0.0%25-brightgreen?style=flat-square)](https://github.com/Pyhroff/weightspecter)
  ```

#### Core Architecture
$$\lambda_+ = \hat{\sigma}^2(1 + \sqrt{\gamma})^2, \quad \text{where } \gamma = \frac{N}{M}$$

```
Weight Matrix W ∈ R^{M×N} (LoRA or .safetensors)
   │
   ▼
[Empirical Spectral Decomposition: W^T W]
   │
   ├── Compute Marchenko-Pastur Upper Bulk Edge λ_+
   ├── Detect Baik-Ben Arous-Péché (BBP) Outlier Spikes: λ_max >> λ_+
   └── Compute Inverse Participation Ratio (IPR): IPR = \sum_i v_i^4 / (\sum_i v_i^2)^2
   │
   ▼
[Surgical Rank-1 SVD Deflation]
   W_sanitized = W - σ_1 · u_1 · v_1^T  (preserving 100% of benign subspace i ≥ 2)
```

#### Empirical Benchmark Numbers
- **Test Matrix:** 6 model checkpoints (2 clean baseline, 4 trojanized: rank-1 trigger, sparse token sleeper, cross-layer highway, spectral evasion).
- **Classification Performance:** **100.0% precision, 100.0% recall, 0.0% false positive rate**.
- **BBP Outlier Ratio:** Clean models exhibit $1.37\times - 1.47\times$ vs trojan models exhibiting **$353\times - 976\times$** spike ratio.
- **Effective Rank Collapse:** Clean models: $13.7 - 13.9$ vs poisoned adapters: **$1.07 - 1.21$**.
- **Remediation:** 4/4 trojan adapters surgically neutralized without retraining.

#### Verification Command
```bash
cd oss_contributions/weightspecter
pytest tests/test_weightspecter.py -v
python -c "import json; data=json.load(open('reports/benchmark-summary.json')); print('Accuracy:', data['metrics']['accuracy'])"
```

---

### Card 3: `specprove-sec` — Formal Z3 SMT Bounded Model Checker & Lean 4 Prover

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│ [REPOS] Pyhroff/specprove-sec         [LEAN 4] 13 Certificates        [Z3 SMT] 5.3    │
│ [DOMAINS] Formal Methods · k-Induction · CEGIS Synthesis · Interactive Theorem Proving  │
│ [ALIGNMENT] Primary: Resume_AI_Security_v5  |  Secondary: Resume_PQC_ZKP_Quantum_v5  │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

#### Social Preview Metadata
- **Repository Title:** `specprove-sec`
- **Short Description (150 chars):** Formal Z3 SMT bounded model checker, k-induction prover, and CEGIS guard synthesizer compiling machine-checked Lean 4 certificates for AI protocols.
- **Topics / Tags:** `formal-methods`, `z3-smt`, `k-induction`, `lean4`, `cegis`, `protocol-verification`
- **Badges:**
  ```markdown
  [![Lean 4](https://img.shields.io/badge/Lean_4-13_Certificates-darkgreen?style=flat-square)](https://github.com/Pyhroff/specprove-sec)
  [![Z3 SMT](https://img.shields.io/badge/SMT-Z3_k--Induction-orange?style=flat-square)](https://github.com/Pyhroff/specprove-sec)
  [![CEGIS](https://img.shields.io/badge/Synthesis-CEGIS_Guards-blue?style=flat-square)](https://github.com/Pyhroff/specprove-sec)
  ```

#### Core Architecture
```
Protocol Invariant Spec  I(s)  &  Transition Relation  T(s, a, s')
   │
   ▼
[Z3 SMT Bounded Model Checking (BMC)]
   ├── Check Base Case: I(s_0)
   ├── Unroll Transitions: ∧_{i=0}^{k-1} T(s_i, a_i, s_{i+1})
   └── Check Invariant Violation: ¬I(s_k)
   │
   ├── [SAT: Counterexample Found] ──► [CEGIS Synthesis Engine]
   │                                         │
   │                                         ▼ Synthesize Guard G(s, a)
   │                                     Re-prove Inductive Step:
   │                                     I(s) ∧ G(s, a) ∧ T(s, a, s') ⟹ I(s')
   │
   └── [UNSAT: Inductive Step Holds ∀ k] ──► Export Machine-Checked Lean 4 Certificate (.lean)
```

#### Empirical Benchmark Numbers
- **Protocols Verified:** 12 security protocols (`MCP-01` to `MCP-04`, `ZTA-01/02`, `CRYPTO-01`, `RAG-01`, `MEM-01`, `HITL-01`, `CLOUD-01`, `SAFE-01/02`).
- **Exploit Discovery:** Discovered concrete counterexamples for 10/10 vulnerable protocols in **149–321 ms** per protocol across 161 SMT queries.
- **Proof Guarantee:** **12/12 inductively proved** ($k$-induction) after automated CEGIS guard synthesis.
- **Formal Certificates:** **13 machine-checked Lean 4 certificates** generated in `lean_certs/`.

#### Verification Command
```bash
cd oss_contributions/specprove-sec
pytest tests/ -v
python -c "import json; data=json.load(open('reports/specprove-summary.json')); print('Total proved:', data['summary']['total_proved'])"
```

---

### Card 4: `ZeroTrace` — Pure x86_64 Direct Syscall Forensics & Active Directory Min-Cut

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│ [REPOS] Pyhroff/zerotrace             [DEPS] 0 AI Dependencies        [TESTS] 10/10   │
│ [DOMAINS] Direct Syscalls · Disk-vs-Memory Diffing · Edmonds-Karp · Sigma Deobfuscation│
│ [ALIGNMENT] Primary: Resume_RedTeam_v5 (Offense) | Primary: Resume_BlueTeam_v5 (Defense)│
└────────────────────────────────────────────────────────────────────────────────────────┘
```

#### Social Preview Metadata
- **Repository Title:** `ZeroTrace`
- **Short Description (150 chars):** Pure systems security: detects Hell's/Halo's Gate direct syscalls, severs 100% of Active Directory attack paths via min-cut, and deobfuscates CLI Sigma.
- **Topics / Tags:** `systems-security`, `direct-syscalls`, `active-directory`, `edmonds-karp`, `malware-forensics`, `zero-ai`
- **Badges:**
  ```markdown
  [![Direct Syscalls](https://img.shields.io/badge/Syscall_Hunter-100%25_Recall-red?style=flat-square)](https://github.com/Pyhroff/zerotrace)
  [![Min-Cut](https://img.shields.io/badge/AD_Tier--0-100%25_Severed-blue?style=flat-square)](https://github.com/Pyhroff/zerotrace)
  [![Sigma Boost](https://img.shields.io/badge/Sigma_Recall-35.7%25_%E2%86%92_100%25-brightgreen?style=flat-square)](https://github.com/Pyhroff/zerotrace)
  ```

#### Core Architecture
```
[Component 1: SyscallImplantHunter]
   Target PE .text Section in Memory  <─── Byte-by-Byte Diff ───>  ntdll.dll on Disk
   ├── Scans for Hell's Gate Stub: 4C 8B D1 B8 <SSN> 0F 05
   ├── Detects Halo's / Tartarus' Gate neighbor hook evasion (E9 rel32)
   └── Detects SysWhispers3 indirect trampoline jumps into ntdll.dll

[Component 2: ADAttackGraphEngine]
   BloodHound Enterprise Graph G = (V, E)
   ├── Source: Owned Principals S
   ├── Sink: Tier-0 Domain Controllers T
   └── Solves Exact Min-Cut via Edmonds-Karp Max-Flow: min \sum_{e \in C} c(e)

[Component 3: BehavioralEvasionEngine]
   Raw Telemetry CLI String ──► 5-Layer Deterministic Unpacker ──► Canonical Normalized Form
```

#### Empirical Benchmark Numbers
- **Syscall Implant Hunter:** **100.0% Recall (20/20) and 0.0% FPR (0/20) in 13.06 ms** across 40 memory regions.
- **Active Directory Min-Cut:** **100.0% of Tier-0 attack paths severed (180 to 0)** across 15 enterprise graphs in 6.09 ms by revoking only **7.15% (44/615)** remediable edges.
- **Behavioral Evasion Engine:** Boosts naive Sigma rule detection recall from **35.7% to 100.0% at 0.0% FPR** ($F_1 = 1.000$) across 40 telemetry test cases.

#### Verification Command
```bash
cd oss_contributions/zerotrace
pytest tests/ -v
python benchmarks/run_zerotrace_benchmarks.py
```

---

### Card 5: `Q-MIND` — Autonomous Quantum ML & Verifiable Circuit Compiler

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│ [REPOS] Pyhroff/Q-MIND                [TRIALS] 5,060 Verified         [TESTS] 172/172 │
│ [DOMAINS] Fault-Tolerant Quantum Compilation · QNG · Simulators · PennyLane · Qualtran│
│ [ALIGNMENT] Primary: Resume_PQC_ZKP_Quantum_v5 | Secondary: Resume_AI_Engineer_v5      │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

#### Social Preview Metadata
- **Repository Title:** `Q-MIND`
- **Short Description (150 chars):** Autonomous Quantum ML & verifiable compiler achieving 58.5% T-gate reduction with Gidney MBU, SelectSwap QROM, and 64-bit SIMD Kickmix verification.
- **Topics / Tags:** `quantum-computing`, `quantum-ml`, `circuit-optimization`, `t-gate-reduction`, `qualtran`, `pennylane`
- **Badges:**
  ```markdown
  [![T-Gate Reduction](https://img.shields.io/badge/T--Gate_Reduction-58.5%25-blueviolet?style=flat-square)](https://github.com/Pyhroff/Q-MIND)
  [![Trials](https://img.shields.io/badge/Verified_Trials-5,060-blue?style=flat-square)](https://github.com/Pyhroff/Q-MIND)
  [![Pytest](https://img.shields.io/badge/Pytest-172_passing-brightgreen?style=flat-square)](https://github.com/Pyhroff/Q-MIND)
  [![Verifier](https://img.shields.io/badge/Kickmix-486M_states%2Fs-orange?style=flat-square)](https://github.com/Pyhroff/Q-MIND)
  ```

#### Core Architecture
```
Quantum Circuit AST / Bloq Graph
   │
   ▼
[Kickmix Compilation Engine]
   ├── Gidney Measurement-Based Uncomputation (MBU: 4T compute / 0T uncompute)
   ├── Low-Chuang SelectSwap QROM Table Lookup (λ = 2^k)
   └── Commutative Phase-Polynomial T-Gate Fusion
   │
   ▼
[64-Bit SIMD Kickmix Equivalence Fuzz Verifier]
   ├── Bit-parallel truth table verification (0 bit mismatches, 0 ancilla leaks)
   └── Throughput: 486 Million gate-states/s
```

#### Empirical Benchmark Numbers
- **Compilation Gate Reduction:** **58.53% T-gate reduction**, **48.73% Toffoli reduction**, and **21.37% circuit depth reduction** across Fusion Energy ($1/\sqrt{x}$) and DQI ($\mathrm{GF}(2^m)$ Berlekamp-Massey).
- **Optimization Speedup:** Fubini-Study Riemannian Quantum Natural Gradient (QNG) achieved **5.3× speedup vs Adam** and **51.1% mean loss reduction**.
- **Barren Plateau Recovery:** Restored **13.6× gradient variance** at 8 qubits; Tri-mitigation suppressed NISQ noise degradation by **31.0%**.
- **Scale:** Evaluated over **5,060 verified trials** across 20 SQLite databases with 27 300-DPI publication figures.

#### Verification Command
```bash
python -c "
import sqlite3
db = sqlite3.connect('qmind_experiments.db')
cursor = db.cursor()
cursor.execute('SELECT COUNT(*) FROM experiments;')
print('Verified Q-MIND Experiment Runs:', cursor.fetchone()[0])
"
```

---

### Card 6: `kronos-kv` — Pure Distributed Raft & Bitcask LSM Storage Engine

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│ [REPOS] Pyhroff/kronos-kv             [DEPENDENCIES] 0 (Stdlib Only)  [TESTS] 8/8     │
│ [DOMAINS] Raft Consensus · Bitcask LSM · CRC32 Compaction · Kirsch-Mitzenmacher Bloom  │
│ [ALIGNMENT] Primary: Resume_SDE_v5                                                     │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

#### Social Preview Metadata
- **Repository Title:** `kronos-kv`
- **Short Description (150 chars):** Distributed Raft consensus and Bitcask LSM storage engine in pure Python stdlib: 84.3% disk compaction, 0.11ms reads, and 100% split-brain safety.
- **Topics / Tags:** `distributed-systems`, `raft-consensus`, `bitcask`, `lsm-tree`, `storage-engine`, `consistent-hashing`
- **Badges:**
  ```markdown
  [![Disk Reclaim](https://img.shields.io/badge/Bitcask_Compaction-84.3%25_Reclaimed-brightgreen?style=flat-square)](https://github.com/Pyhroff/kronos-kv)
  [![Latency](https://img.shields.io/badge/Point_Read-0.11_ms-blue?style=flat-square)](https://github.com/Pyhroff/kronos-kv)
  [![Raft Safety](https://img.shields.io/badge/Split--Brain-0%2F30_(100%25_Safe)-brightgreen?style=flat-square)](https://github.com/Pyhroff/kronos-kv)
  ```

#### Core Architecture
```
Write Request (k, v) ──► Append to Binary WAL (>IdII header) ──► Update KeyDir (offset, size)
                                                                       │
Read Request (k) ────► Consult Kirsch-Mitzenmacher Bloom Filter        │
                               │                                       ▼
                       Single File Seek: f.seek(offset) ◄─── O(1) KeyDir Index
```

#### Empirical Benchmark Numbers
- **Bitcask Disk Compaction:** **84.29% disk space reclaimed** (870,600 B $\rightarrow$ 136,800 B), with 800/800 live keys verified intact via hint file.
- **Point Read Latency:** **0.11 ms per read** (91.09 ms for 800 reads).
- **Bloom Filter Accuracy:** **0.00% false negatives and 0.19% empirical FPR** across 10,000 negative lookups.
- **Raft Consensus Safety:** **100.0% (30/30) split-brain prevention** and linearizable log convergence in 7.24 ms under asymmetric partitions ([2] vs [3]).
- **Consistent Hashing:** Remapped only **9.47% of keys** when expanding cluster from 8 to 9 nodes (approaching theoretical $1/N = 11.11\%$).

#### Verification Command
```bash
cd oss_contributions/kronos-kv
pytest tests/ -v
python benchmarks/run_benchmarks.py
```

---

### Card 7: `loopcheck` & `OSIRIS` — AI Agent Runtime & Waste Auditor

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│ [REPOS] Pyhroff/loopcheck & Pyhroff/osiris   [TESTS] 121 (loopcheck)  [LATENCY] 100s->10s│
│ [DOMAINS] AI Agent Loops · Trace Auditing · Token Waste · Groq Semantic Judge          │
│ [ALIGNMENT] Primary: Resume_AI_Engineer_v5  |  Secondary: Resume_SDE_v5              │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

#### Social Preview Metadata
- **Repository Title:** `loopcheck`
- **Short Description (150 chars):** Zero-instrumentation auditor for AI agent traces, detecting token waste, duplicate calls, tight loops, and stale retries with regression CI gating.
- **Topics / Tags:** `ai-agents`, `agent-auditing`, `waste-reduction`, `trace-analysis`, `groq-judge`
- **Badges:**
  ```markdown
  [![Pytest](https://img.shields.io/badge/Pytest-121_passing-brightgreen?style=flat-square)](https://github.com/Pyhroff/loopcheck)
  [![Regression CI](https://img.shields.io/badge/CI--Gating-fail--on--regression-blue?style=flat-square)](https://github.com/Pyhroff/loopcheck)
  ```

#### Core Architecture
```
Agent Execution JSON Trace
   │
   ▼
[TraceRecorder & Turn Parser] (Zero Token Double-Counting)
   │
   ├── Pattern 1: Duplicate Tool Calls Post-Success
   ├── Pattern 2: Tight Loop Thrashing (>4 consecutive identical actions)
   ├── Pattern 3: Stale Retry Loops (≥2 retries with unchanged error state)
   └── Pattern 4: Groq LLM Semantic Redundancy Judge
   │
   ▼
[Fleet Waste Rollup Report] ──► `--fail-on-regression` CI Exit
```

#### Empirical Benchmark Numbers
- **Test Coverage:** **121 passing tests** across 15 test suites in `loopcheck`.
- **Latency Optimization (OSIRIS):** Reduced local model latency from **100 s to 10 s** by replacing generic endpoints with native streaming adapter handling `think:false`.
- **Finding Suppression:** Configurable `--policy` suppressing intentional polling while halting on regression.

#### Verification Command
```bash
cd oss_contributions/loopcheck
pytest tests/ -v
python -m loopcheck.cli --help
```

---

### Card 8: `PromptStrike` — Automated Multi-Turn Adversarial Red Teaming & Defense Shield

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│ [REPOS] Pyhroff/promptstrike          [SUITE] PAIR / TAP / Crescendo / GCG [TESTS] 61/61│
│ [DOMAINS] Adversarial LLM Red Teaming · JailbreakBench · OWASP LLM Top 10 · Proxies   │
│ [ALIGNMENT] Primary: Resume_RedTeam_v5  |  Secondary: Resume_AI_Security_v5          │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

#### Social Preview Metadata
- **Repository Title:** `PromptStrike`
- **Short Description (150 chars):** Automated multi-turn adversarial red-teaming CLI implementing PAIR, TAP, Crescendo, and GCG jailbreaks with CI safety gates and transparent proxy defense.
- **Topics / Tags:** `adversarial-ml`, `red-teaming`, `jailbreak-attacks`, `owasp-llm`, `pair`, `tap`, `crescendo`, `gcg`
- **Badges:**
  ```markdown
  [![Attacks](https://img.shields.io/badge/Attacks-PAIR_|_TAP_|_Crescendo_|_GCG-red?style=flat-square)](https://github.com/Pyhroff/promptstrike)
  [![Judge](https://img.shields.io/badge/Judge-JailbreakBench_Calibrated-orange?style=flat-square)](https://github.com/Pyhroff/promptstrike)
  [![Pytest](https://img.shields.io/badge/Pytest-61_passing-brightgreen?style=flat-square)](https://github.com/Pyhroff/promptstrike)
  [![Defense Shield](https://img.shields.io/badge/Defense_Shield-10--Rule_Proxy-blue?style=flat-square)](https://github.com/Pyhroff/promptstrike)
  ```

#### Core Architecture
```
Adversarial Attacker (PAIR / TAP / Crescendo / GCG)
   │
   ▼
[Transparent Defense Shield Proxy]
   ├── Regex & Tokenizer Normalization Filter
   ├── 10-Rule Semantic Injection Classifier
   └── Fallback: Model Adapter Forwarding
   │
   ▼
[Multi-Model Inference Fleet]
   ├── Groq API (Llama 3.3 70B Versatile)
   ├── OpenAI API (GPT-4o)
   └── Ollama Local Host (Qwen 2.5 14B)
   │
   ▼
[Calibrated JailbreakBench 1-10 Judge] ──► ASR Regression CI Gate (Exit 0 or 1)
```

#### Empirical Benchmark Numbers
- **Algorithm Implementations:** 4 peer-reviewed jailbreak algorithms (PAIR, TAP, Crescendo, GCG).
- **Behavior Goal Set:** 50 standardized adversarial goals covering OWASP Top 10 for LLMs.
- **Defense Shield Latency:** < 2.5 ms transparent input inspection overhead.
- **Test Suite:** **61 passing offline unit and integration tests**.

#### Verification Command
```bash
cd oss_contributions/promptstrike
pytest tests/ -v
python -m promptstrike.cli attack --target groq --algorithm crescendo --goal 1
```

---

### Card 9: `ModelHawk` — Static AST Disassembler for Pickle Deserialization Exploits

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│ [REPOS] Pyhroff/ModelHawk             [DEPS] 0 (Python Stdlib Only)   [TESTS] 8/8     │
│ [DOMAINS] Model Supply Chain Security · Opcode Disassembly · PyTorch Weights · RCE    │
│ [ALIGNMENT] Primary: Resume_AI_Security_v5  |  Secondary: Resume_BlueTeam_v5          │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

#### Social Preview Metadata
- **Repository Title:** `ModelHawk`
- **Short Description (150 chars):** Pure stdlib static analyzer detecting pickle deserialization arbitrary code execution in PyTorch models without loading untrusted weights into memory.
- **Topics / Tags:** `supply-chain-security`, `model-scanning`, `pickle-disassembly`, `pytorch-security`, `zero-trust`
- **Badges:**
  ```markdown
  [![Dependencies](https://img.shields.io/badge/Dependencies-Zero_(Stdlib_Only)-blue?style=flat-square)](https://github.com/Pyhroff/ModelHawk)
  [![Pytest](https://img.shields.io/badge/Pytest-8_passing-brightgreen?style=flat-square)](https://github.com/Pyhroff/ModelHawk)
  [![Safety](https://img.shields.io/badge/Execution_Risk-Zero_(No_pickle.load)-brightgreen?style=flat-square)](https://github.com/Pyhroff/ModelHawk)
  ```

#### Core Architecture
```
Untrusted PyTorch Checkpoint (.pt / .bin / .pth)
   │
   ▼
[Raw Byte Stream Reader]
   │
   ▼
[pickletools.genops Tokenizer Stream]
   ├── Disassembles Opcode Instructions (REDUCE, GLOBAL, BUILD, INST, OBJ)
   ├── Reconstructs Callable Identity (posix.system, subprocess.Popen, builtins.eval)
   └── Validates Safety Policy: Allow ONLY PyTorch Tensor Reconstructors
   │
   ├── [SAFE] ──► Return Exit Code 0 (Model Verified Safe to Load)
   └── [MALICIOUS] ──► Return Exit Code 1 & Quarantine Report (Zero RCE Risk)
```

#### Empirical Benchmark Numbers
- **Safety Invariant:** 0% code execution probability; models are never parsed using `torch.load()` or `pickle.load()`.
- **Opcode Coverage:** Detects all standard pickle exploit chains including `__reduce__`, `__reduce_ex__`, and custom global imports.
- **Test Harness:** 8/8 tests passing, with reproducible benign and malicious PyTorch fixture generators.

#### Verification Command
```bash
cd oss_contributions/ModelHawk
pytest tests/ -v
python modelhawk.py scan --path fixtures/malicious_sample.pt
```

---

### Card 10: `DarkDecoder` — AI Threat Intelligence & Dual MITRE ATT&CK/ATLAS Platform

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│ [REPOS] Pyhroff/darkdecoder           [FRAMEWORKS] ATT&CK + ATLAS     [INTEG] JSON-LD │
│ [DOMAINS] Cyber Threat Intelligence · Kill Chain Synthesis · CTI Grounding · LLM Evals │
│ [ALIGNMENT] Primary: Resume_BlueTeam_v5  |  Secondary: Resume_RedTeam_v5              │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

#### Social Preview Metadata
- **Repository Title:** `DarkDecoder`
- **Short Description (150 chars):** Automated CTI platform mapping multi-stage adversary campaigns to MITRE ATT&CK & ATLAS matrices with grounded LLM reasoning and kill-chain synthesis.
- **Topics / Tags:** `threat-intelligence`, `mitre-attack`, `mitre-atlas`, `kill-chain`, `cti-grounding`, `ioc-extraction`
- **Badges:**
  ```markdown
  [![Framework](https://img.shields.io/badge/Matrices-ATT%26CK_+_ATLAS-red?style=flat-square)](https://github.com/Pyhroff/darkdecoder)
  [![Grounding](https://img.shields.io/badge/Hallucination_Guard-100%25_Grounded-brightgreen?style=flat-square)](https://github.com/Pyhroff/darkdecoder)
  [![Export](https://img.shields.io/badge/Export-Navigator_JSON_&_JSON--LD-orange?style=flat-square)](https://github.com/Pyhroff/darkdecoder)
  ```

#### Core Architecture
```
Unstructured Threat Bulletins & Dark Web Feeds
   │
   ▼
[Regex & Named Entity IOC Extractor] (Hashes, IPs, Domains, File Paths, Registry Keys)
   │
   ▼
[Dual Matrix Normalizer & Classifier]
   ├── Enterprise IT: MITRE ATT&CK (Initial Access, Persistence, Command & Control)
   └── Adversarial ML: MITRE ATLAS (Reconnaissance, Resource Dev, Evasion, Exfiltration)
   │
   ▼
[Grounded Kill-Chain Reconstruction Engine]
   └── Invariant: Blocks Invented Techniques Absent from Raw Evidence Corpus
   │
   ▼
Structured Attack Layer Export (MITRE ATT&CK Navigator JSON)
```

#### Empirical Benchmark Numbers
- **Technique Coverage:** Maps across 14 enterprise ATT&CK tactic categories and 12 ATLAS adversary machine learning tactics.
- **Grounding Veracity:** 100% of asserted TTP nodes tied to byte-offset spans in source threat intelligence documents.

#### Verification Command
```bash
cd oss_contributions/darkdecoder
pytest tests/ -v
python -m darkdecoder.cli ingest --report samples/apt_report.txt
```

---

## PART II: UPSTREAM OPEN-SOURCE CONTRIBUTION CARDS

---

### Contribution 1: `tobymao/sqlglot` (PR #8780 Merged)
- **Repository:** [`tobymao/sqlglot`](https://github.com/tobymao/sqlglot)
- **PR Link:** [PR #8780](https://github.com/tobymao/sqlglot/pull/8780)
- **Status:** 🟣 **MERGED by Founder Toby Mao**
- **Category:** Compilers & Transpiler Internals
- **Problem Statement:** In `sqlglot/parser.py::_replace_lambda`, transpiling higher-order functions with multi-argument lambdas mutated shared AST `DataType` nodes by reference, causing silent downstream optimizer corruptions.
- **Surgical Mechanism:** Replaced shared reference with `.copy()` on the AST node (`exp.Cast(this=arg, to=data_type.copy())`). Zero deepcopy overhead.
- **Test Impact:** Passed all 9 dialect test suites without breaking AST invariants.

---

### Contribution 2: `BerriAI/litellm` (PR #47091 Merged, PR #47312 Open, PR #47311 Open, PR #47105 Open, Commit 846d37e8)
- **Repository:** [`BerriAI/litellm`](https://github.com/BerriAI/litellm)
- **PR Links:**
  - [PR #47091](https://github.com/BerriAI/litellm/pull/47091) (Merged): Standardized Cohere `stop` parameter to array format.
  - [PR #47312](https://github.com/BerriAI/litellm/pull/47312) (Open): Fixed Broken Function Level Authorization (BFLA) scoping `/v1/mcp/access_groups` to caller-authorized servers, mitigating cross-tenant server enumeration (CVSS 7.5).
  - [PR #47311](https://github.com/BerriAI/litellm/pull/47311) (Open): Enforced authorization checks on `budget_duration` and `budget_id` updates in `/key/update` to block spend limit tampering.
  - [PR #47105](https://github.com/BerriAI/litellm/pull/47105) (Open): Fixed BOLA bypass in `can_object_call_model()` where empty `models: []` list was treated as an unrestricted wildcard.
  - [Commit `846d37e8`](https://github.com/BerriAI/litellm): Remediated fail-open MCP tool resolution on non-hyphenated dictionary inputs; verified with Z3 SMT and proved safe in Lean 4 (`lean_certs/MCP_04.lean`).
- **Status:** 🟣 **Merged (PR #47091)** · 🟢 **Open Under Review (PR #47312, #47311, #47105)** · 🟢 **Committed & Verified (Commit 846d37e8)**
- **Category:** AI Gateway Security, Access Control & Formal Methods

---

### Contribution 3: `quantumlib/Qualtran` (PR #1986 Open) & `PennyLaneAI/pennylane` (PR #10391 Open)
- **Repositories:** [`quantumlib/Qualtran`](https://github.com/quantumlib/Qualtran) · [`PennyLaneAI/pennylane`](https://github.com/PennyLaneAI/pennylane)
- **PR Links:**
  - [Qualtran PR #1986](https://github.com/quantumlib/Qualtran/pull/1986): Fixed fault-tolerant Cuccaro adder `Add.build_call_graph` CNOT and T-gate estimation formulas for unequal register bit sizes ($a \ne b$) (#1818).
  - [PennyLane PR #10391](https://github.com/PennyLaneAI/pennylane/pull/10391): Registered Hamiltonian Evolution operator PyTree leaves and fixed `bind_new_parameters` dispatch, resolving JIT autodiff parameter-shift tracing crashes (#6514).
- **Status:** 🟢 **OPEN (In Review)**
- **Category:** Fault-Tolerant Quantum Algorithms & Automatic Differentiation

---

### Contribution 4: `PrefectHQ/fastmcp` (PR #6063 Open)
- **Repository:** [`PrefectHQ/fastmcp`](https://github.com/PrefectHQ/fastmcp)
- **PR Link:** [PR #6063](https://github.com/PrefectHQ/fastmcp/pull/6063)
- **Status:** 🟢 **OPEN (65/65 CI Passing)**
- **Category:** Agent Sandbox Security (CWE-653, CWE-400)
- **Problem Statement:** In `MontySandboxProvider` and `CodeMode`, guest Python code instruction counts were bounded inside the microVM, but external host callbacks escaped CPU counters, allowing host resource starvation.
- **Surgical Mechanism:** Added `wall_clock_timeout_secs` and `max_external_calls` budget caps with fail-closed cancellation.

---

### Contribution 5: `sqlfluff/sqlfluff` (PR #8900 Approved, PR #8899 Verified, PR #8901, PR #8902)
- **Repository:** [`sqlfluff/sqlfluff`](https://github.com/sqlfluff/sqlfluff)
- **PR Links:** [PR #8900](https://github.com/sqlfluff/sqlfluff/pull/8900) · [PR #8899](https://github.com/sqlfluff/sqlfluff/pull/8899) · [PR #8901](https://github.com/sqlfluff/sqlfluff/pull/8901) · [PR #8902](https://github.com/sqlfluff/sqlfluff/pull/8902)
- **Status:** 🟢 **APPROVED LGTM (Danny Jones)** · 🟢 **VERIFIED (by Duo-ee)** · 🟢 **OPEN (In Review)**
- **Category:** SQL Parser Grammar & Dialect AST
- **Problem Statement:** Added `FORMATS` and `POLICIES` unreserved keywords to `AccessSchemaPluralObjectSegment`; fixed StarRocks fixed-range partition comma syntax using `Ref("CommaSegment")`. 57 dialect tests pass cleanly.

---

### Contribution 6: `crewAIInc/crewAI` (PRs #8240, #8242, #8243, #8244, #8245)
- **Repository:** [`crewAIInc/crewAI`](https://github.com/crewAIInc/crewAI)
- **PR Links:** [PR #8240](https://github.com/crewAIInc/crewAI/pull/8240) · [PR #8242](https://github.com/crewAIInc/crewAI/pull/8242) · [PR #8243](https://github.com/crewAIInc/crewAI/pull/8243) · [PR #8244](https://github.com/crewAIInc/crewAI/pull/8244) · [PR #8245](https://github.com/crewAIInc/crewAI/pull/8245)
- **Status:** 🟢 **OPEN (In Review)**
- **Category:** Multi-Agent Framework State, Resilience & Tooling
- **Problem Statement:** Added `nextCursor` pagination across MCP tools; preserved upstream task state during guardrail retries; fixed `suppress_logging()` context hygiene; decoded Redis URL percent-encoded passwords.

---

### Contribution 7: `microsoft/presidio` (PR #2418 Open)
- **Repository:** [`microsoft/presidio`](https://github.com/microsoft/presidio)
- **PR Link:** [PR #2418](https://github.com/microsoft/presidio/pull/2418)
- **Status:** 🟢 **OPEN (In Review)**
- **Category:** Security Documentation & Container Deployment
- **Problem Statement:** Updated container port mapping in documentation from `-p 5001:5001` to `-p 5001:3000` to align host publishing with internal Gunicorn binding.

---

### Contribution 8: `graphql-python/graphene` (Branch feat/lazy-connection-node)
- **Repository:** [`graphql-python/graphene`](https://github.com/graphql-python/graphene)
- **Status:** 🟢 **COMMITTED (Tested)**
- **Category:** Frameworks & Schema Deadlock Prevention
- **Problem Statement:** Implemented lazy type references for `Connection.Meta.node` (#1600), resolving circular import deadlocks in complex Relay schemas.
