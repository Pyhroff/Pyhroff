<div align="center">

# Praising Harris Ratnam

### AI Security Engineer · AI Engineer, with a cybersecurity backbone
**Python-native** · B.Tech CSE (Cybersecurity), IIIT Kottayam, batch of 2028

[![Portfolio](https://img.shields.io/badge/Portfolio-pyhroff.github.io-00ADB5?style=for-the-badge&logo=google-chrome&logoColor=white)](https://pyhroff.github.io)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Praising_Harris-0A66C2?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/praising-harris-8a3320330)
[![Email](https://img.shields.io/badge/Email-praisingharris%40gmail.com-D14836?style=for-the-badge&logo=gmail)](mailto:praisingharris@gmail.com)
[![PyPI](https://img.shields.io/badge/PyPI-aisec--suite_v0.11.0-blue?style=for-the-badge&logo=pypi)](https://pypi.org/project/aisec-suite/)

</div>

---

## What I do

I build and measure security tooling for AI agents, and I build the agent and ML systems themselves.
Everything is written in Python. The only non-Python code across my repositories is a Next.js dashboard front end in `soc-parallax`.

My security background (detection engineering, application security, threat modelling) shapes how I build AI systems:
treat model output and tool metadata as untrusted input, enforce controls in code rather than in the prompt,
and publish what a detector misses next to what it catches.

**Open to:** internships May-Jul 2027, full-time roles from 2028 (AI security, AI engineering, application security; India or remote).

---

## Flagship projects

| Project | What it is | Measured result |
|---|---|---|
| [**aisec-suite**](https://github.com/Pyhroff/aisec-suite) (PyPI `0.11.0`) | CI security gate for what AI agents trust: MCP tool metadata, agent memory files, RAG documents. SARIF output, baselines, reachability analysis, an MCP runtime guard and an LLM red-team CLI. | Structural poisoning detector: 53.7% recall on my held-out attacks, 14.0% on other researchers' attacks (MCPTox, MCP-Poison-Bench), 0.05% false positives on 3,974 real tool descriptions (2 flagged). It misses roughly half of unseen attacks, and the README says so. |
| [**mcp-scan-study**](https://github.com/Pyhroff/mcp-scan-study) | Hand-labelled study of 135 public MCP-server repos, with the scanner patches that came out of it. | No real tool poisoning found in the wild. mcpaudit precision went from 37.5% to 64.3% on a held-out sample, and from 40% to 72.7% on a blind-labelled fresh corpus. |
| [**mcpaudit**](https://github.com/Pyhroff/mcpaudit) · [**memsentry**](https://github.com/Pyhroff/memsentry) · [**ragsentry**](https://github.com/Pyhroff/ragsentry) | The three scanners behind aisec-suite: MCP tool surfaces, agent memory/context files, RAG source documents. | On attacks written by others, memsentry and ragsentry catch the stock "ignore previous instructions" phrase and 0-3% of attacks without it. |
| [**soc-parallax**](https://github.com/Pyhroff/soc-parallax) | Detection platform: per-entity behavioural baselines, an attributable risk score, MITRE ATT&CK mapping from a versioned rulebook, incident correlation in Neo4j, grounded narratives. FastAPI, PostgreSQL, Next.js. | On 278 real EVTX attack samples, 29.5% reach medium severity or higher (27.3% on a held-out half). Nothing reaches high on held-out benign data. An earlier inflated 53% figure was found in an audit and replaced. |
| [**osiris**](https://github.com/Pyhroff/osiris) | Model-agnostic assistant runtime: 8 LLM providers behind one failover router, tool-scoped agents, embedding memory. I use it daily. | Traced a local-model slowdown to Ollama's thinking mode and fixed it with a native adapter (about 100 s to 10 s per call, measured live). |
| [**kronos-kv**](https://github.com/Pyhroff/kronos-kv) | Standard-library-only Python storage and distributed-systems exercise: a Bitcask-style log-structured store with CRC32 and hint files, a Raft simulator and consistent hashing. | 84.29% disk reclaimed by compaction on the benchmark; Raft runs in an in-process simulator, not over a network. |

More in the portfolio: [PhantomGrid](https://github.com/Pyhroff/PhantomGrid) (behavioural biometrics for banking fraud, team hackathon project),
[promptstrike](https://github.com/Pyhroff/promptstrike) (multi-turn LLM red-teaming), [loopcheck](https://github.com/Pyhroff/loopcheck) (agent-loop waste auditor),
[darkdecoder](https://github.com/Pyhroff/darkdecoder) (ATT&CK + ATLAS threat-intel analysis) and
[specprove-sec](https://github.com/Pyhroff/specprove-sec) (Z3 model checking of agent protocols, research prototype).

---

## Upstream open source

7 pull requests merged and 13 open at the last check (13 Nov 2026). Live status is on each PR; the full table is on the [portfolio](https://pyhroff.github.io/#upstream).

| Merged | What it fixed |
|---|---|
| [tobymao/sqlglot #8780](https://github.com/tobymao/sqlglot/pull/8780) | `Parser._replace_lambda` shared one `DataType` node between several casts. |
| [PrefectHQ/fastmcp #6063](https://github.com/PrefectHQ/fastmcp/pull/6063) | Host callbacks were not counted against the Monty sandbox time limit; added a wall-clock timeout and a call budget. |
| [BerriAI/litellm #47091](https://github.com/BerriAI/litellm/pull/47091) | A string `stop` value is now wrapped for Cohere `stop_sequences`. |
| [sqlfluff #8899](https://github.com/sqlfluff/sqlfluff/pull/8899), [#8901](https://github.com/sqlfluff/sqlfluff/pull/8901), [#8902](https://github.com/sqlfluff/sqlfluff/pull/8902), [#9059](https://github.com/sqlfluff/sqlfluff/pull/9059) | Dialect grammar fixes for StarRocks, Doris and MySQL. |

Open work includes authorization fixes in LiteLLM ([#47105](https://github.com/BerriAI/litellm/pull/47105)), MCP pagination in CrewAI ([#8240](https://github.com/crewAIInc/crewAI/pull/8240)),
and fixes in PennyLane, Qualtran, Graphene and Presidio.

---

## Stack

- **Language:** Python (asyncio, FastAPI, Pydantic, pytest, AST analysis, scikit-learn)
- **AI engineering:** LLM tool-calling and agent loops, provider routing and failover, embeddings and retrieval, evaluation harnesses, local models with Ollama
- **AI security:** MCP security, prompt injection and tool poisoning, RAG and memory poisoning, LLM red-teaming (PAIR, TAP, Crescendo), OWASP Top 10 for LLMs, runtime guards, SARIF
- **Security foundations:** MITRE ATT&CK and ATLAS, Sigma, threat modelling (STRIDE), detection engineering, Z3 model checking
- **Data and infra:** PostgreSQL, Neo4j, SQLite, Docker, GitHub Actions
- **Practice:** TryHackMe top 2% globally

---

## Writing

- [Static scanners miss most MCP tool poisoning](https://pyhroff.github.io/blog/static-scanners-miss-mcp-tool-poisoning.html) (Nov 2026): what my detector catches, what it misses, and why a learned classifier did not close the gap.

---

## How I work

Every number links back to a script, a labelled dataset or a study document. Where a result is weak, the README says so:
single labeller, synthetic data, held-out sets evaluated more than once. AI coding assistants were used on some projects
and are disclosed in those READMEs.
