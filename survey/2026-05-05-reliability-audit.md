# Multi-Variant Reliability Audit: What Single-Prompt Accuracy Misses in LLM Evaluation (2026)

## Problem
Standard LLM benchmarks report single-prompt accuracy — one question phrasing, one evaluation run — and treat this number as a stable measure of model capability. This practice systematically hides reliability failures that are immediately apparent in production: the same model answers the same question correctly with one phrasing and incorrectly with a slightly different one. Single-prompt accuracy cannot detect this instability, producing benchmark leaderboards that misrepresent real deployment reliability.

## Method
**Multi-Variant Reliability Audit** (arXiv: 2605.02038, May 2026) evaluates **15 open-weight language models** (10 instruct-tuned variants analysed in depth) across **five classification and reasoning benchmarks** — including MMLU-Pro and ARC-Challenge — using **five prompt variants per benchmark**. Four reliability dimensions are measured: accuracy, calibration, confidence parsing, and prompt-perturbation resilience. The study tests whether model size predicts robustness and whether chain-of-thought (CoT) prompting consistently improves reliability.

## Benchmarks / Datasets
- 5 benchmarks: includes MMLU-Pro, ARC-Challenge, and others
- 5 prompt variants per benchmark
- 15 open-weight models (10 instruct-tuned variants analysed)
- 4 reliability dimensions: accuracy / calibration / confidence parsing / prompt-perturbation resilience

## Key Results

| Finding | Measurement |
|---|---|
| Calibration error sensitivity to metric definition | Mean absolute difference of 0.149 |
| CoT prompting impact on ARC-Challenge accuracy | −72% to −88% reduction across primary models |
| Model size vs. prompt robustness correlation | −0.244 to +0.474 (no consistent relationship) |
| MMLU-Pro confidence vs. actual accuracy | Substantially overconfident across all models |

- **Chain-of-thought prompting reduces accuracy by 72–88% on ARC-Challenge across primary models — CoT is not universally beneficial and can dramatically harm performance on certain task types**
- Model size does not predict prompt robustness: correlation ranges from −0.244 to +0.474 across benchmarks — bigger is not reliably more robust
- Confidence calibration signals are fragile: switching calibration metric definitions shifts per-cell measurements by a mean absolute 0.149 — published calibration numbers are methodology-dependent
- Models are substantially overconfident on MMLU-Pro — stated confidence far exceeds actual accuracy across all tested models

## Enterprise / Industry Relevance
FoxBrain's benchmark-based model selection decisions are based on single-prompt accuracy scores that this paper demonstrates can be deeply misleading. If FoxBrain selects a model based on its MMLU-Pro accuracy, that score may reflect a single prompt phrasing that happens to suit the model's training distribution — the actual production reliability may be substantially lower. The CoT finding is particularly critical: if FoxBrain's prompting strategy adds chain-of-thought reasoning to improve accuracy (a common default), this paper shows it can reduce accuracy by up to 88% on certain task types. Before deploying any model in production, FoxBrain teams should run a multi-variant reliability audit: test with at least 5 prompt variants per task type and measure prompt-perturbation resilience, not just peak single-prompt accuracy.

---
*Back to [Main Digest](../README.md)*
