# TPS-CalcBench: A Benchmark and Diagnostic Evaluation Framework for LLM Analytical Calculation Competence in Hypersonic Thermal Protection System Engineering (2026)

## Problem
LLMs are increasingly used to assist aerospace engineers with closed-form analytical calculations, but no benchmark exists for this safety-critical domain. Standard math benchmarks do not capture the formula-selection nuance and domain-specific physical reasoning required for hypersonic aerodynamics and high-temperature gas dynamics, leaving engineers without a reliable tool to assess LLM competence before deployment.

## Method
**TPS-CalcBench** (arXiv: 2604.17966, April 20, 2026) constructs a dual-track evaluation dataset of 420 core items and 810 pre-gating items (from 4,560 raw data points) covering 8 categories across 4 difficulty levels in hypersonic thermal protection system (TPS) engineering. Thirteen models from 7 groups are evaluated, and three intervention strategies are tested: DFA-TPS fine-tuning, RAG-EQ retrieval grounding, and PA-CoT process-aware prompting.

Authors: Jinglai Zheng, Chuhan Qiao, Haiming Huang

## Benchmarks / Datasets
- 420 core items + 810 pre-gating items from 4,560 raw data points
- 8 calculation categories across 4 difficulty levels
- 13 models from 7 groups evaluated
- Key metrics: KPI Score (0–100%), Formula Selection Accuracy, Intervention Improvement Delta

## Key Results

| Model / Condition | KPI Score Range |
|---|---|
| Baseline (13 models) | 12.6% – 87.9% |
| + DFA-TPS Fine-Tuning | Improved |
| + RAG-EQ Retrieval | Improved |
| + PA-CoT Prompting | Improved |

- **KPI scores range from 12.6% to 87.9% across 13 evaluated models, revealing large variance in engineering calculation competence**
- Hidden formula-selection defects are identified: models appear correct on intermediate steps but select wrong governing equations
- All three intervention methods (fine-tuning, RAG, CoT) provide meaningful improvements; combining them yields best results
- Data-driven ranking of intervention strategies varies by difficulty tier, indicating no universal best approach

## Enterprise / Industry Relevance
Foxconn operates advanced manufacturing facilities that involve thermal management, materials stress analysis, and precision engineering calculations for electronics and server hardware assembly. TPS-CalcBench's diagnostic framework — particularly its formula-selection defect detection and difficulty-stratified evaluation — is directly applicable to auditing FoxBrain's performance on mechanical and thermal engineering calculations used in product design review and process engineering. The benchmark's three intervention strategies (RAG-EQ, PA-CoT, domain fine-tuning) provide a concrete roadmap for improving FoxBrain's reliability on closed-form analytical tasks in Foxconn's advanced manufacturing R&D workflows. Adopting TPS-CalcBench methodology for a FoxBrain-Engineering variant would establish safety gates before deploying LLM-assisted calculation in production-critical contexts.

---
*Back to [Main Digest](../README.md)*
