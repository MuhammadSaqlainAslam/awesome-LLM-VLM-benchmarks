# SOTA LLM/VLM Benchmarks Digest

A curated dashboard of the frontier in AI evaluation. **Updated Daily: Target 8 Papers/Day.**

## 📊 Executive Summary (Q1 2026)
As of March 24, 2026, the evaluation frontier has shifted to **Configurable Reasoning** and **Native Computer Use**. While flagship models like **GPT-5.4** and **Claude 4.6 Opus** lead in agentic planning, **Step3-VL-10B** has redefined efficiency by rivaling 100B+ models in multimodal reasoning.

---

## 🚀 Today's Daily 8 (March 24, 2026)
| Paper | Modality | Benchmarks | Datasets | Metrics | Notes | Links |
| :--- | :---: | :--- | :--- | :--- | :--- | :--- |
| **ARC-AGI-2 Report** | LLM/VLM | ARC-AGI-2 | Visual Abduction | Accuracy | [Notes](./survey/2026-03-24-arc-agi-2.md) | [Link](https://arcprize.org/leaderboard) |
| **Claude 4.6 Opus** | LLM | SWE-bench Pro, HLE | Agent Teams | Resolved % | [Notes](./survey/2026-03-23-claude-4-6.md) | [Link](https://www.anthropic.com/news/claude-opus-4-6) |
| **GPQA Diamond** | LLM | PhD-level Science | 198 Expert QA | Accuracy | [Notes](./survey/2023-11-20-gpqa-diamond.md) | [Link](https://arxiv.org/abs/2311.12022) |
| **MM-IFEngine** | VLM | MM-IFBenchmark | MM-IFDataset | Constraint Sat. | [Notes](./survey/2025-04-10-mm-ifengine.md) | [Link](https://syuan03.github.io/MM-IFEngine/) |
| **Step3-VL-10B** | VLM | MMMU, MathVision | 1.2T MM Tokens | Accuracy | [Notes](./survey/2026-01-14-step3-vl.md) | [arXiv](https://arxiv.org/abs/2601.09668) |
| **Llama 4 Scout** | LLM | Long-Context Eval | 10M Window | Retrieval Acc | [Notes](./survey/2026-02-20-llama-4-scout.md) | [Link](https://llama.meta.com/) |
| **GPT-5.4 mini/nano** | LLM | OSWorld-Verified | Fast Reasoning | Success Rate | [Notes](./survey/2026-03-22-gpt-5-4-mini.md) | [Link](https://openai.com/index/introducing-gpt-5-4-mini-and-nano/) |
| **DeepSeek-V3.2** | LLM | MMLU-Pro, SWE-v | FP8 Training | Acc, Pass@1 | [Notes](./survey/2026-03-24-deepseek-v3-2.md) | [Link](https://www.deepseek.com/) |
---
### 📚 [View Full SOTA Archive (All Previous Papers)](./ARCHIVE.md)

---

## 🌟 Notable Changes (March 2026)
* **ARC-AGI-2 Breakthrough:** Claude 4.6 Opus sets a new frontier for reasoning models with **68.8%** on ARC-AGI-2.
* **10B Efficiency:** Step3-VL-10B achieves **80.1% MMMU**, rivaling proprietary flagships 20x its size.
* **10M Context Window:** Llama 4 Scout (2600 t/s) introduces the first stable 10-million token context window.

---

## LLM Benchmarks

### Expert Reasoning
| Name | Task | Dataset | Metric | SOTA (Mar 2026) | Links |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **GPQA Diamond** | PhD-level Science | 198 QA | Acc | **95.4%** (Claude 4.6 Opus) | [Link](https://arxiv.org/abs/2311.12022) |
| **Humanity's Last Exam** | Expert Knowledge | 2.5K Expert Qs | Accuracy | **45.8%** (Gemini 3.1 Pro) | [Link](https://lastexam.ai/) |
| **LiveBench** | Contamination-free | Monthly Tasks | Pass@1 | **80.3%** (GPT-5.4 Thinking) | [Link](https://livebench.ai/) |
| **ARC-AGI-2** | Abstract Logic | 120 Visual Puzzles | Accuracy | **68.8%** (Claude 4.6 Opus) | [Link](https://arcprize.org/leaderboard) |

### Agentic & Coding
| Name | Task | Dataset | Metric | SOTA (Mar 2026) | Links |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **SWE-bench Verified** | Software Engineering | 500 GitHub Issues | Resolved % | **80.8%** (Claude 4.6 Opus) | [Link](https://www.swebench.com/) |
| **SWE-bench Pro** | Complex Software Fixes| 1,865 Multi-file | Resolved % | **57.7%** (GPT-5.4) | [Link](https://www.morphllm.com/swe-bench-pro) |
| **OSWorld-Verified** | OS/Computer Use | Desktop Navigation | Success Rate | **75.0%** (GPT-5.4) | [Link](https://os-world.github.io/) |

---

## VLM Benchmarks

### Multimodal Reasoning
| Name | Task | Dataset | Metric | SOTA (Mar 2026) | Links |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **MMMU-Pro** | Vision-only Expert | 3.4K Images | Acc | **82.0%** (Gemini 3.1 Pro) | [Link](https://github.com/MMMU-Benchmark/MMMU) |
| **MathVision** | Mathematical Reasoning| Complex Geometry | Accuracy | **75.9%** (Step3-VL-10B) | [Link](https://arxiv.org/abs/2402.14804) |
| **Phi-4 Reasoning-Vision** | Efficient Reasoning | Interleaved Data | Acc, CoT | **SOTA (15B Class)** | [Link](https://aka.ms/phi-4-vision) |
| **MM-IFEngine** | VLM Instruction Following | MM-IFDataset | Constraint Sat. | **64.6%** (GPT-5.4) | [Link](https://syuan03.github.io/MM-IFEngine/) |

---

## FoxBrain Roadmap
- [ ] **Adopt ARC-AGI-2** for internal vision systems (Current SOTA: Claude 4.6 Opus).
- [ ] **Benchmark DeepSeek-V3.2** for high-efficiency reasoning in DevOps.
- [ ] **Test Step3-VL-10B** for local multimodal agent deployment on edge devices.
