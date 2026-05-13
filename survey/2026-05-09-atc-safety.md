# ATC Safety Evaluation: Consequence-Aware LLM Evaluation for Air Traffic Control (2026)

## Problem
LLMs evaluated on safety-critical communication tasks achieve high aggregate accuracy metrics (macro-F1, accuracy) while remaining operationally unreliable in ways that aggregate metrics completely hide. Air traffic control (ATC) is the canonical case: a model that correctly classifies 95% of communication types but systematically misidentifies runway identifiers — a high-consequence error category — would score well on macro-F1 while causing catastrophic real-world risk. Standard evaluation frameworks treat all errors equally, making them structurally incapable of detecting this pattern. The finding applies broadly: any safety-critical domain with asymmetric error consequences requires consequence-aware evaluation, not aggregate accuracy.

## Method
**ATC Safety Evaluation** (arXiv: 2605.11769, May 2026) proposes a **consequence-aware evaluation framework** that weights errors by their operational impact rather than treating all mistakes uniformly. A **Peak Risk Score** is defined as the highest-severity error rate across the most safety-critical entity categories (runway identifiers, altitude instructions, clearance types). The framework is applied to multiple LLMs evaluated on clean ATC transcripts, enabling direct comparison of aggregate accuracy (misleading) versus consequence-weighted risk (operational reality).

## Benchmarks / Datasets
- Clean ATC transcripts from operational air traffic control
- Consequence-weighted error taxonomy (safety-critical vs. routine entities)
- Peak Risk Score metric (highest-severity error category rate)
- Multiple LLMs evaluated under operational ATC conditions

## Key Results

| Metric | Value | Interpretation |
|---|---|---|
| Peak Risk Score (best model) | **0.69** | High-severity error rate unacceptable for ATC deployment |
| Models scoring below 0.6 Risk Score | **Most models** | Despite high macro-F1 performance |
| Aggregate macro-F1 | High (misleading) | Does not capture safety-critical failures |
| Structural grounding deficit | Universal | Errors concentrate in high-impact entity categories |

- **Peak Risk Score reaches 0.69 for the best model — most models score below 0.6 despite high macro-F1 performance — aggregate accuracy systematically hides operational unreliability in safety-critical domains**
- Errors concentrate in **high-impact entity categories** (runway identifiers, altitude specifications) while relatively stable action-type classification inflates aggregate metrics
- The macro-F1 / consequence-risk divergence is structural: standard evaluation frameworks are epistemically incapable of detecting domain-specific error asymmetry
- The consequence-aware evaluation framework is domain-agnostic — applicable to any safety-critical LLM deployment with asymmetric error consequences

## Enterprise / Industry Relevance
Foxconn's factory safety systems, quality assurance automation, and equipment operation instruction parsing all involve asymmetric-consequence error categories: a FoxBrain model misclassifying a production line safety override has far greater consequences than misclassifying a non-critical process parameter. The ATC study's core finding — that aggregate accuracy metrics hide dangerous concentrations of errors in high-consequence categories — directly applies to any Foxconn FoxBrain deployment in safety-critical manufacturing contexts. For FoxBrain's quality inspection systems: a high overall detection rate that masks a systematic failure to flag a specific critical defect type (e.g., PCB short circuits vs. cosmetic scratches) would score well on aggregate metrics while producing unacceptable operational risk. Foxconn should adopt consequence-weighted evaluation (equivalent to the Peak Risk Score framework) for all FoxBrain deployments where error categories have asymmetric consequences.

---
*Back to [Main Digest](../README.md)*
