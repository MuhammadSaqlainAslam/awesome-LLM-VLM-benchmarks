# Thunder-NUBench: A Benchmark for LLMs' Sentence-Level Negation Understanding (2025)

## Problem
Negation is a fundamental linguistic phenomenon, yet existing NLI benchmarks treat it as incidental rather than as a first-class test of language understanding. Without a dedicated benchmark distinguishing standard negation from structurally diverse alternatives, it is impossible to measure whether LLMs truly understand negation or simply pattern-match surface cues.

## Method
Thunder-NUBench targets sentence-level negation understanding by contrasting standard negation against three structural alternatives: local negation, contradiction, and paraphrase. Sentence pairs are manually curated (not LLM-generated) to ensure quality and avoid annotation artifacts. The benchmark features 1,261 multiple-choice test items from 5,083 total instances. Accepted to EACL 2026.

## Benchmarks / Datasets
- **Thunder-NUBench:** 5,083 total instances; 1,261 multiple-choice test items; 3,772 training pairs.
- **Categories:** Standard negation vs. Local negation / Contradiction / Paraphrase.
- **Format:** Multiple-choice (4-way classification).
- **Metrics:** Accuracy per category; overall negation understanding score.
- **Dataset:** HuggingFace `thunder-research-group/SNU_Thunder-NUBench`

## Key Results
All tested LLMs show systematic confusion between standard negation and local negation — the most structurally similar category. Models with strong NLI performance do not reliably transfer that ability to fine-grained negation disambiguation, confirming that current LLMs do not robustly understand sentence-level negation.

## FoxBrain Relevance
Relevant for FoxBrain deployments in quality control, regulatory compliance, or contractual text analysis where negation errors carry real operational risk (e.g., "the component does NOT meet spec" vs. "the component meets spec"). FoxBrain should be evaluated on Thunder-NUBench before any deployment where negation errors could propagate to downstream decisions.

---
*Back to [Main Digest](../README.md)*
