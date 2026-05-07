# NoisyCausal: A Benchmark for Evaluating Causal Reasoning Under Structured Noise (2026)

## Problem
LLM causal reasoning benchmarks present clean, well-structured causal scenarios where the challenge is logical inference. Real-world causal analysis — in manufacturing root cause analysis, supply chain disruption diagnosis, medical differential diagnosis, or financial risk attribution — contains irrelevant distractors, confounded variables, partially observable states, and perturbed values that can mislead correlation-based reasoning. No benchmark tested whether LLMs can distinguish causation from correlation under realistic noisy conditions, leaving a critical blind spot for enterprise diagnostic applications.

## Method
**NoisyCausal** (arXiv: 2605.04313, May 2026) generates benchmark instances from **ground-truth causal graphs** contextualised with natural language scenarios, then injects **four controllable noise types**: (1) irrelevant distractors, (2) value perturbations, (3) confounding variables, and (4) partial observability. A framework combining LLMs with explicit causal structures is proposed as a mitigation. Generalisation is tested on the external **Cladder benchmark** without task-specific tuning.

## Benchmarks / Datasets
- Instances generated from ground-truth causal graphs (verifiable correctness)
- Natural language scenario contextualisation
- Four noise injection types: irrelevant distractors / value perturbations / confounding / partial observability
- External generalisation: Cladder benchmark
- Controllable noise parameterisation for difficulty scaling

## Key Results

| Condition | Performance |
|---|---|
| Standard LLM prompting under noise | Significantly degraded vs. clean |
| Reasoning baselines under noise | Significantly degraded vs. clean |
| Proposed causal structure + LLM | Significantly outperforms baselines |
| Generalisation to Cladder (zero-shot) | Strong generalisation without tuning |

- **Standard prompting and reasoning baselines show significant performance degradation under structured noise — LLMs conflate correlation with causation when distractors, confounders, or missing observations are introduced**
- The combination of explicit causal structure with LLM reasoning significantly outperforms both standard prompting and reasoning baselines on NoisyCausal
- Strong zero-shot generalisation to Cladder benchmark confirms the approach is robust rather than overfitted
- The four noise types are independently controllable, enabling targeted diagnosis of which noise type causes the most severe reasoning failure for a given model

## Enterprise / Industry Relevance
Foxconn's most valuable FoxBrain use cases involve causal diagnosis: identifying root causes of production defects, diagnosing supply chain disruptions, attributing quality failures to specific process variables, and understanding the causal chain of equipment breakdowns. These tasks occur in exactly the noisy, partially observable, confounded environments that NoisyCausal tests. The finding that standard LLM reasoning degrades significantly under structured noise means FoxBrain's current root-cause-analysis prompting approaches are likely generating correlation-based explanations that appear causal but are not. For Foxconn's manufacturing quality analysis, integrating explicit causal structure (e.g., causal graphs of the production process with known variable relationships) into FoxBrain's reasoning framework — rather than relying on pure LLM reasoning — is the validated path to reliable causal diagnosis.

---
*Back to [Main Digest](../README.md)*
