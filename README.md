# SOTA LLM/VLM Benchmarks Digest

A curated dashboard of the frontier in AI evaluation. **Updated Daily: Target 8 Papers/Day.**

---

## 🚀 Today's Daily 8 (March 27, 2026)

| Paper | Modality | Benchmarks | Datasets | Metrics | Notes | Links |
| :--- | :---: | :--- | :--- | :--- | :--- | :--- |
| **SimpleQA** | LLM | SimpleQA | 4,326 Factual QA | F1 / Correct % | [Notes](./survey/2024-11-01-simpleqa.md) | [arXiv](https://arxiv.org/abs/2411.04368) |
| **PentestEval** | LLM | PentestEval | 346 Pentest Tasks | Stage / E2E % | [Notes](./survey/2025-12-15-pentesteval.md) | [arXiv](https://arxiv.org/abs/2512.14233) |
| **BenchHub** | Meta | BenchHub | 839K Qs / 54 Bench | Customizable | [Notes](./survey/2025-06-01-benchhub.md) | [arXiv](https://arxiv.org/abs/2506.00482) |
| **XLRS-Bench** | VLM | XLRS-Bench | 45,942 RS Annotations | VQA / Grounding Acc | [Notes](./survey/2025-03-30-xlrs-bench.md) | [arXiv](https://arxiv.org/abs/2503.23771) |
| **VLR-Bench** | VLM | VLR-Bench | 300 RAG VQA | RAG Accuracy | [Notes](./survey/2024-12-10-vlr-bench.md) | [arXiv](https://arxiv.org/abs/2412.10151) |
| **MotionBench** | VLM | MotionBench | 5,000 Videos | Motion QA Acc | [Notes](./survey/2025-01-06-motionbench.md) | [arXiv](https://arxiv.org/abs/2501.02955) |
| **VL-RewardBench** | VLM | VL-RewardBench | 1,250 Pref Examples | Judgment Acc | [Notes](./survey/2024-11-26-vl-rewardbench.md) | [arXiv](https://arxiv.org/abs/2411.17451) |
| **ToolBench** | LLM | ToolBench | 16k Real APIs | Pass Rate | [Notes](./survey/2025-01-15-toolbench.md) | [arXiv](https://arxiv.org/abs/2307.16789) |

---

## 📑 Frontier Technical Reports
| Model | Lab | Benchmarks | Key SOTA Result | Notes | Official Links |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **GPT-5.4 Report** | OpenAI | GDPval, OSWorld | 75.0% OSWorld-V | [Notes](./survey/2026-03-05-gpt-5-4-report.md) | [OpenAI Report](https://openai.com/index/introducing-gpt-5-4/) |
| **Phi-4 Reasoning** | Microsoft | MMMU, MathVista | 15B Tech Report | [Notes](./survey/2026-03-15-phi-4-reasoning.md) | [Tech Report (PDF)](https://www.microsoft.com/en-us/research/wp-content/uploads/2026/03/Phi-4-reasoning-vision-15B-Tech-Report.pdf) |
| **DeepSeek-V3.2** | DeepSeek | MMLU-Pro, IMO | RL-based Logic | [Notes](./survey/2026-03-24-deepseek-v3-2.md) | [arXiv](https://arxiv.org/abs/2512.02556) |
| **ARC-AGI-2 Report** | ARC Prize | Visual Abduction | Non-semantic Logic | [Notes](./survey/2026-03-24-arc-agi-2.md) | [arXiv](https://arxiv.org/abs/2603.06590) |
| **GPT-5.4 mini/nano**| OpenAI | Agentic Efficiency | OSWorld-mini | [Notes](./survey/2026-03-22-gpt-5-4-mini.md) | [OpenAI Blog](https://openai.com/index/introducing-gpt-5-4-mini-and-nano/) |
| **Gemini 3.1 Pro** | Google | ARC-AGI-2, GPQA | 77.1% ARC-AGI-2 | [Notes](./survey/2026-02-19-gemini-3-1-pro.md) | [DeepMind Blog](https://deepmind.google/technologies/gemini/) |

---
### 📚 [View Full SOTA Archive (Total History)](./ARCHIVE.md)

---

## LLM Benchmarks

### Reasoning, Knowledge & Logic
| Name | Task | Dataset | Metric | SOTA (Mar 2026) | Notes | Links |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **GPQA Diamond** | PhD Science | 198 QA | Acc | **95.4%** | [Notes](./survey/2023-11-20-gpqa-diamond.md) | [arXiv](https://arxiv.org/abs/2311.12022) |
| **SimpleQA** | Factuality | 4,326 Fact QA | F1 Score | **55.6 F1** | [Notes](./survey/2024-11-01-simpleqa.md) | [arXiv](https://arxiv.org/abs/2411.04368) |
| **BenchHub** | Meta-Eval | 839K Qs / 54 Bench | Customizable | **SOTA** | [Notes](./survey/2025-06-01-benchhub.md) | [arXiv](https://arxiv.org/abs/2506.00482) |
| **LiveBench 2026** | Contamination | Monthly | Avg Score | **80.28** | [Notes](./survey/2026-01-20-livebench-v6.md) | [LiveBench](https://livebench.ai/) |
| **AcademicEval** | Writing | arXiv Papers | Judge Score | **Baseline** | [Notes](./survey/2025-10-20-academiceval.md) | [arXiv](https://arxiv.org/abs/2510.17725) |
| **DeepSeek-V3** | Knowledge | 14.8T Tokens | MMLU-Pro | **75.1%** | [Notes](./survey/2025-05-15-deepseek-v3.md) | [arXiv](https://arxiv.org/abs/2412.19437) |
| **SurveyBench** | Lit Review | 11.3k Papers | Qual | **Baseline** | [Notes](./survey/2025-10-03-surveybench.md) | [arXiv](https://arxiv.org/abs/2510.03120) |
| **LPFQA** | Tech Forums | 430 Tasks | Reasoning | **High Diff** | [Notes](./survey/2026-01-08-lpfqa.md) | [arXiv](https://arxiv.org/abs/2511.06346) |
| **PLawBench** | Legal | 850 Cases | Rubric | **SOTA** | [Notes](./survey/2026-01-23-plawbench.md) | [arXiv](https://arxiv.org/abs/2601.16669) |
| **NC-Bench** | Conv. | IBM Patterns | Pattern | **New Metric** | [Notes](./survey/2026-01-06-nc-bench.md) | [arXiv](https://arxiv.org/abs/2601.06426) |

### Agentic, Coding & Security
| Name | Task | Dataset | Metric | SOTA (Mar 2026) | Notes | Links |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **ToolBench** | Tool Use | 16,459 APIs | Pass Rate | **SOTA** | [Notes](./survey/2025-01-15-toolbench.md) | [arXiv](https://arxiv.org/abs/2307.16789) |
| **PentestEval** | Cybersecurity | 346 Pentest Tasks | E2E Success % | **31%** | [Notes](./survey/2025-12-15-pentesteval.md) | [arXiv](https://arxiv.org/abs/2512.14233) |
| **SWE-bench Ver.** | Engineering | 500 Issues | Resolved % | **80.8%** | [Notes](./survey/2026-03-23-claude-4-6.md) | [SWE-bench](https://www.swebench.com/) |
| **OSWorld-Ver.** | OS Nav | Desktop Nav | Success % | **75.0%** | [Notes](./survey/2026-03-05-gpt-5-4-report.md) | [OSWorld](https://os-world.github.io/) |
| **Llama 4 Scout** | RAG | 10M Window | TPS | **2600 TPS** | [Notes](./survey/2026-02-20-llama-4-scout.md) | [Meta Llama](https://llama.meta.com/) |

---

## VLM Benchmarks

### Multimodal & Physical Reasoning
| Name | Task | Dataset | Metric | SOTA (Mar 2026) | Notes | Links |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **MathVision** | Math | 3k Problems | Acc | **75.95%** | [Notes](./survey/2026-01-14-step3-vl.md) | [arXiv](https://arxiv.org/abs/2402.14804) |
| **Humanity's Last Exam**| Expert | 2.5K Expert Qs | Accuracy | **46.2%** | [Notes](./survey/2025-01-20-hle-survey.md) | [HLE Site](https://lastexam.ai/) |
| **PhysBench** | World | 10k entries | Dynamics | **Baseline** | [Notes](./survey/2025-02-28-physbench.md) | [GitHub](https://github.com/USC-GVL/PhysBench) |
| **Step3-VL-10B** | Efficient | 1.2T MM Tokens | MMMU/MathV | **80.11%** | [Notes](./survey/2026-01-14-step3-vl.md) | [arXiv](https://arxiv.org/abs/2601.09668) |
| **XLRS-Bench** | Remote Sensing | 45,942 Annotations | VQA / Ground Acc | **Baseline** | [Notes](./survey/2025-03-30-xlrs-bench.md) | [arXiv](https://arxiv.org/abs/2503.23771) |
| **VL-RewardBench** | Reward Models | 1,250 Pref Examples | Judgment Acc | **65.4%** | [Notes](./survey/2024-11-26-vl-rewardbench.md) | [arXiv](https://arxiv.org/abs/2411.17451) |

### Document Parsing, Video & RAG Understanding
| Name | Task | Dataset | Metric | SOTA (Mar 2026) | Notes | Links |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **OmniDocBench** | Parsing | 1,355 Images | OCR Acc | **94.6%** | [Notes](./survey/2026-03-04-omnidocbench.md) | [arXiv](https://arxiv.org/abs/2601.21957) |
| **MotionBench** | Video Motion | 5,000 Videos | Motion QA Acc | **Baseline** | [Notes](./survey/2025-01-06-motionbench.md) | [arXiv](https://arxiv.org/abs/2501.02955) |
| **VLR-Bench** | Vision-RAG | 300 RAG VQA | RAG Accuracy | **Baseline** | [Notes](./survey/2024-12-10-vlr-bench.md) | [arXiv](https://arxiv.org/abs/2412.10151) |
| **TemporalBench** | Video | 10k QA | Binary Acc | **38.0%** | [Notes](./survey/2026-01-10-temporalbench.md) | [NeurIPS](https://neurips.cc/virtual/2024/103554) |
| **MM-IFEngine** | Instruct | 23k SFT/DPO | Constraint % | **64.6%** | [Notes](./survey/2025-04-10-mm-ifengine.md) | [GitHub](https://github.com/SYuan03/MM-IFEngine) |
| **olmOCR (AI2)** | Parsing | 1.4M PDFs | Pass % | **SOTA** | [Notes](./survey/2025-10-05-olmocr-survey.md) | [AllenAI](https://olmocr.allenai.org/) |
| **VideoLLM Survey** | Meta | Review | Review | **Research SOTA**| [Notes](./survey/2025-05-03-videollm-survey.md) | [arXiv](https://arxiv.org/abs/2505.03829) |

---

## 🦊 FoxBrain Roadmap
- [ ] **Adopt StructEval** to verify FoxBrain's JSON-schema generation reliability.
- [ ] **Benchmark LemmaBench** for internal R&D mathematical verification.
- [ ] **Test ToolBench** for agentic multi-API orchestration capabilities.
- [ ] **Run SimpleQA** on every FoxBrain checkpoint as hallucination stress-test before production.
- [ ] **Integrate BenchHub** to unify all 54 benchmarks into a single evaluation pipeline.
- [ ] **Evaluate PentestEval** stage-by-stage to define safe agentic security capability limits.
- [ ] **Assess MotionBench** for manufacturing inspection and assembly-line motion-detection tasks.
- [ ] **Gate RLHF runs with VL-RewardBench** to validate reward model quality before alignment training.
