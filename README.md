# SOTA LLM/VLM Benchmarks Digest

A curated list of Large Language Model (LLM) and Vision-Language Model (VLM) evaluation resources, focusing on State-of-the-Art (SOTA) papers, datasets, and metrics.

## 📊 Executive Summary (Q1 2026)
This quarter's survey tracks the transition from general knowledge (MMLU) toward **PhD-level reasoning**, **contamination-free evaluation**, and **strict instruction following**. The emergence of "Google-proof" benchmarks like HLE, dynamic suites like LiveBench, and automated evaluators like MM-IFEngine represent the new frontier for model validation.

## Table of Contents
- [SOTA LLM/VLM Benchmarks Digest](#sota-llm-vlm-benchmarks-digest)
- [Individual Paper Surveys (Detailed)](./survey/)
- [LLM Benchmarks](#llm-benchmarks)
  - [General Reasoning](#general-reasoning)
- [VLM Benchmarks](#vlm-benchmarks)
  - [Image Understanding](#image-understanding)
  - [Instruction Following](#instruction-following)
- [FoxBrain Roadmap](#foxbrain-roadmap)

---

## SOTA LLM/VLM Benchmarks Digest
*Quarterly survey of new benchmark-related papers and SOTA claims.*

| Paper | Modality | Benchmarks | Datasets | Metrics | Notes | Links |
| :--- | :---: | :--- | :--- | :--- | :--- | :--- |
| **Phi-4 Reasoning-Vision** | VLM | MMMU, MathVista, Blink | Interleaved Vision-Text | Acc, CoT | [Notes](./survey/2026-03-15-phi-4-reasoning.md) | [Report](https://aka.ms/phi-4-vision) |
| **MM-IFEngine** | VLM | MM-IFBenchmark | MM-IFDataset | Constraint Sat. | [Notes](./survey/2025-04-10-mm-ifengine.md) | [arXiv](https://arxiv.org/pdf/2504.07957) |
| **Humanity's Last Exam** | LLM/VLM | HLE-Multimodal | 2,500 Expert Qs | Accuracy | [Notes](./survey/2025-01-20-hle-survey.md) | [Project](https://lastexam.ai/) |
| **LiveBench 2026** | LLM | LiveBench-V6 | Monthly-updated tasks | Pass@1 | [Notes](./survey/2026-01-20-livebench-v6.md) | [Project](https://livebench.ai/) |
| **DeepSeek-V3 Tech Report** | LLM | MMLU-Redux, GPQA | 14.8T Tokens | Acc, Pass@1 | [Notes](./survey/2025-05-15-deepseek-v3.md) | [arXiv](https://arxiv.org/abs/2412.19437) |

## 🌟 Notable New/Changed Benchmarks
* **HLE (Humanity's Last Exam):** Emerging as the primary replacement for MMLU for frontier models.
* **LiveBench:** Introduced to solve the "memorization" problem by releasing new tasks every month to ensure zero contamination.
* **MM-IFBenchmark:** First systematic effort to automate multi-modal constraint evaluation.

---

## LLM Benchmarks

### General Reasoning
| Name | Task | Dataset | Metric | Paper | Code |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **GPQA Diamond** | PhD-level Science | 448 QA | Acc | [Link](https://arxiv.org/abs/2311.12022) | [Link](https://github.com/openai/gpqa) |
| **LiveBench** | Contamination-free Reasoning | Monthly-updated tasks | Pass@1 | [Link](https://arxiv.org/abs/2406.19314) | [Link](https://github.com/LiveBench/LiveBench) |
| **Humanity's Last Exam** | Expert Knowledge | 2.5K Expert Qs | Accuracy | [Link](https://arxiv.org/abs/2501.14249) | [Link](https://github.com/centerforaisafety/hle) |
| **MMLU-Pro** | Multi-discipline | 12K MCQs | Acc | [Link](https://arxiv.org/abs/2406.01574) | [Link](https://github.com/TIGER-AI-Lab/MMLU-Pro) |

---

## VLM Benchmarks

### Image Understanding
| Name | Task | Dataset | Metric | Paper | Code |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **MMMU-Pro** | Academic Reasoning | 3.4K Expert Images | Acc | [Link](https://arxiv.org/abs/2409.02813) | [Link](https://github.com/MMMU-Benchmark/MMMU) |
| **MathVista** | Visual Math | 6.5K Images | Acc | [Link](https://arxiv.org/abs/2310.02255) | [Link](https://github.com/lucas0/MathVista) |

### Instruction Following
| Name | Task | Dataset | Metric | Paper | Code |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **MM-IFEngine** | VLM Instruction Following | MM-IFDataset | Constraint Sat. | [Link](https://arxiv.org/pdf/2504.07957) | [Link](https://syuan03.github.io/MM-IFEngine/) |

---

## FoxBrain Roadmap
*Action items for the internal benchmark roadmap.*
- [ ] **Establish HLE baseline** to test frontier-level "expert" knowledge.
- [ ] **Adopt LiveBench methodology** for zero-contamination testing of internal models.
- [ ] **Benchmark Phi-4** against internal 15B-class baselines.
- [ ] **Integrate MM-IFEngine** to measure multimodal instruction adherence.
