# Awesome SOTA LLM/VLM Benchmarks

A curated list of Large Language Model (LLM) and Vision-Language Model (VLM) evaluation resources, focusing on State-of-the-Art (SOTA) papers, datasets, and metrics.

## Table of Contents
- [SOTA Digests](#sota-digests)
- [Large Language Model (LLM) Benchmarks](#llm-benchmarks)
  - [General Reasoning](#general-reasoning)
  - [Coding & Math](#coding--math)
  - [Agentic & Planning](#agentic--planning)
- [Vision-Language Model (VLM) Benchmarks](#vlm-benchmarks)
  - [Image Understanding](#image-understanding)
  - [Instruction Following](#instruction-following)
  - [Video Understanding](#video-understanding)
- [FoxBrain Roadmap](#foxbrain-roadmap)

---

## SOTA Digests
*Quarterly survey of new benchmark-related papers and SOTA claims.*

| Paper | Modality | Key Benchmarks | Dataset | Metric | SOTA Claim | Links |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Phi-4 Reasoning-Vision** | VLM | MMMU, MathVista, Blink | Interleaved Vision-Text | Accuracy, CoT | SOTA in 15B parameter class | [Report](https://www.microsoft.com/en-us/research/wp-content/uploads/2026/03/Phi-4-reasoning-vision-15B-Tech-Report-1.pdf) [Blog](https://aka.ms/phi-4-vision) |
| **DeepSeek-V3 Tech Report** | LLM | MMLU-Redux, GPQA | 14.8T Tokens | Acc, Pass@1 | SOTA performance in open-weights | [arXiv (2025)](https://arxiv.org/abs/2412.19437) [Code](https://github.com/deepseek-ai/DeepSeek-V3) |
| **Humanity's Last Exam (HLE)** | LLM/VLM | HLE-Multimodal | 2,500 Expert Qs | Accuracy | New PhD-level "Google-proof" frontier | [arXiv (2025)](https://arxiv.org/abs/2501.14249) [Project](https://lastexam.ai/) |
| **MM-IFEngine** | VLM | MM-IFBenchmark | MM-IFDataset | Constraint Satisfaction | Systematic eval for MLLM constraints | [arXiv (2025)](https://arxiv.org/pdf/2504.07957) [Project](https://syuan03.github.io/MM-IFEngine/) |
| **LiveBench 2026 Refresh** | LLM | LiveBench-V6 | Monthly-updated tasks | Pass@1 | Contamination-free reasoning SOTA | [Project](https://livebench.ai/) [Code](https://github.com/LiveBench/LiveBench) |

---

## LLM Benchmarks

### General Reasoning
| Name | Task | Dataset | Metric | Paper | Code |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **GPQA Diamond** | PhD-level Science | 448 QA | Acc | [Link](https://arxiv.org/abs/2311.12022) | [Link](https://github.com/openai/gpqa) |
| **MMLU-Pro** | Multi-discipline | 12K MCQs | Acc | [Link](https://arxiv.org/abs/2406.01574) | [Link](https://github.com/TIGER-AI-Lab/MMLU-Pro) |
| **Humanity's Last Exam** | Expert Knowledge | 2.5K Expert Qs | Accuracy | [Link](https://arxiv.org/abs/2501.14249) | [Link](https://github.com/centerforaisafety/hle) |

### Coding & Math
| Name | Task | Dataset | Metric | Paper | Code |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **LiveCodeBench** | Contamination-free Code | LeetCode/AtCoder | Pass@1 | [Link](https://arxiv.org/abs/2403.07974) | [Link](https://github.com/LiveCodeBench/LiveCodeBench) |
| **AIME 2025** | Frontier Mathematics | Olympiad Level | Accuracy | [Link](https://livebench.ai/) | [Link](https://github.com/LiveBench/LiveBench) |

---

## VLM Benchmarks

### Image Understanding
| Name | Task | Dataset | Metric | Paper | Code |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **MMMU-Pro** | Academic Reasoning | 3.4K Expert Images | Acc | [Link](https://arxiv.org/abs/2409.02813) | [Link](https://github.com/MMMU-Benchmark/MMMU) |
| **MathVista** | Visual Math | 6.5K Images | Acc | [Link](https://arxiv.org/abs/2310.02255) | [Link](https://github.com/lucas0/MathVista) |
| **Phi-4 (Reasoning-Vision)** | Multimodal Reasoning | Synthetic + Curated | Acc, CoT | [Link](https://www.microsoft.com/en-us/research/wp-content/uploads/2026/03/Phi-4-reasoning-vision-15B-Tech-Report-1.pdf) | [Blog](https://aka.ms/phi-4-vision) |

### Instruction Following
| Name | Task | Dataset | Metric | Paper | Code |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **MM-IFEngine** | VLM Instruction Following | MM-IFDataset | Constraint Satisfaction | [Link](https://arxiv.org/pdf/2504.07957) | [Link](https://syuan03.github.io/MM-IFEngine/) |

### Video Understanding
| Name | Task | Dataset | Metric | Paper | Code |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Video-MME** | Long Video (1h+) | 900 Clips | Acc | [Link](https://arxiv.org/abs/2405.21075) | [Link](https://github.com/VectorSpaceLab/Video-MME) |

---

## FoxBrain Roadmap
*Action items for the internal benchmark roadmap.*
- [ ] **Establish HLE baseline** to test frontier-level "expert" knowledge.
- [ ] **Benchmark Phi-4** against internal 15B-class baselines.
- [ ] **Integrate MM-IFEngine** to measure multimodal instruction adherence.
- [ ] **Adopt LiveBench methodology** for zero-contamination testing.
- [ ] **Integrate Video-MME** for multimodal testing.
