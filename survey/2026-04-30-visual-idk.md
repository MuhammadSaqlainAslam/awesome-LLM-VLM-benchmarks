# Visual-Idk: Delineating Knowledge Boundaries for Honest Large Vision-Language Models (2026)

## Problem
Large vision-language models hallucinate by generating confident-sounding answers to questions that exceed their actual knowledge — particularly in specialised visual domains like medical imaging. No systematic methodology existed for identifying a VLM's precise knowledge boundaries from its own internal states, meaning deployed VLMs cannot reliably recognise and decline questions they cannot answer. This produces systems that appear highly capable in evaluation but generate dangerous misinformation in production.

## Method
**Visual-Idk** (arXiv: 2604.26419, April 30, 2026) introduces a model-specific benchmark construction methodology using multi-sample consistency probing: a question is sampled multiple times and if the model produces inconsistent answers, it is classified as "unknown." This builds a calibrated Visual-I-Don't-Know (Visual-Idk) dataset distinguishing known from unknown facts for each specific model. The framework then applies supervised fine-tuning with preference-aware optimisation (DPO and ORPO) to instil principled refusal behaviour, verified through internal probing to confirm the model genuinely recognises limits rather than memorising refusal patterns. Generalisation is tested across medical and perceptual domains.

## Benchmarks / Datasets
- Visual-Idk dataset (model-specific, built via multi-sample consistency probing)
- Evaluation domains: general visual Q&A, medical imaging, perceptual tasks
- Methods: supervised fine-tuning + DPO + ORPO preference optimisation
- Internal probing for genuine boundary recognition vs. pattern memorisation

## Key Results

| Metric | Baseline | After Intervention |
|---|---|---|
| Truthful Rate | 57.9% | 67.3% |
| Improvement | — | +9.4 percentage points |
| Boundary recognition | Memorised patterns | Genuine internal recognition |

- **A 9.4 percentage point improvement in Truthful Rate (57.9% → 67.3%) through knowledge boundary training — VLMs can be taught to genuinely recognise their limits rather than fabricate answers**
- Internal probing confirms the model's improved behaviour reflects genuine knowledge boundary awareness, not surface-level refusal pattern memorisation
- Generalises across medical and perceptual domains, suggesting the approach is modality- and domain-transferable
- Multi-sample consistency probing provides a principled, model-agnostic method for constructing "unknown question" datasets without human annotation

## Enterprise / Industry Relevance
Foxconn's use of FoxBrain for visual document analysis — reading engineering schematics, inspecting defect images, processing OCR'd invoices — creates direct exposure to the hallucination problem Visual-Idk addresses. A VLM that confidently answers questions about visual content it cannot reliably interpret is more dangerous than one that returns no answer. The 57.9% baseline Truthful Rate means that before boundary training, VLMs are unreliable roughly 42% of the time on questions they cannot actually answer. The multi-sample consistency probing methodology also provides FoxBrain teams with a practical, annotation-free technique to identify which visual question types exceed the deployed model's reliable knowledge — a critical audit step before any production VLM deployment at Foxconn.

---
*Back to [Main Digest](../README.md)*
