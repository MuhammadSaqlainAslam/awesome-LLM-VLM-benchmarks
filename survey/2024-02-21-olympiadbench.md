# OlympiadBench: A Bilingual Multimodal Scientific Olympiad Benchmark (2024)

## Problem
Existing LLM evaluation benchmarks were predominantly monolingual (English-only), text-only, and insufficiently challenging for frontier models. No benchmark combined **bilingual (Chinese + English)** Olympiad-level difficulty with **multimodal problems** across both mathematics and physics, with expert-annotated step-by-step solutions — leaving a critical gap in evaluating the intersection of scientific reasoning, visual understanding, and cross-lingual capability.

## Method
Problems were collected from **national and international Olympiad competitions** and the **Chinese college entrance exam (Gaokao)**, then manually annotated by human experts with full step-by-step solutions. Evaluation protocols distinguish three answer types: numeric, symbolic, and proof-based. Notably, **57% of all problems include diagrams** (figures, geometric constructions, physics schematics), making this a true multimodal benchmark. The benchmark covers both Mathematics and Physics, in both Chinese and English. Published at **ACL 2024 (main conference, Long Papers)**, from Tsinghua University and collaborating institutions.

## Benchmarks / Datasets
- **8,476 total problems** (Math: 6,524 / Physics: 2,428)
- **Bilingual:** English (2,288 problems) and Chinese (6,664 problems)
- **Multimodal:** 5,129 problems with images (57%)
- **Answer formats:** Open-ended (7,254 / 81%) and theorem-proving (1,698 / 19%)
- **Sources:** International and Chinese national Olympiad competitions, Gaokao
- **Domains:** Mathematics (algebra, geometry, number theory, combinatorics) and Physics (mechanics, electromagnetism, optics, thermodynamics)

## Key Results

| Model | Math Avg | Physics Avg | Overall |
|---|---|---|---|
| **GPT-4V** | **20.35%** | **11.28%** | **17.23%** |
| DeepSeekMath-7B-RL (text) | 20.25% | 9.38% | 18.73% |
| Qwen-VL-Max | 12.76% | 4.44% | 10.31% |
| Gemini Pro Vision | 5.35% | 2.89% | 4.38% |
| LLaVA-NeXT-34B | 4.36% | 1.80% | 3.60% |
| Yi-VL-34B | 4.67% | 1.55% | 3.37% |

Even GPT-4V achieves only **17.23% overall**, with Physics proving harder than Mathematics across all models. Performance on diagram-based problems is substantially lower than on text-only problems, confirming that visual-scientific reasoning remains a major frontier.

## FoxBrain Relevance
OlympiadBench's bilingual Chinese/English design is directly aligned with FoxBrain's deployment environment. The 57% image-containing problems map precisely to Foxconn's engineering workflows, where workers routinely interpret physics schematics, circuit diagrams, and geometric manufacturing drawings alongside Chinese-language specifications. Physics performance (particularly mechanics and electromagnetism) is directly applicable to FoxBrain's industrial automation and equipment maintenance use cases. The theorem-proving subset (19%) provides a ceiling test for FoxBrain's formal technical reasoning.

---
*Back to [Main Digest](../README.md)*
