# Praising Y Harris Ratnam (@Pyhroff)

**Application security & AI security, in Python.** I build static scanners for the inputs AI agents trust (MCP tool metadata, agent memory files, RAG documents), measure them on real repositories, and publish what they miss.

B.Tech CSE (Cybersecurity), IIIT Kottayam, 2024–2028 · Looking for Summer 2027 security / AI-security internships
[praisingharris@gmail.com](mailto:praisingharris@gmail.com) · [LinkedIn](https://www.linkedin.com/in/praising-harris-8a3320330) · [PyPI](https://pypi.org/user/Pyhroff/)

[![IIIT Kottayam · B.Tech Cybersecurity](assets/badges/badge_iiitk.svg)](https://www.iiitkottayam.ac.in)
[![4 merged PRs](assets/badges/badge_merged_prs.svg)](#upstream-pull-requests)
[![12 open PRs](assets/badges/badge_active_prs.svg)](#upstream-pull-requests)
[![4 PyPI packages](assets/badges/badge_pypi_packages.svg)](#what-i-build)

---

## What I build

| Project | What it is | Measured result |
|---|---|---|
| [**aisec-suite**](https://github.com/Pyhroff/aisec-suite) · [PyPI 0.4.0](https://pypi.org/project/aisec-suite/) | A CI security gate for AI-agent inputs. One `aisec scan` runs the scanners below and emits SARIF; it also ships as a GitHub Action. | Tool-poisoning detector: 48.1% recall on 54 held-out synthetic attacks (naive regex: 0%), 0.03% false positives (1 of 3,974 real tool descriptions). Method and caveats in [STUDY.md](https://github.com/Pyhroff/aisec-suite/blob/main/docs/STUDY.md). |
| [**mcpaudit**](https://github.com/Pyhroff/mcpaudit) · [PyPI 0.8.0](https://pypi.org/project/pyhroff-mcpaudit/) | Scans MCP server tool surfaces for tool poisoning, over-broad scope, rug pulls and confused-deputy behaviour. | Scope-rule rewrite (v0.7) raised precision from 40% to 72.7% on a blind-labelled fresh corpus of 45 repos, keeping all 16 true findings. |
| [**mcp-scan-study**](https://github.com/Pyhroff/mcp-scan-study) | Hand-labelled scan of 135 public MCP-server repos. | Found **no tool poisoning in the wild**. Naive scope rules were right 37.5% of the time. |
| [**memsentry**](https://github.com/Pyhroff/memsentry) · [**ragsentry**](https://github.com/Pyhroff/ragsentry) | Static scanners for injected instructions in agent memory/context files and in RAG source documents. | memsentry 1.2.0 cut findings on 170 real context files from 61 to 5. |
| [**soc-parallax**](https://github.com/Pyhroff/soc-parallax) | Behavioural detection platform: per-entity baselines, attributable risk scores, MITRE ATT&CK mapping (FastAPI, Neo4j, Next.js). | On 278 real EVTX attack samples, 29.5% reach medium severity or higher (27.3% held-out). |
| [**osiris**](https://github.com/Pyhroff/osiris) | My daily-use personal AI assistant runtime: 8 providers with failover, 9 tool-scoped agents, embedding memory. | Used every day from the terminal. |

On PyPI: `aisec-suite` 0.4.0 · `pyhroff-mcpaudit` 0.8.0 · `memsentry` 1.2.0 · `pyhroff-ragsentry` 1.1.0

## Upstream pull requests

**Merged and shipped:**
- [tobymao/sqlglot #8780](https://github.com/tobymao/sqlglot/pull/8780) (v30.25.0): copy the `DataType` node for each cast in `_replace_lambda` so no AST node has two parents.
- [sqlfluff/sqlfluff #8901](https://github.com/sqlfluff/sqlfluff/pull/8901), [#8902](https://github.com/sqlfluff/sqlfluff/pull/8902) (4.5.0): remove unsupported `FLUSH` from the Doris and StarRocks grammars.
- [BerriAI/litellm #47091](https://github.com/BerriAI/litellm/pull/47091): normalise a string `stop` to a list for Cohere.

**Open, under review:**
- [BerriAI/litellm #47105](https://github.com/BerriAI/litellm/pull/47105): fail closed when a key or team has access groups but an empty model list (issue #46951). Also [#47106](https://github.com/BerriAI/litellm/pull/47106) and [#47107](https://github.com/BerriAI/litellm/pull/47107).
- [sqlfluff/sqlfluff #8900](https://github.com/sqlfluff/sqlfluff/pull/8900) (maintainer-approved).
- [crewAIInc/crewAI #8240](https://github.com/crewAIInc/crewAI/pull/8240) (MCP pagination), [#8242](https://github.com/crewAIInc/crewAI/pull/8242), [#8244](https://github.com/crewAIInc/crewAI/pull/8244), [#8245](https://github.com/crewAIInc/crewAI/pull/8245).
- [PrefectHQ/fastmcp #6063](https://github.com/PrefectHQ/fastmcp/pull/6063): wall-clock timeout and callback cap for the Monty sandbox.
- [graphql-python/graphene #1610](https://github.com/graphql-python/graphene/pull/1610): lazy type references for `Connection.Meta.node`.
- [PennyLaneAI/pennylane #10391](https://github.com/PennyLaneAI/pennylane/pull/10391): `Evolution` pytree leaves and `bind_new_parameters` with a parametric base.
- [quantumlib/Qualtran #1986](https://github.com/quantumlib/Qualtran/pull/1986): CNOT count in `Add.build_call_graph` for unequal register bitsizes.

## How I report results

- Every number above links to the repo or PR it comes from, including the ones that don't flatter me: the null result in the wild, and the held-out set I evaluated twice.
- Detectors are review aids, not security boundaries. My tool-poisoning detector still misses about half of unseen attacks.
