# VLM-RobustBench: A Comprehensive Robustness Benchmark for Vision-Language Models (2026)

## Problem
Vision-language models are routinely evaluated on clean images, leaving their robustness under real-world image corruptions poorly understood. Existing robustness studies are narrow in scope and do not distinguish between the effects of different distortion types on semantic versus spatial reasoning.

## Method
VLM-RobustBench spans 49 augmentation types — noise, blur, weather, digital, and geometric perturbations — applied at graded severities to yield 133 distinct corrupted evaluation settings. Four VLM families (Qwen, InternVL, Molmo, Gemma) are evaluated on two axes: semantic understanding (MMBench) and multimodal reasoning (MMMU-Pro), enabling fine-grained diagnosis of distortion-type-specific failure modes.

## Benchmarks / Datasets
- **VLM-RobustBench:** 133 corrupted settings across 49 augmentation types at multiple severity levels.
- **Evaluation Bases:** MMBench (visual grounding/semantic) and MMMU-Pro (multimodal reasoning).
- **Metrics:** Accuracy drop relative to clean baseline; robustness gap across distortion categories.

## Key Results
VLMs are semantically strong but spatially fragile: subtle geometric distortions caused accuracy drops of up to **34 percentage points**, far exceeding the impact of visually severe photometric corruptions like noise or blur. All four evaluated VLM families showed consistent spatial reasoning fragility.

## FoxBrain Relevance
Critical finding for any FoxBrain deployment involving camera feeds or scanned documents from factory floors. Geometric distortions (perspective shift, rotation) are common in industrial imaging — FoxBrain's VLM pipeline must be stress-tested and potentially augmented with geometric pre-processing to avoid silent accuracy failures in visual reasoning tasks.

---
*Back to [Main Digest](../README.md)*
