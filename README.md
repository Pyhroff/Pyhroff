<div align="center">

# Praising Harris Ratnam
### AI Systems Security Researcher & Runtime Defense Engineer
**B.Tech CSE (Cybersecurity), IIIT Kottayam** · *Target: AI Systems / Security / Agent Engineering Internship*

[![GitHub Profile](https://img.shields.io/badge/GitHub-Pyhroff-181717?style=flat-square&logo=github)](https://github.com/Pyhroff)
[![Security Advisories](https://img.shields.io/badge/Advisories-Repository-critical?style=flat-square&logo=github)](https://github.com/Pyhroff/security-advisories)
[![Latest Research Release](https://img.shields.io/badge/Release-v2026.10.1-blue?style=flat-square&logo=github)](https://github.com/Pyhroff/security-advisories/releases/tag/v2026.10.1)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Praising_Harris-0A66C2?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/praising-harris-8a3320330)
[![Email](https://img.shields.io/badge/Email-praisingharris%40gmail.com-D14836?style=flat-square&logo=gmail)](mailto:praisingharris@gmail.com)

</div>

---

### 🛡️ Verified Vulnerability Disclosures & Upstream Contributions

Authored upstream security advisories, vulnerability patches, and runtime fixes for production AI infrastructure:

| Project | Pull Request / Advisory | Severity / Impact | Target Component | Status |
|---|---|:---:|---|:---:|
| **LiteLLM** | [PR #47105](https://github.com/BerriAI/litellm/pull/47105) | **CVSS 7.5 (High)** | BOLA Access Control Bypass with Empty Models List (`auth_checks.py`) | **Submitted** |
| **FastMCP** | [PR #5786](https://github.com/PrefectHQ/fastmcp/pull/5786) | **Medium** | Converted malformed port `ValueError` to `SSRFError` in `validate_url` to stop 500 crashes | **Submitted** |
| **CrewAI** | [PR #8245](https://github.com/crewAIInc/crewAI/pull/8245) | **Medium** | Preserved universal newlines across Unicode line breaks in tool artifacts | **Submitted** |
| **CrewAI** | [PR #8244](https://github.com/crewAIInc/crewAI/pull/8244) | **Medium** | Decoded percent-encoded passwords in `REDIS_URL` for A2A cache | **Submitted** |
| **CrewAI** | [PR #8243](https://github.com/crewAIInc/crewAI/pull/8243) | **Medium** | Restored configured logger levels & preserved `NOTSET` hierarchy on errors | **Submitted** |
| **CrewAI** | [PR #8242](https://github.com/crewAIInc/crewAI/pull/8242) | **Medium** | Preserved upstream dependent task context during guardrail retry loops | **Submitted** |
| **CrewAI** | [PR #8240](https://github.com/crewAIInc/crewAI/pull/8240) | **Medium** | Fixed native MCP pagination cursor handling (`nextCursor` / `next_cursor`) | **Submitted** |
| **LiteLLM** | [PR #47107](https://github.com/BerriAI/litellm/pull/47107) | **Medium** | Fixed silent dropping of `model_names` when `model_ids` is supplied | **Submitted** |
| **LiteLLM** | [PR #47106](https://github.com/BerriAI/litellm/pull/47106) | **Medium** | Excluded `budget_id` from entity updates to prevent duplicate kwarg 500 crashes | **Submitted** |
| **LiteLLM** | [PR #47097](https://github.com/BerriAI/litellm/pull/47097) | **Medium** | Fixed router image generation failure callbacks (Langfuse, OTel) | **Submitted** |
| **LiteLLM** | [PR #47091](https://github.com/BerriAI/litellm/pull/47091) | **Low** | Fixed Cohere chat API string stop sequences dropping | **Submitted** |
| **FastMCP** | [PYHROFF-ADV-2026-002](https://github.com/Pyhroff/security-advisories/blob/main/GHSA_FASTMCP_SANDBOX_AUDIT.md) | **CVSS 5.3 (Med)** | Async Monty sandbox boundary analysis & host-side callback decoupling | **Audited** |

---

### 📄 Featured Open-Source Projects & Tooling

```
  ┌────────────────────────────────────────────────────────────────────────┐
  │                           AI SECURITY SUITE                            │
  ├──────────────────────────────────┬─────────────────────────────────────┤
  │  aisec-suite / mcpaudit          │  promptstrike                       │
  │  AST scanner for MCP & agents    │  Automated LLM Red-Teaming CLI      │
  ├──────────────────────────────────┼─────────────────────────────────────┤
  │  ModelHawk                       │  loopcheck / osiris                 │
  │  PyTorch backdoor AST scanner    │  Agent loop waste auditor & runtime │
  └──────────────────────────────────┴─────────────────────────────────────┘
```

* **[aisec-suite](https://github.com/Pyhroff/aisec-suite)** *(Specialist Scanners: [mcpaudit](https://github.com/Pyhroff/mcpaudit), [memsentry](https://github.com/Pyhroff/memsentry), [ragsentry](https://github.com/Pyhroff/ragsentry), [trainsentry](https://github.com/Pyhroff/trainsentry))*  
  *Unified CLI and CI gate for AI application security, generating SARIF reports and policy baselines across agent runtimes, MCP servers, and context memory.*
* **[PromptStrike](https://github.com/Pyhroff/promptstrike)**  
  *Automated adversarial red-teaming CLI for LLMs — PAIR/TAP/Crescendo jailbreak algorithms, live dashboard, multi-model sweep comparison, and CI/CD safety gate.*
* **[ModelHawk](https://github.com/Pyhroff/ModelHawk)**  
  *Static AST-based analyzer detecting code-execution backdoors (pickle-deserialization RCE) in PyTorch/pickle ML model files without loading weights.*
* **[loopcheck](https://github.com/Pyhroff/loopcheck)**  
  *Zero-instrumentation waste auditor for agent loops — analyze, compare, and report on wasted tool calls without any SDK integration or OTel collector.*
* **[OSIRIS](https://github.com/Pyhroff/osiris)**  
  *Model-agnostic agent runtime with provider failover (Gemini/Groq/Ollama/OpenAI), persistent vector memory, and developer integrations.*
* **[specprove-sec](https://github.com/Pyhroff/specprove-sec)**  
  *Formal Z3 SMT Bounded Model Checker, Unbounded k-Induction Prover, Counterexample Exploit Synthesizer & Lean 4 Proof Certificate Exporter for Agentic (MCP) Protocols.*
* **[pqc-scanner](https://github.com/Pyhroff/pqc-scanner)**  
  *Static analyzer detecting quantum-vulnerable cryptography (RSA/ECC) across Python, Java, JS, and Go with NIST FIPS 203/204/205 post-quantum migration advice.*

---

### 🔬 Engineering Philosophy

$$\text{Threat Model} \longrightarrow \text{AST / Formal Analysis} \longrightarrow \text{Exploit Harness} \longrightarrow \text{Regression Test} \longrightarrow \text{Upstream PR}$$

- **Defense-in-Depth**: I evaluate systems assuming the model layer is inherently untrusted. Security boundaries must live in the host process, AST parser, and kernel/sandbox isolation layer.
- **Empirical Rigor**: Prefer controlled regression test suites and verified reproductions over hand-wavy claims.

---

### 🛠️ Technical Arsenal

- **Languages:** Python (Advanced AST/Asyncio), Go, C/C++, Rust, TypeScript, Bash  
- **AI Infrastructure:** LiteLLM, CrewAI, LangGraph, Model Context Protocol (MCP), vLLM, Ollama  
- **Security & Systems:** Linux Namespaces/cgroups, Docker, E2B Sandboxes, Z3 SMT Theorem Prover, Lean 4, SARIF, OpenTelemetry, MITRE ATT&CK & ATLAS  
- **Cloud & Databases:** AWS, GCP, Redis, PostgreSQL, SQLite, Neo4j  

---

### 📬 Connect With Me

- **Email:** [praisingharris@gmail.com](mailto:praisingharris@gmail.com)  
- **LinkedIn:** [linkedin.com/in/Praising_Harris](https://www.linkedin.com/in/Praising_Harris)  
- **Security Advisories:** [github.com/Pyhroff/security-advisories](https://github.com/Pyhroff/security-advisories)
