# SOTA LLM/VLM Benchmarks Digest

A curated list of Large Language Model (LLM) and Vision-Language Model (VLM) evaluation resources, focusing on State-of-the-Art (SOTA) papers, datasets, and metrics.

## 📊 Executive Summary (Q1 2026)
As of March 2026, the evaluation frontier has shifted from static knowledge to **Configurable Reasoning** and **Native Computer Use**. Frontier models like **GPT-5.4** and **Gemini 3.1 Pro** now allow users to scale "thinking effort," leading to breakthroughs in PhD-level science (GPQA) and abstract logic (ARC-AGI-2). 

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
| **Gemini 3.1 Pro Report** | LLM/VLM | ARC-AGI-2, GPQA | Expert Logic/Science | Acc, Verified Pass | [Notes](./survey/2026-02-19-gemini-3-1-pro.md) | [Report](https://deepmind.google/models/gemini/pro/) |
| **GPT-5.4 Tech Report** | LLM | GDPval, SWE-bench | 44 Occupations | Success Rate | [Notes](./survey/2026-03-05-gpt-5-4-report.md) | [Project](https://openai.com/index/gpt-5-4) |
| **Phi-4 Reasoning-Vision** | VLM | MMMU, MathVista | Interleaved Vision | Acc, CoT | [Notes](./survey/2026-03-15-phi-4-reasoning.md) | [Report](https://aka.ms/phi-4-vision) |
| **Humanity's Last Exam** | LLM/VLM | HLE-Multimodal | 2,500 PhD Qs | Accuracy | [Notes](./survey/2025-01-20-hle-survey.md) | [Project](https://lastexam.ai/) |
| **MM-IFEngine** | VLM | MM-IFBenchmark | MM-IFDataset | Constraint Sat. | [Notes](./survey/2025-04-10-mm-ifengine.md) | [arXiv](https://arxiv.org/pdf/2504.07957) |

## 🌟 Notable Changes (March 2026)
* **Native Agentic Logic:** Both Gemini 3.1 and GPT-5.4 now support multi-level reasoning "thinking" modes (Low/Medium/High/Max).
* **ARC-AGI-2 Milestone:** Gemini 3.1 Pro has crossed the **77.1%** threshold, proving that models are beginning to master abstract logic patterns without memorization.
* **Computer Use API:** GPT-5.4 introduces native computer operation, allowing agents to navigate file systems and UIs directly via screenshots.

---

## LLM Benchmarks

### Expert Reasoning
| Name | Task | Dataset | Metric | SOTA (Mar 2026) | Links |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **GPQA Diamond** | PhD-level Science | 198 QA | Acc | **94.3%** (Gemini 3.1 Pro) | [Link](https://arxiv.org/abs/2311.12022) |
| **Humanity's Last Exam** | Expert Knowledge | 2.5K Expert Qs | Accuracy | **45.8%** (Gemini 3.1 Pro) | [Link](https://lastexam.ai/) |
| **LiveBench** | Contamination-free | Monthly Tasks | Pass@1 | **~68%** (GPT-5.4) | [Link](https://livebench.ai/) |

### Agentic & Coding
| Name | Task | Dataset | Metric | SOTA (Mar 2026) | Links |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **SWE-bench Verified** | Software Engineering | 500 GitHub Issues | Resolved % | **80.8%** (Claude 4.6 Opus) | [Link](https://www.swebench.com/) |
| **OSWorld-Verified** | OS/Computer Use | Desktop Navigation | Success Rate | **75.0%** (GPT-5.4) | [Link](https://os-world.github.io/) |

---

## VLM Benchmarks

### Multimodal Reasoning
| Name | Task | Dataset | Metric | SOTA (Mar 2026) | Links |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **ARC-AGI-2** | Visual Abduction | Non-semantic Grids | Acc | **77.1%** (Gemini 3.1 Pro) | [Link](https://arcprize.org/) |
| **MMMU-Pro** | Vision-only Expert | 3.4K Images | Acc | **82.0%** (Gemini 3.1 Pro) | [Link](https://github.com/MMMU-Benchmark/MMMU) |

### Document Intelligence
| Name | Task | Dataset | Metric | SOTA (Mar 2026) | Links |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **olmOCR-Bench** | PDF-to-Markdown | 1.4K PDFs | Unit Pass% | **+14.2% over GPT-4o** | [Link](https://github.com/allenai/olmocr) |

---

## FoxBrain Roadmap
*Action items for the internal benchmark roadmap.*
- [ ] **Benchmark Gemini 3.1 Pro** as the new cost-efficiency baseline for long-context reasoning.
- [ ] **Adopt OSWorld-Verified** to evaluate native computer-use capabilities for FoxBrain agents.
- [ ] **Establish HLE baseline** to test PhD-level domain expertise.
