# VisNumBench: Evaluating Number Sense of Multimodal Large Language Models (2025)

## Problem
Current multimodal benchmarks focus on symbolic math or text-based arithmetic, but ignore a foundational human perceptual skill: **number sense** — the ability to rapidly estimate, compare, and reason about quantities directly from visual data without explicit counting. No prior benchmark systematically tested whether MLLMs possess this capability.

## Method
VisNumBench constructs ~**1,900 multiple-choice question-answer pairs** derived from both synthetic and real-world visual data. The benchmark covers:
- **7 visual numerical attributes:** e.g., count, density, proportion, magnitude, rank, ratio, and sequence.
- **4 types of visual numerical estimation tasks:** direct count estimation, comparative estimation, proportional estimation, and ordinal estimation.

Evaluation is zero-shot across 17 MLLMs spanning open-source models (Qwen2.5-VL, InternVL2.5) and proprietary models (GPT-4o, Gemini 2.0 Flash).

## Benchmarks / Datasets
- **VisNumBench:** ~1,900 MCQ pairs / 7 visual attributes / 4 task types.
- **Metrics:** Multiple-choice accuracy.
- **Models tested:** 17 MLLMs including GPT-4o, Gemini 2.0 Flash, Qwen2.5-VL, InternVL2.5.

## Key Results
All 17 tested MLLMs perform **significantly below human levels** on number sense tasks. Multimodal math-specialized models and chain-of-thought (CoT) models show no significant improvement, indicating number sense is a distinct skill not addressed by math fine-tuning or reasoning augmentation.

## FoxBrain Relevance
Number sense is critical for FoxBrain's **manufacturing quality control** use cases: estimating defect density on a surface, comparing component counts across trays, or reading analog gauges. VisNumBench reveals that current MLLMs cannot reliably perform these tasks — FoxBrain must be targeted-trained on numerical visual estimation before factory-floor deployment.

---
*Back to [Main Digest](../README.md)*
