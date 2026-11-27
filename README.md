<div align="center">

# Praising Harris Ratnam

### AI Engineering · AI Security · Applied AI
**Python-native** · B.Tech CSE (Cybersecurity), IIIT Kottayam, batch of 2028

[![Portfolio](https://img.shields.io/badge/Portfolio-pyhroff.github.io-00ADB5?style=for-the-badge&logo=google-chrome&logoColor=white)](https://pyhroff.github.io)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Praising_Harris-0A66C2?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/praising-harris-8a3320330)
[![Email](https://img.shields.io/badge/Email-praisingharris%40gmail.com-D14836?style=for-the-badge&logo=gmail)](mailto:praisingharris@gmail.com)
[![PyPI](https://img.shields.io/badge/PyPI-aisec--suite_v0.11.0-blue?style=for-the-badge&logo=pypi)](https://pypi.org/project/aisec-suite/)

</div>

---

## What I do

I build AI systems and security tooling in Python, and publish benchmarks that show where they work and where they fail.

My security background (detection engineering, application security, threat modelling) shapes how I build AI systems:
treat model output and tool metadata as untrusted input, enforce controls in code rather than in the prompt,
and publish what a detector misses next to what it catches.

**Open to:** internships May-Jul 2027, full-time roles from 2028 (AI security, AI engineering, application security; India or remote).

---

## Featured projects

| Project | What it shows | Evaluation |
|---|---|---|
| [**aisec-suite**](https://github.com/Pyhroff/aisec-suite) | AI security tooling for MCP tool metadata, agent memory, and RAG documents, with CI integration and published benchmarks. | Structural detector recall was 53.7% on my holdout and 14.0% on each external benchmark. It flagged 2 of 3,974 real tool descriptions. [Study](https://github.com/Pyhroff/aisec-suite/blob/master/docs/STUDY.md) |
| [**Osiris**](https://github.com/Pyhroff/osiris) | Model-agnostic assistant runtime with eight provider adapters, automatic failover, scoped tools, and embedding memory. | Switching to Ollama's native adapter reduced one CPU-only plain-generation task from about 100 s to 10 s. [Benchmark](https://github.com/Pyhroff/osiris/blob/main/benchmarks/FINDINGS.md) |
| [**SOC Parallax**](https://github.com/Pyhroff/soc-parallax) | Full-stack detection platform with attributable risk scores and incident correlation. Built with FastAPI, PostgreSQL, Neo4j, and Next.js. | 35 of 128 held-out attack files reached medium severity or higher. Across the full 278-file corpus, 46 files yielded no parsed events. [Evaluation](https://github.com/Pyhroff/soc-parallax/blob/main/docs/EVALUATION.md) |
| [**Lucid**](https://github.com/Pyhroff/lucid-housing-ai) | Team project for housing assistance with structured intake, human confirmation, and a deterministic eligibility rules engine. | The live model extracted all required fields correctly in 91% of 23 synthetic scenarios. [Evaluation](https://github.com/Pyhroff/lucid-housing-ai/blob/main/eval/EVAL_RESULTS.md) |

The [MCP Scan Study](https://github.com/Pyhroff/mcp-scan-study) documents the research behind aisec-suite. [mcpaudit](https://github.com/Pyhroff/mcpaudit), [memsentry](https://github.com/Pyhroff/memsentry), [ragsentry](https://github.com/Pyhroff/ragsentry), and [agent-security-ci](https://github.com/Pyhroff/agent-security-ci) provide its scanners and regression infrastructure. [ModelHawk](https://github.com/Pyhroff/ModelHawk) checks model artifacts, and [PurpleLens](https://github.com/Pyhroff/PurpleLens) tests detection rules with synthetic telemetry.

---

## Upstream open source

Eight public upstream pull requests merged as of 27 Nov 2026. [Merged PRs](https://github.com/pulls?q=is%3Apr+author%3APyhroff+is%3Apublic+-user%3APyhroff+is%3Amerged) · [Current open PRs](https://github.com/pulls?q=is%3Apr+author%3APyhroff+is%3Apublic+-user%3APyhroff+is%3Aopen)

| Merged | What it fixed |
|---|---|
| [FastMCP #6063](https://github.com/PrefectHQ/fastmcp/pull/6063) | Added a wall-clock timeout and callback budget for sandbox execution. |
| [LiteLLM #47091](https://github.com/BerriAI/litellm/pull/47091) | Normalized a string stop value to a list for Cohere's `stop_sequences`. |
| [SQLGlot #8780](https://github.com/tobymao/sqlglot/pull/8780) | Copied the `DataType` node for each cast in lambda rewrites. |
| [SQLFluff #8899](https://github.com/sqlfluff/sqlfluff/pull/8899), [#8900](https://github.com/sqlfluff/sqlfluff/pull/8900), [#8901](https://github.com/sqlfluff/sqlfluff/pull/8901), [#8902](https://github.com/sqlfluff/sqlfluff/pull/8902), [#9059](https://github.com/sqlfluff/sqlfluff/pull/9059) | Updated SQL grammar for ANSI, StarRocks, Doris, and MySQL. |

More projects on [my portfolio](https://pyhroff.github.io) and GitHub include [PhantomGrid](https://github.com/Pyhroff/PhantomGrid), [promptstrike](https://github.com/Pyhroff/promptstrike), [loopcheck](https://github.com/Pyhroff/loopcheck), and [darkdecoder](https://github.com/Pyhroff/darkdecoder).

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
