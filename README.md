# Awesome SOTA LLM/VLM Benchmarks

A curated list of Large Language Model (LLM) and Vision-Language Model (VLM) evaluation resources, focusing on State-of-the-Art (SOTA) papers, datasets, and metrics.

## Table of Contents
- [SOTA Digests](#sota-digests)
- [Large Language Model (LLM) Benchmarks](#llm-benchmarks)
  - [General Reasoning](#general-reasoning)
  - [Coding & Math](#coding--math)
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
| **Phi-4 Reasoning-Vision** | VLM | MMMU, MathVista, Blink | Interleaved Vision-Text | Accuracy, CoT | SOTA in 15B parameter class | [Report](https://www.microsoft.com/en-us/research/wp-content/uploads/2026/03/Phi-4-reasoning-vision-15B-Tech-Report-1.pdf) [Blog](https://www.microsoft.com/en-us/research/blog/phi-4-reasoning-vision-and-the-lessons-of-training-a-multimodal-reasoning-model/) |
| **MM-IFEngine** | VLM | MM-IFBenchmark | MM-IFDataset | Constraint Satisfaction | Systematic eval for MLLM constraints | [arXiv](https://arxiv.org/pdf/2504.07957) [Project](https://syuan03.github.io/MM-IFEngine/) |
| **Qwen3 Tech Report** | LLM/VLM | MMLU, GPQA Diamond | 36T tokens | Acc, Pass@1 | SOTA open-weights (0.6B-235B) | [arXiv](https://arxiv.org/abs/2505.09388) |

---

## LLM Benchmarks

### General Reasoning
| Name | Task | Dataset | Metric | Paper | Code |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **GPQA** | Graduate Science | 448 QA | Acc | [Link](https://arxiv.org/abs/2311.12022) | [Link](https://github.com/openai/gpqa) |
| **MMLU-Pro** | Multi-discipline | 12K MCQs | Acc | [Link](https://arxiv.org/abs/2406.01574) | [Link](https://github.com/TIGER-AI-Lab/MMLU-Pro) |

---

## VLM Benchmarks

### Image Understanding
| Name | Task | Dataset | Metric | Paper | Code |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **MMMU** | Expert Reasoning | 11.5K Images | Acc | [Link](https://arxiv.org/abs/2311.16502) | [Link](https://github.com/MMMU-Benchmark/MMMU) |
| **MathVista** | Visual Math | 6.5K Images | Acc | [Link](https://arxiv.org/abs/2310.02255) | [Link](https://github.com/lucas0/MathVista) |
| **Phi-4 (Reasoning-Vision)** | Multimodal Reasoning | Synthetic + Curated | Acc, CoT | [Link](https://www.microsoft.com/en-us/research/wp-content/uploads/2026/03/Phi-4-reasoning-vision-15B-Tech-Report-1.pdf) | [Blog](https://www.microsoft.com/en-us/research/blog/phi-4-reasoning-vision-and-the-lessons-of-training-a-multimodal-reasoning-model/) |

### Instruction Following
| Name | Task | Dataset | Metric | Paper | Code |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **MM-IFEngine** | VLM Instruction Following | MM-IFDataset | Instruction Satisfaction | [Link](https://arxiv.org/pdf/2504.07957) | [Link](https://syuan03.github.io/MM-IFEngine/) |

### Video Understanding
| Name | Task | Dataset | Metric | Paper | Code |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Video-MME** | Long Video | 900 Clips | Acc | [Link](https://arxiv.org/abs/2405.21075) | [Link](https://github.com/VectorSpaceLab/Video-MME) |

---

## FoxBrain Roadmap
*Action items for the internal benchmark roadmap.*
- [ ] **Benchmark Phi-4** against internal 15B-class baselines.
- [ ] Integrate **MM-IFEngine** to measure multimodal instruction adherence.
- [ ] Integrate **Video-MME** for multimodal testing.
- [ ] Establish **Human-in-the-loop**
