# HINTBench: Horizon-agent Intrinsic Non-attack Trajectory Benchmark (2026)

## Problem
Existing agent safety benchmarks focus almost exclusively on adversarial, attack-based failures — scenarios where an external actor deliberately attempts to manipulate agent behavior. No benchmark evaluated intrinsic safety failures: risks that emerge organically from benign operational conditions such as misplanning, constraint violations, or cascading tool misuse without any adversarial intent. This blind spot means agents certified as "safe against attacks" may still exhibit dangerous intrinsic failure modes in production.

## Method
**HINTBench** (arXiv: 2604.13954, April 15, 2026) introduces a benchmark of 629 agent trajectories (523 risky, 106 safe; average 33 steps each) for evaluating intrinsic agent safety across three tasks: trajectory-level risk detection, risk-step localization, and intrinsic failure-type identification. Annotations follow a five-constraint unified taxonomy, and the benchmark compares both large language models and existing guard models on all three tasks.

Authors: Jiacheng Wang, Jinchang Hou, Fabian Wang, Ping Jian, Chenfu Bao, Zhonghou Lv

## Benchmarks / Datasets
- 629 total agent trajectories: 523 risky, 106 safe
- Average trajectory length: 33 steps
- 3 evaluation tasks: risk detection, risk-step localization, failure-type identification
- Five-constraint unified annotation taxonomy
- Evaluation of strong LLMs and existing guard models

## Key Results

| Task | Strong LLM Performance | Guard Model Performance |
|---|---|---|
| Risk Detection (trajectory-level) | Good | Poor transferability |
| Risk-Step Localization | Below 35 Strict-F1 | Near-failure |
| Failure-Type Identification | Hard; substantially lower | Near-failure |

- Strong LLMs perform well on trajectory-level risk detection but drop sharply to below 35 Strict-F1 on the finer-grained risk-step localization task.
- Fine-grained failure-type identification proves substantially harder than detection for all evaluated models, revealing a large capability gap between coarse and granular safety assessment.
- Existing guard models show poor transferability to the intrinsic failure domain, confirming that attack-focused safety tools are insufficient for production agent deployment.

## FoxBrain Relevance
HINTBench's focus on intrinsic, non-attack safety failures is critically important for Foxconn's FoxBrain deployment in manufacturing control systems, where agent failures due to misplanning or constraint violations (not attacks) could cause production halts, safety incidents, or regulatory violations. The benchmark's three-task structure (detect → localize → classify) provides a progressive safety certification framework that FoxBrain agents should pass before being granted autonomous control over factory floor operations or supply chain execution systems. The finding that strong LLMs fail at step-level localization means FoxBrain's safety monitoring system needs dedicated failure-localization components, not just high-level risk classifiers. The five-constraint taxonomy offers a starting vocabulary for Foxconn's internal agent safety policy documentation.

---
*Back to [Main Digest](../README.md)*
