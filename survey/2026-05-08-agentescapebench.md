# AgentEscapeBench: Evaluating Out-of-Domain Tool-Grounded Reasoning in LLM Agents (2026)

## Problem
Existing agent benchmarks evaluate tool use in familiar scenarios where agents can rely on training-time patterns. They fail to test whether agents can generalise tool-grounded reasoning to genuinely novel situations with complex, long-range tool dependencies. When deployed in production, agents encounter unfamiliar tool chains and multi-step dependency structures not seen during training. No benchmark existed to specifically isolate and measure this out-of-domain tool-grounded generalisation capability — the gap between benchmark performance and real deployment failure.

## Method
**AgentEscapeBench** (arXiv: 2605.07926, May 2026) introduces an escape-room-style benchmark where tasks are modelled as **directed acyclic dependency graphs (DAGs)** over tools and items. Agents must invoke real external functions, track progressively revealed state information, propagate intermediate results across steps, and provide deterministically verifiable final answers. The benchmark comprises **270 instances across five difficulty tiers** (parameterised by DAG depth and branching). **16 LLM agents and human participants** are evaluated. Trajectory analysis identifies primary failure modes from agent execution traces.

## Benchmarks / Datasets
- 270 instances across 5 difficulty tiers (DAG-parameterised difficulty)
- 16 LLM agents evaluated
- Human participants as comparison baseline
- Real external function invocation (not simulated)
- Deterministically verifiable answers (no LLM-judge required)

## Key Results

| Condition | Human Success Rate | Top Model Success Rate |
|---|---|---|
| Difficulty tier (easiest) | 98.3% | 90.0% |
| Difficulty tier (hardest) | 80.0% | 60.0% |
| Performance gap (humans vs. top model at hardest) | — | 20 pp below human |

- **Top-performing LLM agent drops from 90.0% to 60.0% success rate across difficulty tiers — a 30 pp collapse vs. humans who drop from 98.3% to 80.0% (18 pp)**
- The human-agent performance gap widens substantially with difficulty: from 8.3 pp at easiest to 20 pp at hardest — current agents cannot scale with task complexity the way humans do
- Trajectory analysis identifies three primary failure modes: breakdown in long-range state tracking, failure to adhere to revealed clues, and loss of intermediate-result propagation
- Deterministic verifiability eliminates LLM-judge confounds — benchmark results directly reflect tool-grounded reasoning capability

## Enterprise / Industry Relevance
Foxconn's FoxBrain agents are deployed in complex multi-tool workflows: quality inspection chains, supplier compliance verification, and cross-system data integration pipelines all involve DAG-structured tool dependencies where intermediate results from one step gate subsequent actions. AgentEscapeBench's finding that top agents drop to 60% success on high-depth dependency chains directly predicts FoxBrain failure rates in production workflows where tool dependencies are deep and sequential. The three identified failure modes — state tracking breakdown, clue non-adherence, and intermediate-result propagation loss — are exactly the failure modes that would cause silent errors in FoxBrain supply chain automation (e.g., using a stale intermediate result from step 2 in step 5 of a compliance check). Foxconn should adopt DAG-parameterised difficulty evaluation for FoxBrain agent testing, and treat the 60% success rate at high depth as an upper bound for complex multi-step FoxBrain deployments pending targeted remediation.

---
*Back to [Main Digest](../README.md)*
