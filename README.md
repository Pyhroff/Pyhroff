<div align="center">

# Praising Harris Ratnam
### AI Systems Security Researcher & Runtime Defense Engineer
**B.Tech CSE (Cybersecurity), IIIT Kottayam** · *Target: Winter Internship (Available 14 Nov 2026)*

[![GitHub Profile](https://img.shields.io/badge/GitHub-Pyhroff-181717?style=flat-square&logo=github)](https://github.com/Pyhroff)
[![Security Advisories](https://img.shields.io/badge/Advisories-Repository-critical?style=flat-square&logo=github)](https://github.com/Pyhroff/security-advisories)
[![Latest Research Release](https://img.shields.io/badge/Release-v2026.10.1-blue?style=flat-square&logo=github)](https://github.com/Pyhroff/security-advisories/releases/tag/v2026.10.1)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Praising_Harris-0A66C2?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/Praising_Harris)
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

### 📄 Empirical Security Research & Tooling

```
  ┌────────────────────────────────────────────────────────────────────────┐
  │                           AI SECURITY SUITE                            │
  ├──────────────────────────────────┬─────────────────────────────────────┤
  │  mcp_security_auditor.py         │  specprove-sec                      │
  │  AST scanner for MCP tools       │  Formal Z3 SMT Bounded Checker      │
  ├──────────────────────────────────┼─────────────────────────────────────┤
  │  THE 2026 STATE OF MCP SECURITY  │  pqc-scanner                        │
  │  Empirical 90-server paper       │  NIST FIPS 203/204/205 PQC scanner  │
  └──────────────────────────────────┴─────────────────────────────────────┘
```

* **[The 2026 State of Model Context Protocol (MCP) Security](https://github.com/Pyhroff/security-advisories/blob/main/THE_2026_STATE_OF_MCP_SECURITY.md)**  
  *Comprehensive empirical vulnerability audit of 90 public MCP servers, mapping CWE-78 subshell hazards, schema poisoning attacks, and runtime sandbox boundaries to MITRE ATLAS.*
* **[MCP Security Auditor (`mcp_security_auditor.py`)](https://github.com/Pyhroff/security-advisories/blob/main/mcp_security_auditor.py)**  
  *Static AST-based vulnerability analyzer detecting unsafe deserialization (CWE-502), subshell command injection (CWE-78), dynamic evaluation (CWE-95), and path traversal (CWE-22).*
* **[specprove-sec](https://github.com/Pyhroff/specprove-sec)**  
  *Formal Z3 SMT Bounded Model Checker, Unbounded k-Induction Prover, Counterexample Exploit Synthesizer & Lean 4 Proof Certificate Exporter for Agentic (MCP) & Zero-Trust Security Protocols.*
* **[aisec-suite](https://github.com/Pyhroff/aisec-suite)**  
  *Unified CLI and CI gate for AI application security, generating SARIF reports and policy baselines across agent runtimes, MCP servers, and context memory.*
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
