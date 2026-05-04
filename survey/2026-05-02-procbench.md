# ProcBench: When LLMs Stop Following Steps — Diagnostic Study of Procedural Execution (2026)

## Problem
LLM reasoning benchmarks measure final-answer correctness, but this conflates two distinct capabilities: getting the right answer (by any means) versus faithfully executing a specified procedure step by step. Enterprise and safety-critical deployments often require the latter — an LLM that arrives at the right answer via a shortcut or hallucinated intermediate steps is fundamentally unreliable for process compliance, auditing, and traceable decision-making. No diagnostic benchmark had separated procedural execution fidelity from final-answer accuracy.

## Method
**ProcBench** (arXiv: 2605.00817, May 2026) introduces a controlled diagnostic benchmark using step-wise arithmetic algorithms with numeric inputs, where complexity is varied by algorithm length (step count) and the dependency depth between intermediate variables. The benchmark spans **55 datasets across varying difficulty levels** and evaluates **14 language models**. Rather than measuring only final correctness, the evaluation captures full execution traces and categorises failure modes: missing answers, premature termination, self-corrections after errors, incomplete execution traces, and fabricated additional steps.

## Benchmarks / Datasets
- 55 datasets spanning varying procedure lengths and dependency depths
- 14 language models evaluated
- Step-wise arithmetic algorithms with numeric inputs (controlled, verifiable ground truth)
- Full execution trace evaluation (not just final answer)
- Failure mode taxonomy: missing / premature termination / self-correction / incomplete trace / fabricated steps

## Key Results

| Procedure Length | Average First-Answer Accuracy |
|---|---|
| 5 steps | 61% |
| 25 steps | ~45% (interpolated) |
| 55 steps | ~32% (interpolated) |
| 95 steps | 20% |

- **Accuracy collapses from 61% on 5-step procedures to 20% on 95-step procedures — a 41 percentage point drop driven purely by procedure length, not task difficulty**
- Five distinct failure modes identified: missing answers, premature termination, error-triggered self-corrections, incomplete execution traces, and fabricated extraneous steps — each with different implications for downstream system reliability
- Final-answer benchmarks mask procedural execution failures: a model can appear accurate on short-procedure versions of a task while completely failing the same task at production-relevant procedure lengths
- The degradation is continuous and predictable — procedure length is a reliable predictor of execution reliability independent of domain

## Enterprise / Industry Relevance
Foxconn's highest-value FoxBrain use cases include process-guided workflows: step-by-step quality inspection protocols, multi-stage procurement approval procedures, and sequential manufacturing process verification. ProcBench's finding that LLM execution accuracy drops from 61% to 20% as procedures grow from 5 to 95 steps is a direct reliability warning. Any FoxBrain deployment that asks a model to follow a multi-step operational procedure — particularly procedures with 20+ steps — must not rely on final-answer verification alone; step-by-step trace auditing is essential. FoxBrain's SOPs and process compliance workflows should be designed with procedure-length awareness: where possible, long procedures should be decomposed into shorter sub-procedures (≤10 steps) before LLM execution, with intermediate human verification checkpoints at stage boundaries.

---
*Back to [Main Digest](../README.md)*
