## Problem
Traditional mathematical benchmarks are static and quickly become part of the training data (contamination), making it impossible to measure true out-of-distribution reasoning.

## Method
**LemmaBench** uses a "Live arXiv" pipeline that automatically pulls new, unreleased mathematical lemmas from daily preprints and converts them into formal synthesis tasks for LLMs.

## Benchmarks / Datasets
- **Benchmark:** LemmaBench (Dynamic)
- **Dataset:** Live arXiv Math/Physics preprints (2026)
- **Metrics:** Pass@1 Accuracy, Rigorous Proof Verification

## Key Results
Frontier models that score 90%+ on GSM8K drop significantly to **12.4% Pass@1** on LemmaBench, highlighting the gap between memorization and novel mathematical reasoning.

## FoxBrain Relevance
We should benchmark LemmaBench for our internal R&D. It provides a "moving target" that ensures FoxBrain’s mathematical logic is genuinely improving rather than just memorizing public datasets.

---
*Back to [Main Digest](../README.md)*
