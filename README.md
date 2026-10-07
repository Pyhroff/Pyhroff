# Praising Harris Ratnam

Computer science undergraduate focused on **security for AI systems**: scanners, detectors, red-team tooling and evaluation harnesses for agents, MCP servers, RAG pipelines, model artifacts and SOC telemetry. I care about measured results, reproducible experiments, and being explicit about limitations.

## Selected work

| Project | What it is |
|---|---|
| [mcp-scan-study](https://github.com/Pyhroff/mcp-scan-study) | Empirical study of MCP-server security scanning, with a fresh validation set, hand-labelled findings, confidence intervals, and scanner patches evaluated on data the patch had not seen. |
| [aisec-suite](https://github.com/Pyhroff/aisec-suite) | Unified CLI for security scanning across MCP, memory, RAG, training data, supply chain, agent behavior and package-worm surfaces, with JSON/SARIF output, baselines and CI enforcement. |
| [promptstrike](https://github.com/Pyhroff/promptstrike) | LLM red-team framework implementing PAIR, TAP, GCG and Crescendo, including agent/tool-output testing and a defensive shield. |
| [soc-parallax](https://github.com/Pyhroff/soc-parallax) | Behavioral SOC platform with attributable risk scoring, rule-based MITRE ATT&CK mapping, Neo4j correlation and grounded investigation narratives. |
| [darkdecoder](https://github.com/Pyhroff/darkdecoder) | Threat-intelligence analyzer combining MITRE ATT&CK and MITRE ATLAS for suspicious code and AI-security inputs. |
| [ModelHawk](https://github.com/Pyhroff/ModelHawk) | Static scanner for code-execution backdoors in PyTorch and pickle model artifacts. |
| [pqc-scanner](https://github.com/Pyhroff/pqc-scanner) | Static analyzer for quantum-vulnerable cryptography across Python, JavaScript, Java and Go, aligned with NIST post-quantum standards. |
| [PhantomGrid](https://github.com/Pyhroff/PhantomGrid) | Behavioral security research prototype for detecting suspicious interaction patterns in banking workflows. |
| [proxy-Strands](https://github.com/Pyhroff/proxy-Strands) | AI browser-agent prototype with policy gating, indirect prompt-injection defense and human-gated handling of sensitive form fields. |

## How I work

- **Evaluate honestly.** Separate development and evaluation data, report false positives beside detection rates, and document where a benchmark does not generalize.
- **Secure by default.** Fail-closed authorization, path-confined file access, no default secrets, least-privilege workflows and non-root containers.
- **Build small, tested units.** Detection rules and parsers ship with positive and negative cases; CI validates the important paths.
- **Make security claims auditable.** Prefer deterministic mappings, evidence-backed explanations and reproducible experiments over impressive but unsupported numbers.

## Stack

Python, FastAPI, TypeScript, Next.js, PostgreSQL, Neo4j, Docker, GitHub Actions, MITRE ATT&CK, MITRE ATLAS, Sysmon/Windows event logs, Ollama and LangGraph.

## Currently

Extending AI-security tooling, strengthening benchmark methodology, and building toward security and AI engineering roles.

## Contact

[praisinghharris@gmail.com](mailto:praisinghharris@gmail.com) · [LinkedIn](https://www.linkedin.com/in/Praising_Harris)
