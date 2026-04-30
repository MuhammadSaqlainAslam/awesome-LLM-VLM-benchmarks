# When Text Hijacks Vision: Benchmarking and Mitigating Text Overlay-Induced Hallucination in Vision Language Models (2026)

## Problem
Vision-language models hallucinate systematically when on-screen text contradicts the actual visual content of an image, defaulting to the textual overlay rather than reasoning from visual evidence. This "text hijacking" phenomenon is undetected by standard VLM benchmarks which do not construct adversarial text-visual conflicts, leaving a critical blind spot in safety and reliability evaluations.

## Method
**VisualTextTrap** (arXiv: 2604.17375, April 19, 2026) is introduced as the first comprehensive benchmark for text overlay-induced hallucination, containing 6,057 human-validated samples annotated with 88 fine-grained attributes across four dimensions and a five-level hallucination intensity scale (L1–L5). The paper also proposes Visual Text Hallucination Mitigation Mixture-of-Experts (VTHM-MoE) with four specialized expert modules (temporal, action, object, spatial reasoning) and adaptive token routing to mitigate the identified failure mode.

Authors: Cui Yakun, Xingqun Qi, TianTian Geng, Yuyao Zhang, Sirui Han, Yike Guo

## Benchmarks / Datasets
- 6,057 human-validated samples with full attribute annotation
- 88 fine-grained attributes across 4 evaluation dimensions
- 5-level hallucination intensity scale (L1–L5)
- Key metrics: Hallucination Rate by Intensity Level, VQA Accuracy under Text-Visual Conflict, VTHM-MoE vs. Baseline

## Key Results

| Condition | Hallucination Rate | VQA Accuracy |
|---|---|---|
| No text overlay | Low | High |
| Conflicting text overlay | High | Degraded |
| + VTHM-MoE mitigation | Reduced | Improved |

- **All evaluated VLMs systematically hallucinate when overlaid text conflicts with visual content, defaulting to text regardless of visual evidence**
- The five-level intensity scale reveals that higher-conflict overlays trigger proportionally more severe hallucination across all models
- VTHM-MoE's adaptive token routing with four specialized experts reduces hallucination rates compared to single-model baselines
- The benchmark identifies object-level hallucination as the most severe dimension, followed by spatial and action reasoning

## Enterprise / Industry Relevance
Foxconn's visual quality inspection systems frequently encounter product images with overlaid labels, part numbers, barcode stamps, or warning text that may conflict with actual defect conditions observed in the image. FoxBrain deployed in visual QC pipelines must not be misled by text annotations on inspection images when the visual evidence tells a different story — exactly the failure mode VisualTextTrap benchmarks. Evaluating FoxBrain's VLM components against the VisualTextTrap L3–L5 intensity levels would reveal whether the system is reliable enough for production-floor deployment where mislabeled images or in-situ text annotations are common. The VTHM-MoE mitigation strategy also provides a direct upgrade path for FoxBrain's visual inspection pipeline.

---
*Back to [Main Digest](../README.md)*
