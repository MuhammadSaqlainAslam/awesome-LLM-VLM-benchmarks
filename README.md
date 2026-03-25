# SOTA LLM/VLM Benchmarks Digest

A curated dashboard of the frontier in AI evaluation. **Updated Daily: Target 8 Papers/Day.**

---

## 🚀 Today's Daily 8 (March 25, 2026)
| Paper | Modality | Benchmarks | Datasets | Metrics | Notes | Links |
| :--- | :---: | :--- | :--- | :--- | :--- | :--- |
| **AcademicEval** | LLM | AcademicEval | arXiv Papers | Judge Score | [Notes](./survey/2025-10-20-academiceval.md) | [arXiv](https://arxiv.org/abs/2510.17725) |
| **SurveyBench** | LLM | SurveyBench | 11.3k Papers | Outline Qual | [Notes](./survey/2025-10-03-surveybench.md) | [arXiv](https://arxiv.org/abs/2510.03120) |
| **LPFQA** | LLM | LPFQA | Tech Forums | Reasoning | [Notes](./survey/2026-01-08-lpfqa.md) | [arXiv](https://arxiv.org/abs/2511.06346) |
| **VideoLLM Survey** | VLM | VideoLLM Survey | Meta-Analysis | Review | [Notes](./survey/2025-05-03-videollm-survey.md) | [arXiv](https://arxiv.org/abs/2505.03829) |
| **PhysBench** | VLM | PhysBench | 10k Samples | Dynamics Acc | [Notes](./survey/2025-02-28-physbench.md) | [ICLR](https://proceedings.iclr.cc/paper/2025/hash/f38cb4cf9a5eaa92b3cfa481832719c6-Abstract-Conference.html) |
| **PLawBench** | LLM | PLawBench | Legal Practice | Rubric Acc | [Notes](./survey/2026-01-23-plawbench.md) | [arXiv](https://arxiv.org/abs/2601.16669) |
| **NC-Bench** | LLM | NC-Bench | IBM Patterns | Patterns | [Notes](./survey/2026-01-06-nc-bench.md) | [arXiv](https://arxiv.org/abs/2601.06426) |
| **TemporalBench** | VLM | TemporalBench | 2k Videos | Binary Acc | [Notes](./survey/2026-01-10-temporalbench.md) | [NeurIPS](https://neurips.cc/virtual/2024/103554) |
---

## 📑 Frontier Technical Reports
*Permanent SOTA reports from major labs.*

| Model | Lab | Benchmarks | Key SOTA Result | Notes | Official Links |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **GPT-5.4** | OpenAI | GDPval, OSWorld | 75.0% OSWorld-V | [Notes](./survey/2026-03-05-gpt-5-4-report.md) | [System Card](https://openai.com/index/gpt-5-4-thinking-system-card/) |
| **Gemini 3.1 Pro** | Google | ARC-AGI-2, GPQA | 77.1% ARC-AGI-2 | [Notes](./survey/2026-02-19-gemini-3-1-pro.md) | [Model Card](https://deepmind.google/models/model-cards/gemini-3-1-pro/) |
| **Claude 4.6 Opus** | Anthropic | SWE-bench Pro | 80.8% SWE-Verified | [Notes](./survey/2026-03-23-claude-4-6.md) | [Technical Report](https://www.anthropic.com/news/claude-opus-4-6) |
| **DeepSeek-V3.2** | DeepSeek | MMLU-Pro, IMO | RL-based Logic | [Notes](./survey/2026-03-24-deepseek-v3-2.md) | [arXiv Paper](https://arxiv.org/abs/2512.02556) |

---
### 📚 [View Full SOTA Archive (Total History)](./ARCHIVE.md)
*Historical papers like DeepSeek-V3, Step3-VL-10B, and Llama 4 Scout are preserved here.*

---

## LLM Benchmarks

### Reasoning & Knowledge
| Name | Task | Dataset | Metric | SOTA (Mar 2026) | Links |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **LiveBench 2026** | Contamination-Free | Monthly | Avg Score | **80.28** (GPT-5.4) | [Link](https://livebench.ai/) |
| **GPQA Diamond** | PhD Science | 198 QA | Acc | **95.4%** (Claude 4.6) | [Link](https://arxiv.org/abs/2311.12022) |
| **Humanity's Last Exam** | Expert Exam | 2.5K Qs | Acc | **46.2%** (Claude 4.6) | [Link](https://lastexam.ai/) |
| **ARC-AGI-2** | Visual Logic | 120 Puzzles | Acc | **77.1%** (Gemini 3.1 Pro) | [Link](https://arcprize.org/) |

### Agentic & Coding
| Name | Task | Dataset | Metric | SOTA (Mar 2026) | Links |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **SWE-bench Verified** | Engineering | 500 Issues | Resolved % | **80.8%** (Claude 4.6) | [Link](https://www.swebench.com/) |
| **OSWorld-Verified** | OS Navigation | Desktop Nav | Success % | **75.0%** (GPT-5.4) | [Link](https://os-world.github.io/) |
| **LiveCodeBench v6** | Contamination-Free Code | Monthly | Pass@1 | **91.7%** (Gemini 3 Pro) | [Link](https://livecodebench.github.io/) |

---

## VLM Benchmarks

### Multimodal Reasoning
| Name | Task | Dataset | Metric | SOTA (Mar 2026) | Links |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **MMMU-Pro** | Vision Expert | 3.4K Images | Acc | **82.0%** (Gemini 3.1 Pro) | [Link](https://github.com/MMMU-Benchmark/MMMU) |
| **MathVision** | Math Reasoning | Geometry | Acc | **75.9%** (Step3-VL-10B) | [Link](https://arxiv.org/abs/2402.14804) |
| **Phi-4 Reasoning-Vision**| Small Model Reason| Mid-Fusion | Acc | **SOTA (15B Class)** | [Link](https://aka.ms/phi-4-vision) |
| **MM-IFEngine** | Instruct Follow | MM-IFDataset | Constraint % | **64.6%** (GPT-5.4) | [Link](https://syuan03.github.io/MM-IFEngine/) |

### Video & Temporal Understanding
| Name | Task | Dataset | Metric | SOTA (Mar 2026) | Links |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **TemporalBench** | Temporal Logic | 10k QA | Binary Acc | **38.0%** (GPT-4o) | [Link](https://neurips.cc/virtual/2024/103554) |
| **PhysBench** | Physical World | 10k Video-Text | Dynamics Acc | **Low (Baseline)** | [Link](https://proceedings.iclr.cc/paper/2025/hash/f38cb4cf9a5eaa92b3cfa481832719c6-Abstract-Conference.html) |
| **VideoLLM Survey** | Meta-Analysis | Multi-Bench | Review | **Systematic Review** | [Link](https://arxiv.org/abs/2505.03829) |

---

## 🦊 FoxBrain Roadmap
- [ ] **Adopt ARC-AGI-2** for internal vision systems.
- [ ] **Benchmark DeepSeek-V3.2** as an open-weights alternative for internal reasoning.
- [ ] **Establish HLE baseline** to test frontier-level "expert" knowledge.
- [ ] **Test Step3-VL-10B** for efficient multimodal agent deployment.
- [ ] Implement **Llama 4 Scout** for high-speed documentation RAG.
