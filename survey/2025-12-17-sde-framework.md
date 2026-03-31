# SDE Framework: Evaluating Large Language Models in Scientific Discovery (2025)

## Problem
Existing science benchmarks (GPQA, SciEval) evaluate narrow factual recall rather than the full scientific discovery workflow — hypothesis generation, experimental design, and result interpretation. Without scenario-grounded evaluation defined by domain experts on genuine research projects, it is impossible to measure whether LLMs are approaching real scientific utility.

## Method
The **Scientific Discovery Evaluation (SDE)** framework is built around genuine research projects contributed by domain experts in biology, chemistry, materials science, and physics. Each project is decomposed into modular scenarios from which evaluation questions are sampled. Performance is measured at two levels: question-level accuracy and project-level holistic performance (covering hypothesis generation, experiment design, and result interpretation). The study involves 51+ co-authors across multiple institutions.

## Benchmarks / Datasets
- **SDE Framework:** Multi-domain scenario-grounded benchmark; biology, chemistry, materials science, physics.
- **Task Types:** Hypothesis generation, experimental design, result interpretation.
- **Evaluation Levels:** Question-level accuracy; project-level performance.
- **Metrics:** Accuracy per domain, per task type; project completion score.
- **GitHub:** https://github.com/HowieHwong/sde-harness

## Key Results
All current LLMs show consistent performance gaps versus general science benchmarks when evaluated on genuine discovery scenarios, with **diminishing returns from scaling** observable across the 51-co-author model set. Cross-model failure modes cluster around experimental design and result interpretation — the least textbook-like task types. The authors conclude that all current LLMs remain distant from scientific superintelligence.

## FoxBrain Relevance
A strategic benchmark for FoxBrain's R&D-assist positioning. If FoxBrain is intended to support materials science or process engineering research at Foxconn, SDE provides exactly the right evaluation framework — project-level scenarios that mirror actual research workflows rather than textbook QA. The experimental design failure mode is the highest-risk gap to close first.

---
*Back to [Main Digest](../README.md)*
