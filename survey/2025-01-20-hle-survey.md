# Humanity's Last Exam (HLE) (2025)

## Problem
Frontier benchmarks such as MMLU (now exceeded at ~90% by top models), GPQA, and AIME have become saturated — they no longer meaningfully separate frontier AI systems from each other or from genuine expert-level human reasoning. HLE is designed to be the hardest publicly available closed-ended benchmark in existence: a multi-disciplinary, expert-curated exam spanning over 100 subjects where no question can be answered by web search or simple retrieval, and where the best models at launch scored below 10%.

## Method
HLE was created by the **Center for AI Safety (CAIS)** and **Scale AI**, led by Dan Hendrycks, Alexandr Wang, and Summer Yue. Questions were solicited globally from nearly **1,000 subject-matter experts** (professors, researchers, and graduate degree holders) affiliated with over **500 institutions across 50 countries**, incentivised by a **$500,000 prize pool** ($5,000 per accepted question for the top 50, $500 for the next 500). Over **70,000 candidate questions** were submitted. These were reduced through a multi-stage pipeline — LLM pre-screening (must stump all frontier models), two rounds of graduate-level human expert review, and non-searchability verification — down to **2,500 final public questions**. A private held-out set exists separately. The benchmark was published on **arXiv January 24, 2025** (arXiv:2501.14249) and subsequently published in ***Nature*, Vol. 649, January 2026**.

## Benchmarks / Datasets
- **HLE Public Set:** 2,500 questions spanning 100+ subjects
  - **~90% text-only** questions (short-answer exact-match and multiple-choice)
  - **~10% multimodal** (image + text, approximately 250 questions) — per the Nature-published version
  - Format: ~80% short-answer/exact-match, ~20% multiple-choice
- **Domain breakdown:** Mathematics (41%), Biology/Medicine (11%), Computer Science/AI (10%), Physics (9%), Humanities/Social Science (9%), Chemistry (7%), Engineering (4%), Other (9%)
- **Calibration benchmarks referenced:** MMLU, GPQA Diamond, MATH, AIME, ARC-AGI

## Key Results
At initial release (January 2025), all models scored dramatically below human expert performance (~90% in-domain):

| Model | Accuracy |
|---|---|
| GPT-4o | **2.7%** |
| Grok 2 | **3.0%** |
| Claude 3.5 Sonnet | **4.1%** |
| Gemini 1.5 Pro | **4.6%** |
| Gemini 2.0 Flash Thinking | **6.6%** |
| o1 | **8.0%** |
| DeepSeek-R1 *(text-only)* | **8.5%** |
| o3-mini high *(text-only)* | **13.4%** |
| **Human expert (own domain)** | **~90%** |

All models were severely miscalibrated — expressing high confidence (~87–89% RMS calibration error) while being almost entirely wrong.

**Current SOTA (April 2026):** GPT-5.4-pro scores **~44.3%** (Scale Labs leaderboard), up from sub-10% at launch. Claude Opus 4.6 (thinking-max) reaches ~34.4%. Despite rapid progress, the human expert ceiling of ~90% remains far out of reach.

## FoxBrain Relevance
HLE is the ideal "north star" ceiling benchmark for FoxBrain. Its domain breakdown (41% mathematics, 10% CS/AI, 9% physics, 7% chemistry, 4% engineering) maps closely to Foxconn's core R&D verticals. Because every question is verified non-searchable and must stump all frontier models at time of collection, a strong HLE score provides genuine evidence of deep reasoning — not retrieval. FoxBrain should be tracked against the HLE Mathematics and Engineering subsets specifically, as these are the most production-relevant and least likely to be affected by the ground-truth quality concerns flagged in the Chemistry/Biology domains.

---
*Back to [Main Digest](../README.md)*
