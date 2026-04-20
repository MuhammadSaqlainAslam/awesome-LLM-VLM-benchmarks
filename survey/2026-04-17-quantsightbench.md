# QuantSightBench: Evaluating LLM Quantitative Forecasting with Prediction Intervals (2026)

## Problem
Existing LLM benchmarks focus on categorical or qualitative answers, leaving a critical gap in assessing numerical forecasting over continuous quantities. Calibration and uncertainty quantification — the ability to produce appropriately wide or narrow prediction intervals — are rarely tested, yet are essential for any deployment that requires probabilistic numerical reasoning. Prior work has not systematically measured whether LLMs achieve stated coverage targets across diverse real-world forecasting domains.

## Method
**QuantSightBench** (arXiv: 2604.15859, April 17, 2026) introduces a benchmark where models must provide numerical prediction intervals (lower bound, upper bound) at specified confidence levels rather than point estimates. The benchmark draws on diverse factual and empirical questions spanning science, economics, geography, and current events, evaluating both empirical coverage (whether the true answer falls inside the interval) and interval sharpness (how tight the intervals are). Eleven frontier and open-weight models were evaluated.

Authors: Jeremy Qin, Maksym Andriushchenko

## Benchmarks / Datasets
- Diverse set of numerical forecasting questions across science, economics, geography, and current events
- Evaluation protocol: prediction intervals at multiple confidence levels (e.g., 50%, 90%)
- 11 frontier and open-weight models evaluated including Gemini 3.1 Pro, Grok 4, and GPT-5.4
- Key metrics: empirical coverage rate, interval sharpness, calibration error at extreme magnitudes

## Key Results

| Model | 90% Coverage Rate | Notes |
|---|---|---|
| Gemini 3.1 Pro | 79.1% | Top performer |
| Grok 4 | 76.4% | Second best |
| GPT-5.4 | 75.3% | Strong but overconfident |
| Target | 90.0% | No model achieves this |

- **No model among 11 evaluated achieves the 90% coverage target; top performer (Gemini 3.1 Pro) reaches only 79.1%.**
- Systematic overconfidence across all models, particularly pronounced at extreme magnitudes (very large or very small values).
- Coverage degrades further at higher confidence levels (90% vs. 50%), indicating models fail to appropriately widen intervals for harder questions.

## FoxBrain Relevance
Foxconn's FoxBrain is increasingly deployed in supply-chain demand forecasting, component pricing, and yield prediction — all of which require numerical estimates with uncertainty bounds rather than simple point predictions. QuantSightBench provides a direct evaluation framework to stress-test FoxBrain's calibration on continuous numerical outputs before deployment in procurement or capacity-planning workflows. The systematic overconfidence at extreme magnitudes is particularly relevant to Foxconn's outlier-heavy production contexts (e.g., surge orders, rare material shortages). Incorporating interval-calibration evaluation into FoxBrain's pre-release checklist would directly reduce downstream financial risk from overconfident AI forecasts.

---
*Back to [Main Digest](../README.md)*
