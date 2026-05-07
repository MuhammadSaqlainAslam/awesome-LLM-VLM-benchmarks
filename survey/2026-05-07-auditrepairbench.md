# AuditRepairBench: Evaluator-Channel Ranking Instability in Agent Repair Systems (2026)

## Problem
Agent repair leaderboards — used to rank and select agent systems that fix errors in execution traces — are systematically unreliable due to a hidden methodological flaw: repair candidates that improperly use evaluator signals during selection inflate their scores in evaluator-aligned conditions but fail when the evaluator configuration changes. This "evaluator-channel leakage" causes leaderboard rankings to reorder dramatically when the evaluator is reconfigured, meaning organisations selecting the best agent repair system based on leaderboard rankings may be deploying systems that perform very differently in production.

## Method
**AuditRepairBench** (arXiv: 2605.04624, May 2026) introduces a paired-execution trace corpus of **576,000 registered cells** (96,000 executed) designed to detect evaluator-channel-blocking ranking instability. A lighter variant — **AuditRepairBench-Lite** (12,000 cells) — enables practical iterative evaluation. Four screening implementations are compared: a learned influence proxy, a rule-based channel-exposure ratio, a counterfactual sensitivity proxy, and a sparse human-audit proxy. Screening-guided blinding patches are evaluated as a ranking stabilisation mechanism.

## Benchmarks / Datasets
- 576,000 registered cells (96,000 executed), AuditRepairBench-Lite: 12,000 cells
- Four screening implementations (learned / rule-based / counterfactual / human-audit)
- Paired-execution trace corpus for ranking stability testing
- Evaluator reconfiguration tests for leaderboard stability measurement

## Key Results

| Metric | Result |
|---|---|
| Rank displacement reduction (screening-guided blinding) | **55–74%** (mean 62%) |
| Independent discovery validation AUROC | **0.83** |
| Kendall τ preservation (AuditRepairBench-Lite) | **0.88** |
| Community-evaluator Spearman ρ (forward transfer) | **0.65** |

- **Screening-guided blinding patches reduce rank displacement by 55–74% (mean 62%) — leaderboard stability is achievable but requires active mitigation of evaluator-channel leakage**
- Independent discovery validation AUROC of 0.83 confirms the screening approach identifies genuine evaluator-channel leakage rather than overfitting to the corpus
- Kendall τ = 0.88 on the lite variant demonstrates that the lightweight 12,000-cell corpus preserves ranking fidelity at 70% lower evaluation cost
- Community-evaluator forward transfer (ρ = 0.65) shows moderate but imperfect generalisation — evaluator-specific calibration remains necessary

## Enterprise / Industry Relevance
Foxconn's FoxBrain infrastructure increasingly relies on automated agent repair and self-correction systems that are selected based on benchmark leaderboard performance. AuditRepairBench's finding that agent repair leaderboards reorder significantly under evaluator reconfiguration means the system FoxBrain selects as best-in-class on published benchmarks may perform very differently in Foxconn's actual production evaluator configuration. For FoxBrain's agent repair procurement and internal development decisions, this paper mandates evaluating repair systems under Foxconn's own evaluator configuration — not published leaderboard conditions — before deployment. The 62% mean rank displacement reduction from screening-guided blinding is directly applicable as a quality gate: FoxBrain's agent repair evaluation pipeline should implement channel-exposure screening to detect and exclude repair candidates that improperly optimise for the evaluator rather than genuine repair quality.

---
*Back to [Main Digest](../README.md)*
