# Praising Harris Ratnam

Computer science undergraduate focused on **security for AI systems**: scanners, detectors and evaluation harnesses for agents, MCP servers, RAG pipelines and SOC telemetry. I care about measured results and say what a number does and does not show.

## Selected work

| Project | What it is | Status |
|---|---|---|
| [mcp-scan-study](https://github.com/Pyhroff/mcp-scan-study) | Empirical study: I scanned 90 public MCP-server repos (plus a fresh 45-repo validation set) with my own scanners, hand-labelled 120 findings with Wilson confidence intervals, found no genuine tool poisoning, and used the labelled false positives to patch the scanners. On samples the patch had not seen, precision rose from about 39% to 69% at 81% recall. Single labeller and top-starred repos only; limits are in the report. | Full method, data and patches published |
| [aisec-suite](https://github.com/Pyhroff/aisec-suite) | One command that runs static security scanners over AI-agent projects: MCP servers, agent memory files and RAG documents. SARIF output, baselines, and reachability analysis to cut false positives. Tested on a held-out benchmark (48.1% recall at 0.03% false-positive rate; the held-out set was evaluated twice and that is disclosed in the repo). | Released on PyPI, v0.3.0, CI with trusted publishing |
| [soc-parallax](https://github.com/Pyhroff/soc-parallax) | SOC detection platform: attributable risk scores, MITRE ATT&CK mapping from a YAML rulebook, incident correlation in Neo4j, and narratives checked against the evidence before they are shown. FastAPI, PostgreSQL, Next.js. | I audited my own first version, found its headline metrics were inflated, rebuilt the evaluation, and published the lower numbers in [docs/EVALUATION.md](https://github.com/Pyhroff/soc-parallax/blob/master/docs/EVALUATION.md) |
| [ModelHawk](https://github.com/Pyhroff/ModelHawk) | Static scanner for code-execution backdoors in PyTorch and pickle model files (deserialization RCE), standard library only. | Public |
| [pqc-scanner](https://github.com/Pyhroff/pqc-scanner) | Static analyzer for quantum-vulnerable cryptography: AST-based Python detector plus rules for JS, Java and Go, aware of NIST FIPS 203/204/205. | Public |

Also built (private for now): scanners for MCP servers, agent memory files, RAG documents and fine-tuning datasets, and a waste auditor for agent tool-calling loops.

## How I work

- **Evaluate honestly.** Train and test on separate data, report false positives next to detection rates, and keep the caveats in the write-up.
- **Secure by default.** Constant-time key checks, fail-closed auth, path-confined file access, no default secrets, non-root containers.
- **Small, tested units.** Rules and parsers ship with positive and negative test cases; CI runs lint and tests on every push.

## Stack

Python, FastAPI, TypeScript, Next.js, PostgreSQL, Neo4j, Docker, GitHub Actions, MITRE ATT&CK, Sysmon and Windows event logs, LLM tooling (Ollama, LangGraph).

## Currently

Extending soc-parallax to more Windows log sources and evaluating it on real benign logs; adding scanners to aisec-suite; preparing for security and AI engineering roles.

## Contact

[praisinghharris@gmail.com](mailto:praisinghharris@gmail.com) · [LinkedIn](https://www.linkedin.com/in/Praising_Harris)
