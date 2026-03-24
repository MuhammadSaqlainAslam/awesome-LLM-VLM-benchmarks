# SOTA LLM/VLM Benchmarks Digest



A curated list of Large Language Model (LLM) and Vision-Language Model (VLM) evaluation resources, focusing on State-of-the-Art (SOTA) papers, datasets, and metrics.



## 📊 Executive Summary (Q1 2026)

As of March 2026, the evaluation frontier has shifted from static knowledge to **Configurable Reasoning** and **Native Computer Use**. While frontier models like **GPT-5.4** and **Gemini 3.1 Pro** now allow users to scale "thinking effort" for PhD-level tasks, **Phi-4 Reasoning-Vision** remains the SOTA benchmark for efficient, high-reasoning multimodal performance in the 15B parameter class.



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

| **GPT-5.4 Tech Report** | LLM | GDPval, SWE-bench | 44 Occupations | Success Rate | [Notes](./survey/2026-03-05-gpt-5-4-report.md) | [Project](https://openai.com/index/introducing-gpt-5-4/) |

| **Phi-4 Reasoning-Vision** | VLM | MMMU, MathVista | Interleaved Vision | Acc, CoT | [Notes](./survey/2026-03-15-phi-4-reasoning.md) | [Report](https://aka.ms/phi-4-vision) |

| **MMMU-Pro** | VLM | MMMU-Pro Vision | Expert Images | Accuracy | [Notes](./survey/2026-03-20-mmmu-pro-survey.md) | [Paper](https://arxiv.org/abs/2409.02813) |

| **Humanity's Last Exam** | LLM/VLM | HLE-Multimodal | 2,500 PhD Qs | Accuracy | [Notes](./survey/2025-01-20-hle-survey.md) | [Project](https://lastexam.ai/) |

| **LiveBench 2026** | LLM | LiveBench-V6 | Monthly Tasks | Pass@1 | [Notes](./survey/2026-01-20-livebench-v6.md) | [Project](https://livebench.ai/) |

| **DeepSeek-V3** | LLM | MMLU-Pro, SWE-bench | 14.8T Tokens | Acc, Pass@1 | [Notes](./survey/2025-05-15-deepseek-v3.md) | [arXiv](https://arxiv.org/abs/2412.19437) |

| **olmOCR (AI2)** | VLM | olmOCR-Bench | 1.4M PDFs | Unit Pass% | [Notes](./survey/2025-10-05-olmocr-survey.md) | [Project](https://olmocr.allenai.org/) |



## 🌟 Notable Changes (March 2026)

* **Native Agentic Logic:** Both Gemini 3.1 and GPT-5.4 now support multi-level reasoning "thinking" modes (Low/Medium/High/Max).

* **Phi-4 Resilience:** Despite larger models, Phi-4 continues to set the standard for "Reasoning-Vision" in efficient model architectures.

* **ARC-AGI-2 Breakthrough:** Gemini 3.1 Pro has crossed the **77.1%** threshold, proving that models are mastering abstract logic without memorization.

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

| **Phi-4 Reasoning-Vision** | Efficient Reasoning | Interleaved Data | Acc, CoT | **SOTA (15B Class)** | [Link](https://aka.ms/phi-4-vision) |

| **ARC-AGI-2** | Visual Abduction | Non-semantic Grids | Acc | **77.1%** (Gemini 3.1 Pro) | [Link](https://arcprize.org/) |

| **MMMU-Pro** | Vision-only Expert | 3.4K Images | Acc | **82.0%** (Gemini 3.1 Pro) | [Link](https://github.com/MMMU-Benchmark/MMMU) |



### Document Intelligence

| Name | Task | Dataset | Metric | SOTA (Mar 2026) | Links |

| :--- | :--- | :--- | :--- | :--- | :--- |

| **olmOCR-Bench** | PDF-to-Markdown | 1.4K PDFs | Unit Pass% | **+14.2% over GPT-4o** | [Link](https://github.com/allenai/olmocr) |

| **MM-IFEngine** | VLM Instruction Following | MM-IFDataset | Constraint Sat. | **64.6%** (GPT-5.4) | [Link](https://syuan03.github.io/MM-IFEngine/) |



---



## FoxBrain Roadmap

*Action items for the internal benchmark roadmap.*

- [ ] **Benchmark Phi-4** against internal 15B-class baselines.

- [ ] **Benchmark Gemini 3.1 Pro** for long-context reasoning and cost-efficiency.

- [ ] **Adopt OSWorld-Verified** to evaluate native computer-use capabilities for FoxBrain agents.

- [ ] **Establish HLE baseline** to test frontier-level "expert" knowledge.

