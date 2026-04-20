# Do Vision-Language Models Truly Perform Vision Reasoning? A Rigorous Study of the Modality Gap (2026)

## Problem
Vision-language models (VLMs) consistently score well on multimodal benchmarks, but it is unclear whether this reflects genuine visual reasoning or merely strong language priors. Existing benchmarks mix visual and textual information in ways that allow models to succeed by ignoring the visual modality entirely. There is no controlled framework that holds task-relevant information constant across text-only, image-only, and combined modalities to isolate true visual reasoning from language-driven shortcuts.

## Method
**CrossMath** (arXiv: 2604.16256, April 17, 2026) is a multimodal mathematical reasoning benchmark that constructs the same problems in three formats: text-only, image-only, and image+text, with identical task-relevant content across formats. This controlled design allows direct measurement of modality-specific performance drops. The authors also release a fine-tuning dataset for targeted improvement. The benchmark evaluates leading VLMs including GPT-4o, Gemini 3.1 Pro, and open-source alternatives.

Authors: Yige Xu, Yongjie Wang, Zizhuo Wu, Kaisong Song, Jun Lin, Zhiqi Shen

## Benchmarks / Datasets
- Mathematical reasoning problems in 3 controlled formats: text-only, image-only, image+text
- Same task-relevant information preserved across all format variants
- Leading VLMs evaluated: GPT-4o, Gemini 3.1 Pro, Claude, and open-source models
- Training dataset released for fine-tuning VLMs on CrossMath problems
- Key metrics: accuracy per modality format, modality gap (text-only minus image-inclusive accuracy)

## Key Results

| Modality Format | Typical VLM Accuracy | Finding |
|---|---|---|
| Text-only | High | Models rely on language priors |
| Image-only | Degraded | Visual reasoning rarely triggered |
| Image + Text | Frequently worse than text-only | Visual input often hurts |

- **VLMs excel with text-only inputs but incorporating visual data frequently degrades performance — models conduct reasoning primarily in textual space.**
- Targeted fine-tuning on CrossMath problems improves accuracy across all modality combinations and generalizes to other visual reasoning benchmarks.
- The modality gap is consistent across model families, suggesting a systemic architectural limitation rather than a model-specific failure.

## FoxBrain Relevance
FoxBrain is being evaluated for manufacturing inspection workflows where visual inputs (PCB images, assembly photos, defect scans) must drive reasoning decisions rather than serve as background context. CrossMath's finding that VLMs default to text-space reasoning even when images are present is a critical risk signal: FoxBrain's visual QC pipeline may be silently ignoring key image evidence. Running CrossMath-style controlled modality ablations on FoxBrain's multimodal inspection tasks would verify whether the visual branch is genuinely contributing to fault detection or whether text-based heuristics are masking a latent visual reasoning gap. Fine-tuning on image-grounded tasks (analogous to CrossMath's training set) could close this gap before production deployment.

---
*Back to [Main Digest](../README.md)*
