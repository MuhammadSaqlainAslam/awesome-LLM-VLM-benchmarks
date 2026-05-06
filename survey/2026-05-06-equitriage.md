# EQUITRIAGE: A Fairness Audit of Gender Bias in LLM-Based Emergency Department Triage (2026)

## Problem
Emergency department triage is a high-stakes medical decision with documented human gender disparities — women are systematically undertriaged relative to men. As LLMs are adopted to assist or automate triage decisions, a critical question emerges: do these models replicate, amplify, or mitigate known gender biases? No systematic fairness audit had evaluated multiple frontier LLMs on a clinical triage task using counterfactual gender-swap methodology at scale.

## Method
**EQUITRIAGE** (arXiv: 2605.03998, May 2026) evaluates five frontier LLMs on the **MIMIC-IV-ED dataset** comprising **18,714 clinical vignettes** with **374,275 total evaluations**, including **9,346 gender-swapped counterfactual pairs** (identical cases with only patient gender changed). Five models are evaluated: Gemini-3-Flash, Nemotron-3-Super, DeepSeek-V3.1, Mistral-Small-3.2, and GPT-4.1-Nano. Two bias interventions are tested: demographic blinding (removing gender from input) and age-preserving blinding. The pre-registered threshold for acceptable fairness is a 5% flip rate (triage decisions that change when gender changes).

## Benchmarks / Datasets
- MIMIC-IV-ED dataset: 18,714 clinical vignettes
- 374,275 total evaluations
- 9,346 gender-swapped counterfactual pairs
- 5 frontier LLMs evaluated
- Pre-registered fairness threshold: ≤5% flip rate
- Interventions: demographic blinding / age-preserving blinding

## Key Results

| Model | Flip Rate | Direction |
|---|---|---|
| All five models | **9.9%–43.8%** | All exceed 5% threshold |
| DeepSeek-V3.1 | Highest bias | 2.15:1 Female/Male undertriage ratio |
| Gemini-3-Flash | Moderate bias | 1.34:1 Female/Male undertriage ratio |
| Gemini after demographic blinding | **0.5%** | Below threshold |
| DeepSeek after age-preserving blinding | 1.25:1 residual | Above threshold |

- **All five frontier models exceed the pre-registered 5% fairness threshold (range: 9.9%–43.8%) — no tested model is deployment-safe for clinical triage without bias mitigation**
- DeepSeek-V3.1 shows the most severe gender bias: 2.15:1 female-to-male undertriage ratio — women are more than twice as likely to be assigned lower urgency than identical male cases
- Demographic blinding eliminates Gemini's bias (0.5% flip rate) but DeepSeek maintains residual bias (1.25:1) even after age-preserving blinding — some models encode gender bias more deeply than others
- The wide flip rate range (9.9%–43.8%) shows large model-to-model variation in bias severity — model choice is a critical fairness variable

## Enterprise / Industry Relevance
Foxconn's occupational health systems, worker wellness programs, and factory safety alert routing increasingly use AI to prioritise health-related decisions. EQUITRIAGE's finding that all five tested frontier models produce gender-biased triage decisions — with flip rates up to 43.8% — is a direct warning for any FoxBrain deployment that routes or prioritises health or safety interventions by worker. The DeepSeek-V3.1 result (2.15:1 undertriage ratio) is particularly relevant given FoxBrain's consideration of DeepSeek-V4 for enterprise deployment. Demographic blinding is an effective but model-dependent mitigation: FoxBrain's health-sensitive workflows must remove protected demographic attributes from inputs, but this intervention must be validated per-model since DeepSeek maintains residual bias even after blinding. Any FoxBrain deployment touching worker health prioritisation requires a counterfactual fairness audit before production rollout.

---
*Back to [Main Digest](../README.md)*
