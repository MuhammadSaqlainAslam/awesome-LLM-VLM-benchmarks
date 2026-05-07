# Deployment-Relevant Alignment Cannot Be Inferred from Model-Level Evaluation Alone (2026)

## Problem
AI alignment research and enterprise AI governance rely on model-level benchmark scores as proxies for real-world safety — a model that passes TruthfulQA, HarmBench, or MMLU-safety variants is assumed to be aligned for deployment. This paper demonstrates that this inference is fundamentally invalid: model-level evaluations measure fixed outputs for isolated prompts, but deployment safety depends on interactive, dynamic behaviour across diverse users, scaffolds, and contexts. The alignment claim is made at the wrong level of abstraction.

## Method
**Deployment-Relevant Alignment** (arXiv: 2605.04454, May 2026) conducts a comprehensive audit of **eleven alignment benchmarks** (expanded to sixteen in analysis) across four evaluation levels — model, response, interaction, and deployment — and stress-tests scaffold efficacy across **three frontier models and four scaffolds** using **180 interaction transcripts**. The paper identifies which benchmarks operate at which evaluation level, maps gaps in interactional coverage, and demonstrates empirically that scaffold effectiveness is model-dependent using cross-model transcript analysis.

## Benchmarks / Datasets
- Audit of 11 alignment benchmarks (expanded to 16)
- Four evaluation levels: model / response / interaction / deployment
- Stress test: 3 frontier models × 4 scaffolds / 180 interaction transcripts
- Interactional benchmarks identified: tau-bench, CURATe, Rifts, Common Ground
- Domain: AI alignment evaluation methodology

## Key Results

| Evaluation Dimension | Finding |
|---|---|
| User-facing verification support across 16 benchmarks | **Absent in every benchmark** |
| Process steerability measurement | **Nearly absent** |
| Interactional benchmarks identified | Only **4** (tau-bench / CURATe / Rifts / Common Ground) |
| Scaffold efficacy across models | **Model-dependent** — same scaffold, dramatically different effectiveness |
| Alignment claims at correct level | Rarely matched to evaluation evidence |

- **User-facing verification support is absent across every examined alignment benchmark — no current standard benchmark measures whether users can verify or steer model behaviour during deployment**
- Only 4 interactional benchmarks exist out of 16 examined — the vast majority of alignment evaluation operates at model or response level, missing the deployment-relevant interaction level
- Scaffold efficacy is model-dependent: the same verification or safety scaffold produces dramatically different effectiveness across different frontier models — scaffold selection is not model-agnostic
- Alignment claims require evidence matched to the level of claim: model-level evidence cannot support deployment-level safety assertions

## Enterprise / Industry Relevance
This paper directly challenges the validity of Foxconn's FoxBrain alignment certification process. If FoxBrain's enterprise AI governance team certifies a model as "aligned" based on model-level benchmark performance (TruthfulQA, safety evaluations, MMLU-safety), this paper demonstrates that such certification does not predict interaction-level or deployment-level safety in FoxBrain's actual operating environment. The scaffold-efficacy finding is particularly critical: FoxBrain's prompt engineering, system prompt guardrails, and retrieval scaffolds may perform very differently across model versions — a scaffold proven effective on Claude Opus 4.6 cannot be assumed effective on Claude Opus 4.7 without re-validation. FoxBrain's governance framework must adopt interaction-level and deployment-level evaluation (using tau-bench or CURATe equivalents in Foxconn's domain) alongside model-level scores before any production deployment certification.

---
*Back to [Main Digest](../README.md)*
