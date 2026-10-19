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

### 🛡️ Verified Vulnerability Disclosures & Upstream Contributions (20+ Patches & Advisories)

Authored upstream security advisories, vulnerability patches, and runtime defense fixes across production AI infrastructure (`BerriAI/litellm`, `PrefectHQ/fastmcp`, `crewAIInc/crewAI`):

| Project | Pull Request / Advisory | Severity / Impact | Target Component | Status |
|---|---|:---:|---|:---:|
| **LiteLLM** | [PR #47105](https://github.com/BerriAI/litellm/pull/47105) | **CVSS 7.5 (High)** | BOLA Access Control Bypass with Empty Models List (`auth_checks.py`) | **Submitted** |
| **LiteLLM** | [PR #47119](https://github.com/BerriAI/litellm/compare/main...Pyhroff:litellm:fix/allow-requests-db-unavailable-unconfigured-db?expand=1) | **CVSS 7.5 (High)** | Fail-Open Prevention: Reject Unauthorized Calls on Unconfigured DB (`user_api_key_auth.py`) | **Tested & Synced** |
| **LiteLLM** | [PR #46916](https://github.com/BerriAI/litellm/compare/main...Pyhroff:litellm:fix/key-budget-duration-tier-auth?expand=1) | **CVSS 6.5 (Med)** | Budget Reset & Tier Escalation Prevention on Key Update (`key_management_endpoints.py`) | **Tested & Synced** |
| **LiteLLM** | [PR #47005](https://github.com/BerriAI/litellm/compare/main...Pyhroff:litellm:fix/tag-new-atomic-deployment-validation?expand=1) | **Medium** | Pre-Validate Model Deployments & Atomic Rollback in `/tag/new` (`tag_management_endpoints.py`) | **Tested & Synced** |
| **LiteLLM** | [PR #46913](https://github.com/BerriAI/litellm/compare/main...Pyhroff:litellm:fix/mcp-debug-restricted-caller-headers?expand=1) | **CVSS 5.3 (Med)** | Restrict Outbound MCP Debug Headers & Upstream Auth to Proxy Admins | **Tested & Synced** |
| **LiteLLM** | [PR #46912](https://github.com/BerriAI/litellm/compare/main...Pyhroff:litellm:fix/mcp-access-groups-caller-scope?expand=1) | **CVSS 4.3 (Med)** | Restrict MCP Access Group Enumeration to Caller-Authorized Servers | **Tested & Synced** |
| **LiteLLM** | [PR #46664](https://github.com/BerriAI/litellm/compare/main...Pyhroff:litellm:fix/mcp-byok-tools-list-per-request-header?expand=1) | **Medium** | BYOK Per-Request Authorization Header Propagation in MCP `tools/list` | **Tested & Synced** |
| **LiteLLM** | [PR #47011](https://github.com/BerriAI/litellm/compare/main...Pyhroff:litellm:fix/key-gen-spend-routes-enterprise-error?expand=1) | **Medium** | Structured 403 License Error vs 500 Crash on Non-Enterprise Spend Routes | **Tested & Synced** |
| **LiteLLM** | [PR #46847](https://github.com/BerriAI/litellm/compare/main...Pyhroff:litellm:fix/extra-header-tags-case-insensitive?expand=1) | **Medium** | RFC 7230/9110 Case-Insensitive Header Lookup for Extra Spend Tracking Tags | **Tested & Synced** |
| **LiteLLM** | [PR #47258](https://github.com/BerriAI/litellm/compare/main...Pyhroff:litellm:fix/aiohttp-openai-service-tier?expand=1) | **Low** | Provider `service_tier` Metric Propagation onto `ModelResponse` | **Tested & Synced** |
| **LiteLLM** | [PR #47107](https://github.com/BerriAI/litellm/pull/47107) | **Medium** | Dual Support & Deduplication for `model_names` and `model_ids` in Access Groups | **Submitted** |
| **LiteLLM** | [PR #47106](https://github.com/BerriAI/litellm/pull/47106) | **Medium** | Exclude `budget_id` from Entity Updates to Prevent Duplicate Kwarg Crash | **Passed (88/88 CI)** |
| **LiteLLM** | [PR #47097](https://github.com/BerriAI/litellm/pull/47097) | **Medium** | Router Image Generation Failure Callback Dispatching (Langfuse, OTel) | **Submitted** |
| **LiteLLM** | [PR #47091](https://github.com/BerriAI/litellm/pull/47091) | **Low** | Cohere Chat Completion String Stop Sequence Normalization | **Passed (88/88 CI)** |
| **FastMCP** | [PR #5786](https://github.com/PrefectHQ/fastmcp/pull/5786) | **Medium** | Converted Malformed Port `ValueError` to `SSRFError` in `validate_url` to Stop 500 Crashes | **Submitted** |
| **FastMCP** | [PYHROFF-ADV-2026-002](https://github.com/Pyhroff/security-advisories/blob/main/GHSA_FASTMCP_SANDBOX_AUDIT.md) | **CVSS 5.3 (Med)** | Async Monty Sandbox Boundary Analysis & Host-Side Callback Decoupling | **Audited** |
| **CrewAI** | [PR #8245](https://github.com/crewAIInc/crewAI/pull/8245) | **Medium** | Universal Newline Preservation Across Unicode Line Breaks in Tool Artifacts | **Submitted** |
| **CrewAI** | [PR #8244](https://github.com/crewAIInc/crewAI/pull/8244) | **Medium** | Decoded Percent-Encoded Passwords in `REDIS_URL` for A2A Cache | **Submitted** |
| **CrewAI** | [PR #8243](https://github.com/crewAIInc/crewAI/pull/8243) | **Medium** | Restored Configured Logger Levels & Preserved `NOTSET` Hierarchy on Errors | **Submitted** |
| **CrewAI** | [PR #8242](https://github.com/crewAIInc/crewAI/pull/8242) | **Medium** | Preserved Upstream Dependent Task Context During Guardrail Retry Loops | **Submitted** |
| **CrewAI** | [PR #8240](https://github.com/crewAIInc/crewAI/pull/8240) | **Medium** | Native MCP Pagination Cursor Handling (`nextCursor` / `next_cursor`) | **Submitted** |

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
