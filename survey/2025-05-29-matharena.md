# MathArena: Evaluating LLMs on Uncontaminated Math Competitions (2025)

## Problem
Existing math benchmarks suffer from data contamination — models may have seen problems during training, inflating apparent performance. There was no reliable, contamination-free benchmark for evaluating LLMs on competition mathematics at the moment of release, and no systematic framework for evaluating proof-writing ability on Olympiad-level problems such as the IMO and USAMO.

## Method
MathArena leverages **recurring, freshly released math competitions**, evaluating models immediately after problems are publicly released to eliminate any contamination risk. For numerical-answer competitions (AIME, HMMT, BRUMO, CMIMC), automated answer-checking is used. For proof-based competitions (USAMO, IMO), human experts apply rubric-based scoring. 50+ models are evaluated across 7 competitions covering 162 problems. The paper also documents strong signs of contamination in AIME 2024 results, validating the need for real-time evaluation. Published at **NeurIPS 2025 Datasets and Benchmarks Track** by SRI Lab, ETH Zürich.

## Benchmarks / Datasets
- **7 competitions, 162 problems total:**
  - AIME 2025 (30 problems)
  - HMMT February 2025 (30 problems)
  - CMIMC 2025 (40 problems)
  - BRUMO 2025 (30 problems)
  - USAMO 2025 (6 problems)
  - IMO 2025 (6 problems — proof-writing)
  - Project Euler (20+ problems)
- **50+ models evaluated**
- Live leaderboard: matharena.ai

## Key Results

**Numerical competitions (avg. across AIME, HMMT, BRUMO, CMIMC):**

| Model | Accuracy |
|---|---|
| GPT-5 (high) | **91.25%** |
| Grok 4 Fast | 90.57% |
| Grok 4 | 90.36% |
| GPT OSS 120B | 89.32% |
| DeepSeek-V3.2 | 88.28% |
| Human Top 1% (AIME) | 84.35% |
| Human Top 1% (HMMT) | 66.79% |

**IMO 2025 proof-writing (max 42 points, rubric-scored by experts):**

| Model | Score |
|---|---|
| GPT-5 | **16.00 / 42 (38%)** |
| Gemini 2.5 Pro | 13.25 / 42 |
| o3 | 7.00 / 42 |
| o4-mini | 6.00 / 42 |
| Grok 4 | 5.00 / 42 |

Frontier models now surpass the human 99th percentile on numerical competitions — yet score only ~38% on formal IMO proof-writing. Contamination was confirmed in AIME 2024 but not 2025.

## FoxBrain Relevance
MathArena's contamination-free, live-release methodology is the gold standard for unbiased LLM evaluation and directly applicable to FoxBrain's internal benchmarking pipeline. The numerical competition format (automated exact-match scoring) can be adapted for Foxconn's engineering calculation validation tasks. The dramatic gap between numerical accuracy (~90%) and proof-writing ability (~38%) mirrors FoxBrain's likely gap between formulaic computation and multi-step engineering reasoning — a key capability to develop before deploying FoxBrain on complex design or optimisation problems.

---
*Back to [Main Digest](../README.md)*
