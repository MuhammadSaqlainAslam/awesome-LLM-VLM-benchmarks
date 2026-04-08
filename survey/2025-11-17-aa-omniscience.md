# AA-Omniscience: Evaluating Cross-Domain Knowledge Reliability in Large Language Models (2025)

## Problem
General-purpose benchmark rankings based on reasoning tasks do not reliably predict factual reliability. A model may score highly on complex reasoning benchmarks yet hallucinate frequently on domain-specific factual questions. There was no benchmark specifically measuring whether models have genuinely embedded knowledge — tested without retrieval tools — across the economically important domains where factual errors cause real-world harm.

## Method
A question generation agent derives questions from **authoritative academic and industry sources**, filtered by similarity, difficulty, and ambiguity. Models are evaluated without any context or external tools and are instructed to **abstain when uncertain** (a realistic production setting). Automated grading uses Gemini 2.5 Flash, classifying responses as correct, partially correct, incorrect, or not attempted. The **Omniscience Index (OI)** = 100 × (c − i) / (c + p + i + a), ranging from −100 to +100 — a score of zero means as many correct as incorrect answers, penalising overconfident wrong answers. **6,000 questions** span 6 domains representing **44% of U.S. wages**. Published by **Artificial Analysis** (arXiv: 2511.13029, November 2025).

## Benchmarks / Datasets
- **6,000 questions** across 6 domains and 42 subtopics
- **Domains:** Business; Humanities & Social Sciences; Health; Law; Software Engineering; Science, Engineering & Mathematics
- **Coverage:** 42 economically relevant subtopics representing 44% of U.S. wages (2024)
- **Metric:** Omniscience Index (OI): penalises wrong answers, rewards correct answers, accommodates abstentions
- **Evaluation:** No context or tools; model must draw on embedded knowledge only

## Key Results

**At publication (November 2025):** Only 3 models scored above zero on the Omniscience Index.

**Current leaderboard (April 2026):**

| Rank | Model | OI Score |
|---|---|---|
| 1 | Gemini 3.1 Pro Preview | **33** |
| 2 | Gemini 3 Pro Preview (high) | 16 |
| 3 | Claude Opus 4.6 (Adaptive Reasoning, Max Effort) | 14 |

Domain-level leaders: Claude 4.1 Opus leads in Law, Software Engineering, and Humanities; GPT-5.1 leads in Business; Grok 4 leads in Health and Science/Engineering/Mathematics.

**Key finding:** "Overall intelligence does not reliably predict strong embedded knowledge or low hallucination rates." Model selection should be domain-specific, not based on aggregate leaderboard rank.

## FoxBrain Relevance
AA-Omniscience's domain structure — particularly Law, Software Engineering, and Science/Engineering/Mathematics — maps to FoxBrain's highest-risk deployment contexts: compliance and regulatory reasoning (Law), code generation and debugging (Software Engineering), and process/materials analysis (Science/Engineering). The Omniscience Index's abstention penalty is production-critical for Foxconn: a model that confidently gives wrong legal or engineering answers is more dangerous than one that abstains. FoxBrain's production deployment gates should require a positive OI score (>0) on the relevant domain before any unsupervised agentic deployment in that vertical.

---
*Back to [Main Digest](../README.md)*
