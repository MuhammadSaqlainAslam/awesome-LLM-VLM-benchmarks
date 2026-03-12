# Awesome SOTA LLM/VLM Benchmarks

A curated list of Large Language Model (LLM) and Vision-Language Model (VLM) evaluation resources, focusing on State-of-the-Art (SOTA) papers, datasets, and metrics.

## Table of Contents
- [SOTA Digests](#sota-digests)
- [Large Language Model (LLM) Benchmarks](#llm-benchmarks)
  - [General Reasoning](#general-reasoning)
  - [Coding & Math](#coding--math)
- [Vision-Language Model (VLM) Benchmarks](#vlm-benchmarks)
  - [Image Understanding](#image-understanding)
  - [Video Understanding](#video-understanding)
- [FoxBrain Roadmap](#foxbrain-roadmap)

---

## SOTA Digests
*Quarterly survey of new benchmark-related papers and SOTA claims.*

| Paper | Modality | Key Benchmarks | Dataset | Metric | SOTA Claim | Links |
| :--- | :---: | :--- | :--- | :--- | :--- | :--- |
| **Example Paper Title** | VLM | Video-MME, MMMU | 900+ Videos | Acc, F1 | #1 in Long Video | [arXiv](...) [Code](...) |

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

### Video Understanding
| Name | Task | Dataset | Metric | Paper | Code |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Video-MME** | Long Video | 900 Clips | Acc | [Link](https://arxiv.org/abs/2405.21075) | [Link](https://github.com/VectorSpaceLab/Video-MME) |

---

## FoxBrain Roadmap
*Action items for the internal benchmark roadmap.*
- [ ] Integrate **Video-MME** for multimodal testing.
- [ ] Establish **Human-in-the-loop** scoring for open-ended VLM tasks.
