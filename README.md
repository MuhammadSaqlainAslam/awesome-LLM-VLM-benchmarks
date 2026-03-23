# SOTA LLM/VLM Benchmarks Digest

A curated list of Large Language Model (LLM) and Vision-Language Model (VLM) evaluation resources, focusing on State-of-the-Art (SOTA) papers, datasets, and metrics.

## 📊 Executive Summary (Q1 2026)
As of March 2026, general knowledge benchmarks (MMLU) are considered "solved" by frontier models. The evaluation frontier has shifted to **Expert-level Reasoning (HLE)**, **Agentic Autonomy (Terminal-Bench 2.0)**, and **Vision-centric Perception (MMMU-Pro)**. Google’s **Gemini 3.1 Pro** and Anthropic’s **Claude 4.6 Opus** currently lead the landscape in multi-step reasoning and multimodal adherence.

## Table of Contents
- [SOTA LLM/VLM Benchmarks Digest](#sota-llm-vlm-benchmarks-digest)
- [Individual Paper Surveys (Detailed)](./survey/)
- [LLM Benchmarks](#llm-benchmarks)
  - [Expert Reasoning](#expert-reasoning)
  - [Agentic & Coding](#agentic--coding)
- [VLM Benchmarks](#vlm-benchmarks)
  - [Multimodal Reasoning](#multimodal-reasoning)
  - [Document Intelligence](#document-intelligence)
- [FoxBrain Roadmap](#foxbrain-roadmap)

---

## SOTA LLM/VLM Benchmarks Digest
*Quarterly survey of new benchmark-related papers and SOTA claims.*

| Paper | Modality | Benchmarks | Datasets | Metrics | Notes | Links |
| :--- | :---: | :--- | :--- | :--- | :--- | :--- |
| **MMMU-Pro** | VLM | MMMU-Pro Vision | Expert Images | Accuracy | [Notes](./survey/2026-03-20-mmmu-pro-survey.md) | [Paper](https://arxiv.org/abs/2409.02813) |
| **Terminal-Bench 2.0** | LLM | Terminal-Bench | 89 Expert CLI Tasks | Success Rate | [Notes](./survey/2026-03-22-terminal-bench.md) | [GitHub](https://github.com/mme-bench/terminal-bench) |
| **Phi-4 Reasoning-Vision** | VLM | MMMU, MathVista | Interleaved Vision | Acc, CoT | [Notes](./survey/2026-03-15-phi-4-reasoning.md) | [Report](https://aka.ms/phi-4-vision) |
| **Humanity's Last Exam** | LLM/VLM | HLE-Multimodal | 2,500 PhD Qs | Accuracy | [Notes](./survey/2025-01-20-hle-survey.md) | [Project](https://lastexam.ai/) |
| **LiveBench 2026** | LLM | LiveBench-V6 | Monthly Tasks | Pass@1 | [Notes](./survey/2026-01-20-livebench-v6.md) | [Project](https://livebench.ai/) |
| **GPQA Diamond** | LLM | GPQA | 198 PhD-level QA | Accuracy | [Notes](./survey/2023-11-20-gpqa-diamond.md) | [Paper](https://arxiv.org/abs/2311.12022) |
| **DeepSeek-V3** | LLM | MMLU-Pro, SWE-bench | 14.8T Tokens | Acc, Pass@1 | [Notes](./survey/2025-05-15-deepseek-v3.md) | [arXiv](https://arxiv.org/abs/2412.19437) |
| **olmOCR (AI2)** | VLM | olmOCR-Bench | 1.4M PDFs | Unit Pass% | [Notes](./survey/2025-10-05-olmocr-survey.md) | [Project](https://olmocr.allenai.org/) |

## 🌟 Notable Changes (March 2026)
* **The Rise of "Thinking" Models:** Configurable reasoning (Low/Med/High/Max) is now a standard feature in Claude 4.6 and GPT-5.4.
* **ARC-AGI-2 Breakthrough:** For the first time, models like **Gemini 3.1 Pro** have crossed the 75% threshold, doubling the reasoning performance of 2024-era models.
* **Terminal-Bench 2.0:** Replaces simple code-gen tests as the benchmark for LLMs operating as autonomous terminal-based agents with real-world CLI feedback.

---

## LLM Benchmarks

### Expert Reasoning
| Name | Task | Dataset | Metric | SOTA (Mar 2026) | Links |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **GPQA Diamond** | PhD-level Science | 198 QA | Acc | **94.3%** (Gemini 3.1 Pro) | [Link](https://arxiv.org/abs/2311.12022) |
| **Humanity's Last Exam** | Expert Knowledge | 2.5K Expert Qs | Accuracy | **45.8%** (Gemini 3.1 Pro) | [Link](https://lastexam.ai/) |
| **LiveBench** | Contamination-free | Monthly Tasks | Pass@1 | **~68%** (GPT-5.4 Pro) | [Link](https://livebench.ai/) |

### Agentic & Coding
| Name | Task | Dataset | Metric | SOTA (Mar 2026) | Links |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **SWE-bench Verified** | Software Engineering | 500 GitHub Issues | Resolved % | **80.8%** (Claude 4.6 Opus) | [Link](https://www.swebench.com/) |
| **Terminal-Bench 2.0** | Autonomous Terminal | CLI Sandbox | Success Rate | **77.3%** (GPT-5.3 Codex) | [Link](https://github.com/mme-bench/terminal-bench) |

---

## VLM Benchmarks

### Multimodal Reasoning
| Name | Task | Dataset | Metric | SOTA (Mar 2026) | Links |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **MMMU-Pro** | Vision-only Expert | 3.4K Images | Acc | **82.0%** (Gemini 3.1 Pro) | [Link](https://github.com/MMMU-Benchmark/MMMU) |
| **ARC-AGI-2** | Visual Abduction | Non-semantic Grids | Acc | **77.1%** (Gemini 3.1 Pro) | [Link](https://arcprize.org/) |

### Document Intelligence
| Name | Task | Dataset | Metric | SOTA (Mar 2026) | Links |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **olmOCR-Bench** | PDF-to-Markdown | 1.4K PDFs | Unit Pass% | **+14.2% over GPT-4o** | [Link](https://github.com/allenai/olmocr) |
| **MM-IFEngine** | VLM Instruction Following | MM-IFDataset | Constraint Sat. | **64.6%** (GPT-5.4) | [Link](https://syuan03.github.io/MM-IFEngine/) |

---

## FoxBrain Roadmap
*Action items for the internal benchmark roadmap.*
- [ ] **Adopt ARC-AGI-2** to evaluate pure spatial reasoning in FoxBrain vision systems.
- [ ] **Establish HLE baseline** to test frontier-level "expert" knowledge.
- [ ] **Pilot Terminal-Bench 2.0** to test the "Agentic" autonomy of internal tools.
- [ ] **Evaluate olmOCR** for high-fidelity document ingestion pipelines.
