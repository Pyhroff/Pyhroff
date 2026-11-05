# Pinned Repositories: what to pin and what to write

How to pin repositories on your GitHub profile: open github.com/Pyhroff → "Customize your pins" → tick the six below → drag them into this order.

Checked 3 Nov 2026. Every repo below exists and is public. Numbers come from `Luna/CLAIMS_LEDGER.md`.

## Pin these 6, in this order

| # | Repo | Why it earns a pin |
|---|---|---|
| 1 | [`aisec-suite`](https://github.com/Pyhroff/aisec-suite) | The flagship: a CI gate, a measured detector, an honest STUDY.md |
| 2 | [`mcpaudit`](https://github.com/Pyhroff/mcpaudit) | The scanner behind the precision study, published on PyPI |
| 3 | [`mcp-scan-study`](https://github.com/Pyhroff/mcp-scan-study) | The 135-repo hand-labelled study, with data and patches |
| 4 | [`soc-parallax`](https://github.com/Pyhroff/soc-parallax) | Blue-team breadth: detection engineering, MITRE ATT&CK |
| 5 | [`osiris`](https://github.com/Pyhroff/osiris) | Agentic AI engineering: provider router, tool-scoped agents |
| 6 | [`memsentry`](https://github.com/Pyhroff/memsentry) | Shows the memory-poisoning surface. Swap in `ragsentry` if you prefer RAG |

Don't pin repos that don't exist publicly (`systems-showcase`, `security-advisories`, `pyhroff-mcpaudit`, `pyhroff-ragsentry`).

## Repo "About" lines (paste into GitHub, max ~350 chars)

### 1. aisec-suite
`CI security gate for AI-agent inputs: MCP tool metadata, agent memory files, RAG documents. One command, SARIF output, GitHub Action. Structural tool-poisoning detector: 53.7% recall on held-out synthetic attacks at 0.05% FPR on 3,974 real tool descriptions.`
Topics: `ai-security` `mcp` `prompt-injection` `tool-poisoning` `static-analysis` `sarif` `github-actions` `python`

### 2. mcpaudit (PyPI: `pyhroff-mcpaudit`)
`Security scanner for MCP server tool surfaces: tool poisoning, over-broad scope, rug pulls, confused deputy. v0.7 scope rules: precision 40% to 72.7% on a blind-labelled 45-repo corpus. pip install pyhroff-mcpaudit`
Topics: `mcp` `model-context-protocol` `ai-security` `static-analysis` `python`

### 3. mcp-scan-study
`Hand-labelled scan of 135 public MCP-server repos with mcpaudit and memsentry. No tool poisoning found in the wild; scanner precision measured with Wilson CIs, then patched.`
Topics: `mcp` `security-research` `empirical-study` `ai-security`

### 4. soc-parallax
`Behavioural detection platform: per-entity baselines, attributable risk scores, MITRE ATT&CK mapping, incident graph. Evaluated on 278 real EVTX attack samples.`
Topics: `detection-engineering` `mitre-attack` `soc` `fastapi` `neo4j`

### 5. osiris
`Model-agnostic personal AI assistant runtime: 8 LLM providers with failover, 9 tool-scoped agents, embedding memory.`
Topics: `ai-agents` `llm` `tool-calling` `python`

### 6. memsentry
`Static scanner for poisoned AI-agent memory and context files (CLAUDE.md, .cursorrules, ...): persistent instruction injection, hidden payloads, dependency manipulation.`
Topics: `ai-security` `prompt-injection` `agent-memory` `static-analysis`

## Wording to avoid

Don't use any phrase from section 5 of `Luna/CLAIMS_LEDGER.md` ("Claims with no support"), or "production-grade", "Tier-1" or "peer-reviewed". None of them is backed by a public artifact.
