# AgentTrust: Runtime Safety Evaluation and Interception for AI Agent Tool Use (2026)

## Problem
AI agents executing real-world operations through tool calls — file deletions, shell commands, HTTP requests, database queries — lack runtime safety enforcement. Post-hoc benchmarks measure what happened; static guardrails block based on pattern matching; sandboxes isolate but don't prevent harmful intent from being executed within the sandbox. None of these prevent a harmful tool call from being approved in real time before execution. The gap is a runtime layer that can evaluate whether a tool call is safe before it executes and block or modify it accordingly.

## Method
**AgentTrust** (arXiv: 2605.04785, May 2026) introduces a runtime safety interception layer that sits between the agent and its tools, evaluating every tool call before execution and delivering one of four verdicts: **allow**, **warn**, **block**, or **review**. Technical components include:
- **Shell deobfuscation**: decodes obfuscated shell commands before safety evaluation
- **SafeFix**: proposes safer alternative versions of flagged tool calls
- **RiskChain detection**: identifies multi-step attack patterns across a sequence of tool calls (not just individual calls)
- **LLM-based judgment**: handles ambiguous cases where rule-based evaluation is insufficient
- Evaluated on a 300-scenario internal benchmark (6 risk categories) and 630 independently constructed real-world adversarial scenarios

## Benchmarks / Datasets
- 300-scenario internal benchmark across 6 risk categories
- 630 independently constructed real-world adversarial scenarios
- Shell-obfuscated payload subset for deobfuscation testing
- Compatible with MCP-based agent frameworks

## Key Results

| Benchmark | Verdict Accuracy | Risk-Level Accuracy | Latency |
|---|---|---|---|
| 300-scenario internal | **95.0%** | **73.7%** | Low-millisecond |
| 630 real-world adversarial | **96.7%** | — | Low-millisecond |
| Shell-obfuscated payloads | **~93%** | — | Low-millisecond |

- **96.7% verdict accuracy on 630 real-world adversarial scenarios with low-millisecond latency — runtime safety interception is practical for production deployment without prohibitive overhead**
- 93% accuracy on shell-obfuscated payloads demonstrates that deobfuscation is effective against adversarial evasion attempts
- RiskChain detection enables identification of multi-step attack sequences — the most dangerous attack class (individually benign tool calls that collectively cause harm)
- SafeFix's safe alternative proposal mechanism enables partial task completion rather than full blocking — improving usability while maintaining safety

## Enterprise / Industry Relevance
AgentTrust directly addresses the highest-priority runtime safety gap in FoxBrain's agentic deployments. When FoxBrain agents execute file operations, database queries, or API calls on Foxconn's production systems, a runtime verdict layer at 96.7% accuracy and low-millisecond latency is the difference between an exploitable agent and a safely operating one. The RiskChain multi-step detection capability is particularly critical for Foxconn's complex agentic workflows: a single tool call to read a supplier record followed by a write to a payment system may be legitimate or an attack — only sequence-level analysis can distinguish them. SafeFix's safe-alternative capability is directly applicable to FoxBrain's operational requirements: rather than blocking a query that accesses sensitive supplier data, AgentTrust can propose a redacted version that serves the legitimate intent without exposing unnecessary information. FoxBrain's agentic framework should integrate a runtime interception layer (whether AgentTrust or equivalent) before any agent with enterprise system write access is deployed.

---
*Back to [Main Digest](../README.md)*
