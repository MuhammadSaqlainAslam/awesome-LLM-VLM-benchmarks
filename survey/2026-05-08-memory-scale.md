# Memory Scale Evaluation: When Stored Evidence Stops Being Usable (2026)

## Problem
Standard memory-agent benchmarks report fixed-point metrics — accuracy at a fixed memory load — without revealing whether stored evidence remains functional as irrelevant information accumulates over time. Production deployments of memory-augmented agents accumulate sessions continuously, most of which are irrelevant to any given query. Evaluating at fixed scale conceals a critical deployment risk: an agent that performs well at 10 sessions may degrade systematically at 100 or 1,000 sessions as irrelevant context swamps the memory system. The field has no protocol for identifying the usable-scale threshold beyond which memory reliability collapses.

## Method
**Memory Scale Evaluation** (arXiv: 2605.07313, May 2026) introduces a **scale-conditioned evaluation protocol** where task-relevant evidence stays constant while irrelevant sessions are progressively added. Four diagnostic metrics are tracked: (1) budget-compliant reliability (does the agent stay within its memory retrieval budget?), (2) tail memory-call burden (does memory load spike at scale?), (3) failure patterns (how does the agent fail?), and (4) the **usable-scale threshold** — the point beyond which reliability degrades unacceptably. **LongMemEval** and **LoCoMo** benchmarks are evaluated across **flat, planar, and hierarchical** memory architectures.

## Benchmarks / Datasets
- LongMemEval and LoCoMo (established memory agent benchmarks)
- 3 memory architecture types: flat / planar / hierarchical
- Scale-conditioned protocol: task evidence fixed, irrelevant sessions incrementally added
- Multiple agents: HippoRAG, LiCoMemory with Qwen3-8B / 32B / 235B

## Key Results

| Agent / Architecture | Finding at Scale |
|---|---|
| HippoRAG | Budget-compliant but 16–20 pp reliability decline with irrelevant sessions |
| LiCoMemory (Qwen3-8B) | Exceeds budget constraints — unbounded memory call growth |
| LiCoMemory (Qwen3-32B / 235B) | Remains within tested budget ranges |

- **HippoRAG maintains budget compliance but experiences 16–20 percentage point reliability decline as irrelevant sessions accumulate — memory architectures that appear stable become unreliable at scale**
- Memory reliability degradation operates through multiple failure mechanisms rather than a single failure mode — no single fix addresses all scale failures
- LiCoMemory with Qwen3-8B exceeds memory budget constraints at scale — small-model memory agents cannot sustain bounded resource usage in long-running deployments
- Scalability claims for memory agents are conditional: they depend on specific agent, interface, scale range, and interaction budget — unconditional scalability claims are invalid

## Enterprise / Industry Relevance
FoxBrain deployments that use persistent memory agents — for long-running supplier relationship management, employee knowledge accumulation, or project context maintenance — face exactly the scale failure described here. A FoxBrain memory agent evaluated at 50 sessions may show strong performance, but at 500 sessions (realistic for long-running supply chain projects) the 16–20 pp reliability decline from irrelevant session accumulation means retrieved evidence degrades substantially. Foxconn should adopt scale-conditioned memory evaluation when deploying any FoxBrain memory agent: test at 10×, 50×, and 100× expected session counts, measure the usable-scale threshold, and design session pruning or memory consolidation strategies before the agent reaches its reliability cliff. The finding that Qwen3-8B-backed agents exceed memory budgets at scale is particularly relevant if FoxBrain uses efficiency-optimised small models for deployed memory agents.

---
*Back to [Main Digest](../README.md)*
