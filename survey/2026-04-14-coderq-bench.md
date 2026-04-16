# CodeRQ-Bench: Beyond Output Correctness — Benchmarking and Evaluating LLM Reasoning in Coding Tasks (2026)

## Problem
Existing code evaluation benchmarks measure only output correctness (does the code run and pass tests?) while completely ignoring the quality and validity of the reasoning process that produced the code. This creates a blind spot: an LLM may arrive at a correct answer through flawed reasoning, or produce plausible-looking but semantically incorrect reasoning for a right answer. No benchmark systematically evaluated reasoning quality across all major coding task categories.

## Method
**CodeRQ-Bench** (arXiv: 2604.12379, April 14, 2026) introduces a benchmark evaluating LLM reasoning quality in coding tasks spanning three categories: code generation, code summarization, and code classification. The authors analyze over 1,069 mismatch cases where existing evaluators produce discrepant assessments, and propose VERA — a two-stage evaluator combining evidence-grounded verification with ambiguity-aware score correction — to enable more reliable reasoning quality assessment across four datasets.

Authors: Yuangang Li, Justin Tian Jin Chen, Ethan Yu, David Hong, Iftekhar Ahmed

## Benchmarks / Datasets
- 3 coding task categories: generation, summarization, classification
- 4 benchmark datasets evaluated
- 1,069 mismatch cases analyzed from existing evaluators
- VERA evaluator: two-stage (evidence-grounded verification + ambiguity-aware correction)
- Open-source release on GitHub

## Key Results

| Evaluator | AUCROC Improvement | AUPRC Improvement |
|---|---|---|
| VERA vs. baselines | Up to +0.26 | Up to +0.21 |
| VERA (all 4 datasets) | Consistent improvement | Consistent improvement |
| Strong baselines | Lower ceiling | Limited ambiguity handling |

- VERA achieves improvements of up to 0.26 AUCROC and 0.21 AUPRC over strong baseline evaluators across all four datasets.
- Analysis of 1,069 mismatch cases reveals systematic patterns where existing evaluators disagree, illuminating where reasoning quality measurement is most unreliable.
- Ambiguity-aware score correction in VERA's second stage is the key differentiator, handling edge cases that evidence-grounded verification alone misses.

## FoxBrain Relevance
CodeRQ-Bench is directly applicable to FoxBrain's software engineering support capabilities, where code generated for manufacturing automation, ERP integrations, and IoT device management must not only be functionally correct but produced through sound reasoning — particularly important for safety-critical factory control systems. The three-category evaluation (generation, summarization, classification) covers the full range of FoxBrain's coding assistance use cases, from generating automation scripts to summarizing legacy codebase documentation. VERA's ambiguity-aware evaluation approach can be adapted for FoxBrain's internal code review pipelines to detect AI-generated code with superficially correct outputs but unreliable reasoning. The benchmark's mismatch-case analysis methodology provides a framework for auditing FoxBrain's coding outputs before deployment in production manufacturing systems.

---
*Back to [Main Digest](../README.md)*
