# MarketBench: Evaluating AI Agents as Market Participants (2026)

## Problem
Multi-agent AI systems increasingly operate in competitive or coordinated environments where agents must self-assess their own capability and cost before bidding for or accepting tasks. Market-based coordination — where agents compete for tasks based on self-reported success probability and cost estimates — requires accurate self-calibration. No benchmark had measured whether LLM-based agents can actually self-assess their own task completion likelihood and resource consumption reliably enough to participate meaningfully in market-style allocation systems.

## Method
**MarketBench** (arXiv: 2604.23897, April 28, 2026) evaluates whether AI agents can accurately self-evaluate their task completion likelihood and associated costs — capabilities essential for market-based multi-agent coordination. Using a 93-task subset of SWE-bench Lite (software engineering benchmark), the study tests six recently released LLMs on their ability to estimate success probability and token usage before attempting tasks, and measures how well these self-assessments translate into optimal market-based task allocation versus a full-information baseline.

## Benchmarks / Datasets
- 93-task subset of SWE-bench Lite (software engineering tasks)
- 6 recently released LLMs evaluated
- Two self-assessment targets: success probability calibration + token usage estimation
- Market allocation divergence from full-information baseline as primary metric
- Contextual intervention: prior experimental capability data added to model context

## Key Results

| Evaluation Dimension | Key Finding |
|---|---|
| Success probability calibration | Poor — significant miscalibration across all 6 LLMs |
| Token usage estimation | Poor — substantial underestimation bias |
| Contextual improvement (prior data) | Modest improvement only |
| Market allocation vs. full-information | Substantial gap persists even with interventions |
| Self-assessment as bottleneck | Identified as the key limiting factor for market coordination |

- **All 6 evaluated LLMs show significant miscalibration in self-assessing both success probability and token consumption — agents cannot reliably predict their own performance before attempting a task**
- Adding prior experimental capability data to model context provides only modest improvement — the self-assessment gap is not easily closed through prompting
- Market allocation quality remains substantially below the full-information baseline despite interventions, confirming that agent self-assessment is the primary bottleneck for market-based AI coordination
- MarketBench provides the first evaluation framework specifically for agent self-calibration in competitive multi-agent market settings

## FoxBrain Relevance
Foxconn's multi-agent FoxBrain architecture routes tasks across specialized agents — if a market-based or competitive allocation mechanism is used to assign tasks based on agent self-reported capability, MarketBench's findings are critical: agents cannot reliably estimate their own success probability or cost. This means any FoxBrain orchestration layer that relies on agent self-bids for task allocation must incorporate external performance history and calibration data rather than trusting agent self-reports. The benchmark also provides a direct evaluation framework for measuring FoxBrain's multi-agent market coordination readiness before deployment.

---
*Back to [Main Digest](../README.md)*
