# SOTA LLM/VLM Benchmarks Digest

A curated list of Large Language Model (LLM) and Vision-Language Model (VLM) evaluation resources, focusing on State-of-the-Art (SOTA) papers, datasets, and metrics.

## 📊 Executive Summary (Q1 2026)
As of March 2026, the industry has officially moved beyond "General Knowledge" saturation. Frontier models (GPT-5.3, Gemini 3.1, Claude 4.6) now consistently exceed 90% on MMLU, shifting the focus to **Expert-level Science (GPQA)**, **Agentic Engineering (SWE-bench)**, and **Contamination-free reasoning (LiveBench)**. This digest tracks the transition from simple chat models to **Action-Oriented Agents**.

## Table of Contents
- [SOTA LLM/VLM Benchmarks Digest](#sota-llm-vlm-benchmarks-digest)
- [Individual Paper Surveys (Detailed)](./survey/)
- [LLM Benchmarks](#llm-benchmarks)
  - [Expert Reasoning](#expert-reasoning)
  - [Coding & Agents](#coding--agents)
- [VLM Benchmarks](#vlm-benchmarks)
  - [Visual Reasoning](#visual-reasoning)
  - [Document & Instruction Adherence](#document--instruction-adherence)
- [FoxBrain Roadmap](#foxbrain-roadmap)

---

## SOTA LLM/VLM Benchmarks Digest
*Quarterly survey of new benchmark-related papers and SOTA claims.*

| Paper | Modality | Benchmarks | Datasets | Metrics | Notes | Links |
| :--- | :---: | :--- | :--- | :--- | :--- | :--- |
| **Phi-4 Reasoning-Vision** | VLM | MMMU, MathVista, Blink | Interleaved Vision-Text | Acc, CoT | [Notes](./survey/2026-03-15-phi-4-reasoning.md) | [Report](https://aka.ms/phi-4-vision) |
| **DeepSeek-V3.2 (Speciale)** | LLM | AIME 2026, GPQA | 14.8T tokens | Acc, Pass@1 | [Notes](./survey/2025-05-15-deepseek-v3.md) | [arXiv](https://arxiv.org/abs/2412.19437) |
| **Humanity's Last Exam (HLE)** | LLM/VLM | HLE-Multimodal | 2,500 PhD-level Qs | Accuracy | [Notes](./survey/2025-01-20-hle-survey.md) | [Project](https://lastexam.ai/) |
| **LiveBench 2026** | LLM | LiveBench-V6 | Monthly-updated tasks | Pass@1 | [Notes](./survey/2026-01-20-livebench-v6.md) | [Project](https://livebench.ai/) |
| **olmOCR (AI2)** | VLM | olmOCR-Bench | 1.4M High-quality PDFs | Unit-test Pass% | [Notes](./survey/2025-10-05-olmocr-survey.md) | [Project](https://olmocr.allenai.org/) |

## 🌟 Notable Changes (March 2026)
* **Saturation Alert:** MMLU is now considered a "baseline" rather than a "frontier" metric as GPT-5.3 Codex hits 93%.
* **New Gold Standard:** **GPQA Diamond** and **AIME 2026** are now the primary filters for "Intelligence" (Gemini 3.1 Pro leads at 94.3% on GPQA).
* **Agentic Focus:** **SWE-bench Verified** has become the critical metric for production-ready coding agents.

---

## LLM Benchmarks

### Expert Reasoning
| Name | Task | Dataset | Metric | SOTA (Mar 2026) | Links |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **GPQA Diamond** | PhD-level Science | 448 QA | Acc | **94.3%** (Gemini 3.1 Pro) | [Paper](https://arxiv.org/abs/2311.12022) |
| **Humanity's Last Exam** | PhD-level Frontier | 2,500 Expert Qs | Accuracy | **45.8%** (Gemini 3.1 Pro) | [Project](https://lastexam.ai/) |
| **LiveBench** | Contamination-free | Monthly tasks | Pass@1 | **~68%** (GPT-5.3 Codex) | [GitHub](https://github.com/LiveBench/LiveBench) |

### Coding & Agents
| Name | Task | Dataset | Metric | SOTA (Mar 2026) | Links |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **SWE-bench Verified** | Software Engineering | 500 GitHub Issues | Resolved % | **80.8%** (Claude Opus 4.6) | [Project](https://www.swebench.com/) |
| **AIME 2026** | Frontier Mathematics | Olympiad Level | Accuracy | **91.3%** (Qwen3.5 Plus) | [GitHub](https://github.com/TIGER-AI-Lab/AIME26) |

---

## VLM Benchmarks

### Visual Reasoning
| Name | Task | Dataset | Metric | Paper | Code |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **MMMU-Pro** | Academic Reasoning | 3.4K Expert Images | Acc | [Link](https://arxiv.org/abs/2409.02813) | [Link](https://github.com/MMMU-Benchmark/MMMU) |
| **Video-MME** | Long Video (1h+) | 900 Clips | Acc | [Link](https://arxiv.org/abs/2405.21075) | [Link](https://github.com/VectorSpaceLab/Video-MME) |

### Document & Instruction Adherence
| Name | Task | Dataset | Metric | Paper | Code |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **MM-IFEngine** | VLM Instruction Following | MM-IFDataset | Constraint Sat. | [Link](https://arxiv.org/pdf/2504.07957) | [Link](https://syuan03.github.io/MM-IFEngine/) |
| **olmOCR-Bench** | End-to-end PDF OCR | 1.4K Challenging PDFs | Unit-test Pass% | [Link](https://arxiv.org/abs/2510.05678) | [Link](https://github.com/allenai/olmocr) |

---

## FoxBrain Roadmap
*Action items for the internal benchmark roadmap.*
- [ ] **Establish HLE baseline** to test frontier-level "expert" knowledge.
- [ ] **Adopt LiveBench methodology** for monthly zero-contamination testing.
- [ ] **Scale Agentic Testing:** Integrate **SWE-bench Verified** to evaluate internal coding assistants.
- [ ] **Evaluate olmOCR** for internal high-fidelity document data extraction pipelines.
