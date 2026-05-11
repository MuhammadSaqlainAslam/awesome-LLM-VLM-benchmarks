# Beyond Confidence: Rethinking Self-Assessments for Performance Prediction in LLMs (2026)

## Problem
Confidence — the model's stated certainty about its answer — is the standard self-assessment metric used to predict LLM correctness. It has a well-documented failure mode: confidence is consistently overoptimistic, poorly calibrated, and unstable across model sizes and task types. A model that says "I'm 90% confident" is often no more accurate than one that says "I'm 60% confident," making confidence an unreliable routing signal for high-stakes outputs. No systematic study had evaluated whether alternative self-assessment dimensions from cognitive psychology could outperform confidence for correctness prediction across diverse LLM families and task domains.

## Method
**Beyond Confidence** (arXiv: 2605.07806, May 2026) draws from **cognitive appraisal theory** to develop a **multidimensional self-assessment framework**. Six appraisal-based dimensions are elicited alongside traditional confidence: including **effort** (how hard the model worked on the answer) and **ability** (the model's self-assessed competence for the task type). Evaluations span **12 LLMs**, **38 distinct tasks**, and **8 domains**, enabling task-type and model-size interaction analyses.

## Benchmarks / Datasets
- 12 LLMs evaluated
- 38 distinct tasks across 8 domains
- 6 appraisal dimensions + confidence (7 total self-assessment signals)
- Task-type breakdown: reasoning-intensive vs. retrieval-oriented

## Key Results

| Self-Assessment Dimension | Performance vs. Confidence | Key Property |
|---|---|---|
| Effort | Matches or outperforms | Less overoptimistic; stable across model sizes |
| Ability | Matches or outperforms | Dominant for retrieval-oriented tasks |
| Confidence | Baseline | Overoptimistic; unstable; best for retrieval |
| Multi-dimensional fusion | Consistently best | Outperforms any single dimension |

- **Effort and ability consistently match or outperform confidence across most task types — structured multidimensional self-assessment dominates single-dimension confidence**
- Effort provides **less overoptimistic estimates that remain stable across model sizes** — unlike confidence, which inflates with model size
- Task-dependent signal: effort is most predictive for reasoning-intensive tasks; ability and confidence are strongest for retrieval-oriented tasks — self-assessment strategy should vary by task type
- Across 12 models and 38 tasks, multidimensional self-assessment improves correctness prediction reliability over confidence-only approaches

## Enterprise / Industry Relevance
FoxBrain uses confidence-based routing to flag low-certainty outputs for human review in quality assurance and compliance workflows. Beyond Confidence's finding that confidence is overoptimistic and unstable means FoxBrain's human-review routing is currently under-routing uncertain outputs — the model says "high confidence" when it should flag for review. Replacing confidence-only routing with effort + ability multidimensional self-assessment would immediately improve FoxBrain's routing accuracy. Concretely: for FoxBrain's reasoning-intensive tasks (multi-step compliance checks, engineering requirement analysis), effort-based routing should be the primary signal; for retrieval-oriented tasks (document lookup, specification extraction), ability and confidence remain valid. The 12-model, 38-task scope of this study provides sufficient generalisation confidence to adopt this recommendation across FoxBrain's diverse task portfolio without domain-specific re-evaluation.

---
*Back to [Main Digest](../README.md)*
