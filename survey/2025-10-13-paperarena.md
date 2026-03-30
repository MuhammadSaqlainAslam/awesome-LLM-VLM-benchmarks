# PaperArena: Tool-Augmented Agentic Reasoning on Scientific Literature (2025)

## Problem
LLM-based agents are increasingly used to assist with scientific research, but no benchmark systematically evaluates their ability to reason across multiple papers using tools — multimodal parsing, context retrieval, and programmatic computation — as an integrated agentic workflow.

## Method
PaperArena provides 784 question-answer pairs requiring cross-paper scientific reasoning. Agents must formulate multi-step reasoning plans, interact with multiple papers simultaneously, and invoke specialized tools (PDF parsing, retrieval, computation) to produce grounded answers. Questions are stratified into easy and hard subsets, with Ph.D. expert baselines established for each.

## Benchmarks / Datasets
- **PaperArena:** 784 QA pairs; cross-paper scientific reasoning; tool-augmented agent evaluation.
- **Subsets:** Easy and hard difficulty tiers.
- **Expert Baseline:** 83.50% (Ph.D. domain experts).
- **Metrics:** Exact-match accuracy; tool call correctness; reasoning plan quality.
- **GitHub:** https://github.com/Melmaphother/PaperArena

## Key Results
Leading models achieve only **38.78% average accuracy** overall and **18.47% on hard subsets**, versus the 83.50% Ph.D. expert baseline — a gap of over 44 percentage points. Multi-tool orchestration and cross-paper synthesis remain severe bottlenecks even for frontier models.

## FoxBrain Relevance
High strategic relevance. If FoxBrain is to support R&D teams in literature-grounded technical decision-making, the PaperArena methodology provides both a benchmark and a target architecture. The 38.78% → 83.50% gap quantifies the current ceiling; FoxBrain's scientific reasoning pipeline should be benchmarked here and the tool orchestration failures studied to inform system design improvements.

---
*Back to [Main Digest](../README.md)*
