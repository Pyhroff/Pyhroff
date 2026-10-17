# Praising Harris Ratnam
**AI Security Researcher & Systems Engineer**  
B.Tech CSE (Cybersecurity), IIIT Kottayam · Availability: Remote (from 14 Nov 2026)  
[GitHub Profile](https://github.com/Pyhroff) · [Security Advisories Repo](https://github.com/Pyhroff/security-advisories) · [LinkedIn](https://www.linkedin.com/in/Praising_Harris) · [Email](mailto:praisingharris@gmail.com)

---

### 🛡️ Verified Vulnerability Disclosures & Upstream Contributions

Authored upstream security advisories, vulnerability patches, and runtime fixes for production AI infrastructure:

| Project / Target | PR / Advisory | Type / Vulnerability | Status |
|---|---|---|:---:|
| **CrewAI** | [PR #8245](https://github.com/crewAIInc/crewAI/pull/8245) | Preserved universal newlines across Unicode line separators in tool result artifacts | **Submitted** |
| **CrewAI** | [PR #8244](https://github.com/crewAIInc/crewAI/pull/8244) | Decoded percent-encoded passwords in `REDIS_URL` for A2A task cache | **Submitted** |
| **CrewAI** | [PR #8243](https://github.com/crewAIInc/crewAI/pull/8243) | Restored configured logger levels & preserved `NOTSET` hierarchy on errors | **Submitted** |
| **CrewAI** | [PR #8242](https://github.com/crewAIInc/crewAI/pull/8242) | Preserved upstream dependent task context during guardrail retry loops | **Submitted** |
| **CrewAI** | [PR #8240](https://github.com/crewAIInc/crewAI/pull/8240) | Fixed native MCP pagination cursor handling (`nextCursor` / `next_cursor`) | **Submitted** |
| **LiteLLM** | [PR #47107](https://github.com/BerriAI/litellm/pull/47107) | Fixed `/access_group/new` silently dropping `model_names` when `model_ids` sent | **Submitted** |
| **LiteLLM** | [PR #47106](https://github.com/BerriAI/litellm/pull/47106) | Fixed duplicate `budget_id` 500 error in entity updates | **Submitted** |
| **LiteLLM** | [PR #47105](https://github.com/BerriAI/litellm/pull/47105) | **BOLA Security Advisory (CVSS 7.5)**: Access control bypass with empty model list | **Submitted** |
| **LiteLLM** | [PR #47097](https://github.com/BerriAI/litellm/pull/47097) | Fixed image generation failure callback dispatches (Langfuse, OTel) | **Submitted** |
| **LiteLLM** | [PR #47091](https://github.com/BerriAI/litellm/pull/47091) | Fixed Cohere chat API string stop sequences dropping | **Submitted** |
| **FastMCP** | [PYHROFF-ADV-2026-002](https://github.com/Pyhroff/security-advisories/blob/main/GHSA_FASTMCP_SANDBOX_AUDIT.md) | Async sandbox boundary analysis & host-side event decoupling | **Audited** |

---

### 📄 Empirical Security Research & Tooling

* **[The 2026 State of Model Context Protocol (MCP) Security](https://github.com/Pyhroff/security-advisories/blob/main/THE_2026_STATE_OF_MCP_SECURITY.md)**  
  *Comprehensive empirical vulnerability audit of 90 public MCP servers, mapping CWE-78 subshell hazards, schema poisoning attacks, and runtime sandbox boundaries to MITRE ATLAS.*
* **[MCP Security Auditor (`mcp_security_auditor.py`)](https://github.com/Pyhroff/security-advisories/blob/main/mcp_security_auditor.py)**  
  *Static AST-based vulnerability analyzer detecting unsafe deserialization (CWE-502), subshell command injection (CWE-78), dynamic evaluation (CWE-95), and parameter traversal (CWE-22).*
* **[aisec-suite](https://github.com/Pyhroff/aisec-suite)**  
  *Unified CLI and CI gate for AI application security, generating SARIF reports and policy baselines across agent runtimes, MCP servers, and context memory.*
* **[specprove-sec](https://github.com/Pyhroff/specprove-sec)**  
  *Formal Z3 SMT Bounded Model Checker & Lean 4 Proof Certificate Exporter for Agentic (MCP) & Zero-Trust Security Protocols.*
* **[pqc-scanner](https://github.com/Pyhroff/pqc-scanner)**  
  *Static analyzer detecting quantum-vulnerable cryptography (RSA/ECC) across Python, Java, JS, and Go with NIST FIPS 203/204/205 post-quantum remediation advice.*

---

### 🔬 Methodology & Core Stack

**Threat Model → AST/Symbolic Analysis → Exploit Harness → Regression Test → Upstream PR**

- **Languages:** Python, Go, C/C++, Rust, TypeScript, Bash  
- **Domains:** AI Agent Security, Runtime Sandboxing (E2B / Monty / Docker), MCP Protocol, Vulnerability Research, Formal Verification (Z3 / Lean 4), Post-Quantum Cryptography (NIST FIPS 203/204/205)  
- **Frameworks & Observability:** FastAPI, LiteLLM, CrewAI, LangGraph, OpenTelemetry, SARIF, Docker  

---

### 📬 Get In Touch

- **Email:** [praisingharris@gmail.com](mailto:praisingharris@gmail.com)  
- **LinkedIn:** [linkedin.com/in/Praising_Harris](https://www.linkedin.com/in/Praising_Harris)  
- **Security Advisories:** [github.com/Pyhroff/security-advisories](https://github.com/Pyhroff/security-advisories)  
