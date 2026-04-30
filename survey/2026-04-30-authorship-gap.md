# Authorship Gap: Theory-Grounded Evaluation Exposes the LLM Personalization Failure (2026)

## Problem
LLM stylistic personalization — adapting generated text to match a specific author's writing style — is evaluated using ad hoc metrics that produce inconsistent conclusions and are theoretically ungrounded. When different metrics disagree on whether a model has successfully personalized, there is no principled way to determine which metric is correct. This masks a fundamental capability gap: current LLMs may appear to personalize when evaluated with lenient metrics while failing badly against rigorous authorship science standards.

## Method
**Authorship Gap** (arXiv: 2604.26460, April 30, 2026) applies authorship verification theory to ground LLM personalization evaluation. Using 50 authors and 1,000 text generations, four inference-time personalization methods are assessed under three distinct measurement approaches: LUAR (a trained authorship verification model), an LLM-as-judge with decoupled trait matching, and classical function-word stylometrics. A human author ceiling (0.756) and cross-author floor (0.626) are established as calibrated reference points.

## Benchmarks / Datasets
- 50 authors, 1,000 text generations
- 4 inference-time personalization methods evaluated
- 3 evaluation approaches: LUAR, LLM-as-judge (trait matching), function-word stylometrics
- Calibrated baselines: human ceiling (0.756), cross-author floor (0.626)
- Domain: stylistic personalization evaluation

## Key Results

| Metric | Score |
|---|---|
| Human ceiling | 0.756 |
| Cross-author floor | 0.626 |
| All 4 personalization methods | 0.484–0.508 |
| Pairwise metric correlations | \|r\| < 0.07 (near zero) |

- **All four LLM personalization methods score below the cross-author floor (0.484–0.508 vs. floor 0.626) — current models cannot reliably personalize to a target author's style even by the minimum meaningful threshold**
- Pairwise correlations between evaluation metrics are near zero (|r| < 0.07) — different metrics measure fundamentally different things and cannot be used interchangeably
- The "authorship gap" is larger than previously recognised: models appear to personalize under lenient metrics but fall below floor-level performance under authorship-science-grounded evaluation
- Theory-grounded evaluation with calibrated baselines is essential; without human ceiling and floor references, any accuracy number is uninterpretable

## Enterprise / Industry Relevance
Foxconn and FoxBrain teams that use LLM personalization for customer-facing communications — adapting tone and style for different regions, business relationships, or communication contexts — face the capability gap this paper exposes. If FoxBrain is used to generate communications in a specific executive's voice or adapt materials to Foxconn's brand style guidelines, the Authorship Gap finding that all personalization methods score below the minimum meaningful threshold means these outputs will not achieve genuine stylistic consistency. More critically, the near-zero metric correlations mean that internally developed evaluation metrics for FoxBrain personalization quality are likely measuring something different from actual stylistic fidelity — a calibration step using authorship-grounded evaluation is essential before relying on any personalization quality scores.

---
*Back to [Main Digest](../README.md)*
