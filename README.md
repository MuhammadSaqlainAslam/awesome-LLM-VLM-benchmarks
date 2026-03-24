# SOTA LLM/VLM Benchmarks Digest

A curated list of Large Language Model (LLM) and Vision-Language Model (VLM) evaluation resources, focusing on State-of-the-Art (SOTA) papers, datasets, and metrics.

## 📊 Executive Summary (Q1 2026)
As of March 2026, the evaluation frontier has shifted to **Configurable Reasoning** and **Native Computer Use**. While frontier models like **GPT-5.4** and **Gemini 3.1 Pro** lead in scale, **Phi-4** and **DeepSeek-V3** remain the benchmarks for architectural efficiency and open-weights performance.

## Table of Contents
- [SOTA LLM/VLM Benchmarks Digest](#sota-llm-vlm-benchmarks-digest)
- [Individual Paper Surveys (Detailed)](./survey/)
- [LLM Benchmarks](#llm-benchmarks)
- [VLM Benchmarks](#vlm-benchmarks)
- [FoxBrain Roadmap](#foxbrain-roadmap)

---

## SOTA LLM/VLM Benchmarks Digest
*Cumulative survey of milestone papers and SOTA claims. Organized by Domain.*

| Domain | Paper | Benchmarks | Metrics | Notes |
| :--- | :--- | :--- | :--- | :--- |
| **Logic/AGI** | **ARC-AGI-2 Report** | ARC-AGI-2 | Accuracy | [Notes](./survey/2026-03-24-arc-agi-2.md) |
| **Frontier LLM** | **Gemini 3.1 Pro** | GPQA, MMMU-Pro | Acc, CoT | [Notes](./survey/2026-02-19-gemini-3-1-pro.md) |
| **Frontier LLM** | **GPT-5.4 Tech Report**| SWE-bench, OSWorld | Success Rate | [Notes](./survey/2026-03-05-gpt-5-4-report.md) |
| **Efficient VLM**| **Phi-4 Reasoning** | MMMU, MathVista | Acc, CoT | [Notes](./survey/2026-03-15-phi-4-reasoning.md) |
| **Open MoE** | **DeepSeek-V3** | MMLU-Pro, SWE-v | Acc, Pass@1 | [Notes](./survey/2025-05-15-deepseek-v3.md) |
| **Expert Eval** | **Humanity's Last Exam**| HLE-Multimodal | Accuracy | [Notes](./survey/2025-01-20-hle-survey.md) |
| **Robust Eval** | **LiveBench 2026** | LiveBench-V6 | Pass@1 | [Notes](./survey/2026-01-20-livebench-v6.md) |
| **Document AI** | **olmOCR (AI2)** | olmOCR-Bench | Unit Pass% | [Notes](./survey/2025-10-05-olmocr-survey.md) |
| **Instruction** | **MM-IFEngine** | MM-IFBenchmark | Constraint Sat.| [Notes](./survey/2025-04-10-mm-ifengine.md) |

## 🌟 Notable Changes (March 2026)
* **ARC-AGI-2 Frontier:** Gemini 3.1 Pro (77.1%) and GPT-5.4 xHigh (83.3%) are the first models to exceed average human performance on fluid reasoning.
* **Thinking-as-a-Service:** Configurable reasoning levels (Low to Max) allow models to "spend" more time on a problem to increase accuracy.
* **Native Computer Use:** GPT-5.4 now features a native API for operating desktop environments via screenshots, tested on **OSWorld-Verified**.

---

## LLM Benchmarks

### Expert Reasoning
| Name | Task | Dataset | Metric | SOTA (Mar 2026) |
| :--- | :--- | :--- | :--- | :--- |
| **GPQA Diamond** | PhD-level Science | 198 QA | Acc | **94.3%** (Gemini 3.1 Pro) |
| **Humanity's Last Exam** | Expert Knowledge | 2.5K Expert Qs | Accuracy | **45.8%** (Gemini 3.1 Pro) |
| **LiveBench** | Contamination-free | Monthly Tasks | Pass@1 | **~68%** (GPT-5.4) |

### Agentic & Coding
| Name | Task | Dataset | Metric | SOTA (Mar 2026) |
| :--- | :--- | :--- | :--- | :--- |
| **SWE-bench Verified** | Software Engineering | 500 GitHub Issues | Resolved % | **80.8%** (Claude 4.6 Opus) |
| **OSWorld-Verified** | OS/Computer Use | Desktop Navigation | Success Rate | **75.0%** (GPT-5.4) |

---

## VLM Benchmarks

### Multimodal Reasoning
| Name | Task | Dataset | Metric | SOTA (Mar 2026) |
| :--- | :--- | :--- | :--- | :--- |
| **ARC-AGI-2** | Visual Abduction | Non-semantic Grids | Acc | **84.6%** (Gemini 3 Deep Think) |
| **MMMU-Pro** | Vision-only Expert | 3.4K Images | Acc | **82.0%** (Gemini 3.1 Pro) |
| **Phi-4 Reasoning-Vision** | Efficient Reasoning | 15B Class | Acc | **SOTA (Efficiency)** |

### Document Intelligence
| Name | Task | Dataset | Metric | SOTA (Mar 2026) |
| :--- | :--- | :--- | :--- | :--- |
| **olmOCR-Bench** | PDF-to-Markdown | 1.4K PDFs | Unit Pass% | **+14.2% over GPT-4o** |
| **MM-IFEngine** | VLM Instruction Following | MM-IFDataset | Constraint Sat. | **64.6%** (GPT-5.4) |

---

## FoxBrain Roadmap
- [ ] **Adopt ARC-AGI-2** to evaluate pure spatial reasoning in FoxBrain vision systems.
- [ ] **Benchmark DeepSeek-V3** as an open-weights alternative for internal reasoning tasks.
- [ ] **Evaluate olmOCR** for high-fidelity document ingestion pipelines.
