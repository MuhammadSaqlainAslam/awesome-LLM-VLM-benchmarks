# AnalysisBench: Evaluating LLM Agents on Automated Software Analysis Tasks (2026)

## Problem
Software analysis — running static analysers, fuzz testers, symbolic executors, and dynamic instrumentation tools on real codebases — is one of the most technically demanding engineering tasks for AI agents. It requires not just code generation but installing tool dependencies, configuring complex environments, interpreting cryptic tool output, and iteratively debugging when tools fail or produce unexpected results. Existing coding benchmarks evaluate code generation in clean environments; none tested whether agents could autonomously operate the full software analysis toolchain on real, heterogeneous C/C++ and Java projects with all their build system complexity.

## Method
**AnalysisBench** (arXiv: 2604.11270, April 13, 2026) constructs **35 tool-project pairs** from **7 software analysis tools** × **5 C/C++ + 5 Java projects**, each requiring the agent to: install the tool and its dependencies, configure it for the specific project, execute the analysis, interpret the results, and produce a structured report. Tools include static analysers (Infer, SpotBugs), fuzz testers (AFL++, Jazzer), symbolic executors, and dynamic instrumentation frameworks.

A custom **AnalysisAgent** framework is evaluated alongside frontier LLM backends. Tasks are graded by **manual verification** — a human expert confirms whether the tool ran correctly and whether the output is valid. Authors: Michael Pradel, Cristian Cadar, Islem Bouzenia.

## Benchmarks / Datasets
- **35 tool-project pairs:** 7 analysis tools × 5 C/C++ projects + 5 Java projects
- **Tools:** Static analysis (Infer, SpotBugs), fuzzing (AFL++, Jazzer), symbolic execution, dynamic instrumentation
- **Evaluation:** Manual verification of tool execution and output validity
- **Metrics:** Task success rate (pass/fail per tool-project pair)
- **Baseline comparison:** Direct LLM prompting vs. AnalysisAgent framework

## Key Results

| System | Task Success Rate | Notes |
|---|---|---|
| **AnalysisAgent (Gemini-3-Flash)** | **94% (33/35)** | Best result |
| Direct LLM prompting | Significantly lower | Fails on tool configuration |
| Human expert | ~100% | Baseline |

- **AnalysisAgent with Gemini-3-Flash backend achieves 94% task success** (33/35 tool-project pairs) — the highest reported performance on software analysis automation
- Direct LLM prompting without the AnalysisAgent framework fails significantly on tool installation and configuration steps, confirming that agentic scaffolding is essential for analysis workflows
- The 2 failures involve obscure build system incompatibilities not resolvable without human intervention
- Java project analysis is slightly more reliable than C/C++ due to more predictable dependency management (Maven/Gradle vs. custom Makefiles)

## FoxBrain Relevance
AnalysisBench benchmarks exactly the software quality assurance automation capabilities needed for FoxBrain's engineering productivity tools at Foxconn: automatically running static analysis on embedded firmware, security scanning on factory automation code, and dynamic testing on industrial control software. The 94% success rate with AnalysisAgent is a strong signal that AI-assisted software analysis is production-ready for well-structured projects. The remaining 6% failure rate on complex build systems maps directly onto Foxconn's legacy codebase risk — FoxBrain should be deployed with a human-in-the-loop escalation path for build configuration failures. Adopt the AnalysisAgent scaffold pattern (not raw LLM prompting) as the architecture for FoxBrain's code quality automation pipeline.

---
*Back to [Main Digest](../README.md)*
