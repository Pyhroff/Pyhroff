# Praising Harris Ratnam

**AI security · agentic AI engineering** — B.Tech CSE (Cybersecurity), IIIT Kottayam

I build static scanners and evaluation harnesses for the attack surfaces of LLM agents: MCP tool definitions, agent memory files, RAG corpora and fine-tuning datasets. I measure them on real-world data and report the precision numbers, including the unflattering ones.

📫 praisingharris@gmail.com · [LinkedIn](https://www.linkedin.com/in/praising-harris-8a3320330)

---

### Featured work

**[mcp-scan-study](https://github.com/Pyhroff/mcp-scan-study)** — an empirical evaluation of my own MCP security scanners on 90 top-starred public MCP-server repos (4,898 tools statically extracted, commit-pinned corpus, plus a 45-repo fresh validation set).
- The first result was humbling: mcpaudit v0.6's HIGH `permission_scope` findings had **37.5% strict precision** on hand-labelled samples.
- I patched the scanner and re-evaluated on a held-out sample. Precision rose to **64.3%**, and on a blind-labelled fresh corpus it went from **40% to 72.7%** with every accurate finding retained.
- memsentry false positives on 170 agent-context files dropped from **61 to 5**.
- Limitations (single labeller, top-starred repos only, static extraction) are documented in the report.

**AI-agent security scanners** — Python CLIs on PyPI with SARIF output for GitHub code scanning and documented evaluation methodology:

| Tool | What it detects |
|---|---|
| [mcpaudit](https://github.com/Pyhroff/mcpaudit) | MCP servers: tool-description poisoning, over-broad permission scope, rug-pull and confused-deputy patterns |
| [memsentry](https://github.com/Pyhroff/memsentry) | Injected instructions and hidden payloads in agent memory/context files |
| [ragsentry](https://github.com/Pyhroff/ragsentry) | Instruction injection and retrieval manipulation in RAG source documents |
| [trainsentry](https://github.com/Pyhroff/trainsentry) | Planted poisoning in fine-tuning datasets: injection, rare-trigger backdoors, duplicate flooding |
| [loopcheck](https://github.com/Pyhroff/loopcheck) | Wasted calls in agent tool-calling loops: duplicates, thrashing, semantic redundancy |
| [aisec-suite](https://github.com/Pyhroff/aisec-suite) | One `aisec` CLI and GitHub Action that runs the scanners together |

Also: [adversagen](https://github.com/Pyhroff/adversagen) (red-team counterpart that evolves evasions against the scanners above) and [agent-security-ci](https://github.com/Pyhroff/agent-security-ci) (the scanners wired into a CI gate against clean/vulnerable agent fixtures).

**[OSIRIS](https://github.com/Pyhroff/osiris)** — my personal agent runtime, which I use daily from the terminal. It supports multiple LLM providers with failover, tool calling and a Discord interface. It also includes a tool-calling reliability benchmark for local models, which led to a dedicated Ollama code path and fixed a large local-model latency problem.

**[soc-parallax](https://github.com/Pyhroff/soc-parallax)** — SOC behavioural-detection platform (FastAPI, Postgres, Neo4j, local LLM via Ollama, Next.js).

---

### Open-source contributions

| Project | PR | Status |
|---|---|---|
| **SQLGlot** | [#8780](https://github.com/tobymao/sqlglot/pull/8780) — typed lambda parameters shared one DataType node across casts, breaking in-place transforms | ✅ Merged |
| **LiteLLM** | [#47091](https://github.com/BerriAI/litellm/pull/47091) — map OpenAI-style string stop sequence to list for Cohere chat | ✅ Merged |
| LiteLLM | [#47105](https://github.com/BerriAI/litellm/pull/47105), [#47312](https://github.com/BerriAI/litellm/pull/47312) — proxy access control & model scoping | Open |
| SQLFluff | [#8899](https://github.com/sqlfluff/sqlfluff/pull/8899), [#8900](https://github.com/sqlfluff/sqlfluff/pull/8900), [#8901](https://github.com/sqlfluff/sqlfluff/pull/8901), [#8902](https://github.com/sqlfluff/sqlfluff/pull/8902) — dialect grammar fixes | In review |
| FastMCP · CrewAI | [#6063](https://github.com/PrefectHQ/fastmcp/pull/6063) (timeout & callback limits) · [#8240](https://github.com/crewAIInc/crewAI/pull/8240) | Open |
| Qualtran · PennyLane | [#1986](https://github.com/quantumlib/Qualtran/pull/1986) · [#10391](https://github.com/PennyLaneAI/pennylane/pull/10391) | Open |

---

### Other projects

[ModelHawk](https://github.com/Pyhroff/ModelHawk) (pickle-RCE detection in model files without loading them) · [PromptStrike](https://github.com/Pyhroff/promptstrike) (LLM jailbreak red-teaming CLI) · [pqc-scanner](https://github.com/Pyhroff/pqc-scanner) (post-quantum crypto migration analyzer) · [qec-lab](https://github.com/Pyhroff/qec-lab) (surface-code simulation with Stim + PyMatching)

**Stack:** Python, TypeScript, SQL, Bash · FastAPI, Postgres, Neo4j, Docker · OpenAI/Anthropic/Ollama APIs, MCP · SARIF, GitHub Actions
