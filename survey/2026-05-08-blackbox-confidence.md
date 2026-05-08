# Black-Box CoT Confidence: Geometry, Coverage, and Verbalization for Reasoning Trajectory Confidence (2026)

## Problem
Confidence estimation for chain-of-thought reasoning is essential for safe deployment — systems that know when they are uncertain can route low-confidence outputs to human review. White-box confidence methods require access to model logits or internal activations unavailable from commercial API deployments. Black-box self-consistency sampling (running the model multiple times and measuring agreement) is the standard alternative, but it multiplies inference cost by the sample count and fails to account for reasoning path geometry — whether the model is converging toward an answer or wandering. A cheaper, more informative black-box confidence method is needed.

## Method
**Black-Box CoT Confidence** (arXiv: 2605.06308, May 2026) proposes a trajectory-confidence scoring method that embeds chain-of-thought reasoning text as **sliding-window sequences** and measures convergence toward answer anchors — requiring no logits or calibration data. Confidence is decomposed into **three independent channels**: (1) **Coverage** — breadth of reasoning paths explored, (2) **Geometry** — convergence trajectory toward the final answer, (3) **Verbalization** — explicit confidence language in the reasoning text. Fusion of the three channels is evaluated against self-consistency baselines on **MedQA-USMLE, GPQA Diamond, and MMLU-Pro** using **Gemini 3.1 Pro and Claude Sonnet 4.6**.

## Benchmarks / Datasets
- MedQA-USMLE (medical licensing questions)
- GPQA Diamond (expert-level science)
- MMLU-Pro (professional knowledge)
- Models: Gemini 3.1 Pro, Claude Sonnet 4.6
- No logits or calibration data required (pure text API)

## Key Results

| Method | Samples Required | Median AUC |
|---|---|---|
| Self-consistency (K=8) | 8 | 0.71 |
| Proposed method (K=4) | 4 | **0.78** |
| Improvement | −50% compute | +0.075 AUC |

- **Proposed method achieves median AUC 0.78 vs. self-consistency 0.71 at K=4 samples — outperforming K=8 self-consistency at half the compute cost**
- Three-channel decomposition (Coverage + Geometry + Verbalization) enables interpretable uncertainty diagnosis: is the model uncertain because it explored little, diverged in reasoning, or expressed hedging language?
- No logits or calibration data required — applicable to any text-generating commercial API including GPT, Claude, Gemini, and open API endpoints
- Validated on three expert-level benchmarks covering medical, scientific, and professional knowledge domains

## Enterprise / Industry Relevance
FoxBrain's production deployment needs reliable, low-cost confidence estimation to route uncertain outputs to human review — particularly in high-stakes domains like quality assessment, regulatory compliance, and supplier risk evaluation. The proposed method's +0.075 AUC improvement at 50% compute reduction versus self-consistency is directly actionable: FoxBrain can implement sliding-window trajectory confidence scoring using existing API text outputs with no additional model access or calibration. The three-channel decomposition adds interpretability value beyond a scalar uncertainty score: when FoxBrain flags a low-confidence output, knowing whether the uncertainty originates from narrow Coverage (model didn't explore alternatives), divergent Geometry (reasoning trajectory was inconsistent), or explicit Verbalization (model hedged in its reasoning) enables different human review strategies. For Foxconn's quality and compliance review workflows, this interpretable confidence signal is more actionable than a generic "uncertain" flag.

---
*Back to [Main Digest](../README.md)*
