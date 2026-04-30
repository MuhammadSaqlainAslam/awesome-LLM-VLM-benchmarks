# CNSL-bench: Benchmarking Sign Language Understanding Capabilities of MLLMs on Chinese National Sign Language (2026)

## Problem
Multimodal large language models are increasingly tested on vision-language tasks, yet no comprehensive benchmark existed for Chinese National Sign Language (CNSL) — a communication system used by tens of millions of deaf and hard-of-hearing individuals in China. Existing sign language datasets lack authoritative grounding and do not cover the full range of manual articulatory forms, leaving a critical accessibility gap in MLLM evaluation.

## Method
**CNSL-bench** (arXiv: 2604.22367, April 25, 2026) is the first comprehensive benchmark for evaluating multimodal large language models on Chinese National Sign Language comprehension. Grounded in the official National Common Sign Language Dictionary, it provides aligned textual descriptions, illustrative images, and sign language videos across input modalities. It evaluates performance across manual articulatory forms including air-writing, finger-spelling, and the Chinese manual alphabet, testing 21 open-source and proprietary MLLMs.

## Benchmarks / Datasets
- Grounded in the official National Common Sign Language Dictionary
- Three input modality types: textual descriptions, illustrative images, sign language videos
- Three manual articulatory forms: air-writing, finger-spelling, Chinese manual alphabet
- 21 open-source and proprietary MLLMs evaluated
- First benchmark specifically targeting CNSL comprehension in MLLMs

## Key Results

| Evaluation Dimension | Key Finding |
|---|---|
| Overall MLLM performance | Substantially below human-level across all modalities |
| Instruction-following robustness | Varies substantially across models |
| Articulatory form difficulty | Performance varies significantly across air-writing, finger-spelling, manual alphabet |
| Open-source vs. proprietary | Proprietary models lead but all fall short of expert human performance |

- **All 21 tested MLLMs substantially underperform compared to human abilities on Chinese National Sign Language comprehension**
- Several persistent performance limitations remain beyond improvements in reasoning and instruction-following
- Robustness varies substantially across model architectures, revealing systemic challenges rather than a single model bottleneck
- The benchmark exposes a critical accessibility gap — state-of-the-art MLLMs are not yet reliable tools for sign language communication assistance

## Enterprise / Industry Relevance
Foxconn operates large manufacturing facilities in China with diverse workforces that include deaf and hard-of-hearing employees. CNSL-bench establishes the baseline for MLLM-based accessibility tools in Chinese-language sign communication — relevant if FoxBrain is extended to support inclusive factory floor communication, training materials, or safety alert systems for hearing-impaired workers. The benchmark's finding that all models fail substantially below human level signals that sign language interface features must not be deployed without dedicated fine-tuning and human validation.

---
*Back to [Main Digest](../README.md)*
