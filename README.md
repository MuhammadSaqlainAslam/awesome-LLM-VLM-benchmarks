# SOTA LLM/VLM Benchmarks Digest

A curated dashboard of the frontier in AI evaluation. **Updated Daily: Target 8 Papers/Day.**

---

## 🚀 Today's Daily 8 (April 9, 2026)

| Paper | Modality | Benchmarks | Datasets | Metrics | Notes | Links |
| :--- | :---: | :--- | :--- | :--- | :--- | :--- |
| **GDPval** | LLM | GDPval / GDPval-AA | 1,320 Tasks / 44 Occupations / 9 Sectors | Expert Win Rate / ELO | [Notes](./survey/2025-10-05-gdpval.md) | [arXiv](https://arxiv.org/abs/2510.04374) |
| **Terminal-Bench** | LLM | Terminal-Bench | 89 Tasks / 10 CLI Categories | Pass Rate | [Notes](./survey/2026-01-17-terminal-bench.md) | [arXiv](https://arxiv.org/abs/2601.11868) |
| **AA-Omniscience** | LLM | AA-Omniscience | 6,000 Qs / 6 Domains / 42 Subtopics | Omniscience Index | [Notes](./survey/2025-11-17-aa-omniscience.md) | [arXiv](https://arxiv.org/abs/2511.13029) |
| **CritPt** | LLM | CritPt | 71 Challenges / 190 Checkpoints / 12 Physics Domains | Challenge Acc | [Notes](./survey/2025-09-30-critpt.md) | [arXiv](https://arxiv.org/abs/2509.26574) |
| **MMLU-Pro** | LLM | MMLU-Pro | 12,032 Qs / 14 Disciplines | Accuracy | [Notes](./survey/2024-06-03-mmlu-pro.md) | [arXiv](https://arxiv.org/abs/2406.01574) |
| **Global MMLU** | LLM | Global MMLU | 601,734 Instances / 42 Languages | Accuracy / Cultural Bias | [Notes](./survey/2024-12-04-global-mmlu.md) | [arXiv](https://arxiv.org/abs/2412.03304) |
| **MMT-Bench** | VLM | MMT-Bench | 31,325 Qs / 32 Meta-Tasks / 162 Subtasks | Accuracy | [Notes](./survey/2024-04-24-mmt-bench.md) | [arXiv](https://arxiv.org/abs/2404.16006) |
| **WebArena** | LLM | WebArena | 812 Tasks / 5 Websites / 3 Categories | Task Success Rate | [Notes](./survey/2023-07-25-webarena.md) | [arXiv](https://arxiv.org/abs/2307.13854) |
| **Reasoning Gym** | LLM | Reasoning Gym | 100+ Tasks / 11 Domains | Zero-Shot Score | [Notes](./survey/2025-05-30-reasoning-gym.md) | [arXiv](https://arxiv.org/abs/2505.24760) |
| **PaperBench** | LLM | PaperBench | 20 ICML 2024 Papers / 8,316 Rubric Nodes | Replication Score | [Notes](./survey/2025-04-02-paperbench.md) | [arXiv](https://arxiv.org/abs/2504.01848) |
| **MultiAgentBench** | LLM | MultiAgentBench | 6 Scenarios / 400+ Test Cases | Task Score / Coord Score | [Notes](./survey/2025-03-03-multiagentbench.md) | [arXiv](https://arxiv.org/abs/2503.01935) |

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
| **ERNIE 5.0** | Baidu | MMMU / MMBench | Trillion-Param Unified MoE | [Notes](./survey/2026-02-07-ernie-5.md) | [arXiv](https://arxiv.org/abs/2602.04705) |
| **Emu3.5** | BAAI | TIIF-Bench / LeX-Bench / OneIG-EN | 94.03 TIIF-Bench; 20× Gen Speedup | [Notes](./survey/2025-10-30-emu3-5.md) | [arXiv](https://arxiv.org/abs/2510.26583) |
| **Qwen3.5-Omni** | Alibaba Cloud | 215 Audio/AV Benchmarks | WER 1.11 Librispeech; 119 Languages | [Notes](./survey/2025-09-22-qwen3-5-omni.md) | [arXiv](https://arxiv.org/abs/2509.17765) |

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
| **HalluLens** | Hallucination | Dynamic Sets | Extrinsic+Intrinsic | **ACL 2025** | [Notes](./survey/2025-04-24-hallulens.md) | [arXiv](https://arxiv.org/abs/2504.17550) |
| **LegalEval-Q** | Legal Quality | 49 LLMs | Clarity/Coherence | **14B Plateau** | [Notes](./survey/2025-05-30-legaleval-q.md) | [arXiv](https://arxiv.org/abs/2505.24826) |
| **SDE Framework** | Sci. Discovery | Bio/Chem/Phys | Project-level Acc | **Baseline** | [Notes](./survey/2025-12-17-sde-framework.md) | [arXiv](https://arxiv.org/abs/2512.15567) |
| **BenchBench** | Meta-Eval | 9 Variants / 15K | Discriminability | **New** | [Notes](./survey/2026-03-21-benchbench.md) | [arXiv](https://arxiv.org/abs/2603.20807) |
| **MultiChallenge** | Multi-turn Conv | 273 Conversations | Pass Rate | **41.4%** | [Notes](./survey/2025-01-29-multichallenge.md) | [arXiv](https://arxiv.org/abs/2501.17399) |
| **Sci2Pol** | Sci→Policy | 18 Tasks | Quality Score | **Baseline** | [Notes](./survey/2025-09-25-sci2pol.md) | [arXiv](https://arxiv.org/abs/2509.21493) |
| **Thunder-NUBench** | Negation | 1,261 MCQ Items | Accuracy | **EACL 2026** | [Notes](./survey/2025-06-17-thunder-nubench.md) | [arXiv](https://arxiv.org/abs/2506.14397) |
| **DSR-Bench** | Structural Reasoning | 4,140 Instances | Struct. Acc | **0.46/1.0** | [Notes](./survey/2025-05-29-dsr-bench.md) | [arXiv](https://arxiv.org/abs/2505.24069) |
| **OmniScience** | Scientific Reasoning | Expert Science QA | Accuracy | **0.72 GPQA-Diamond** | [Notes](./survey/2025-03-25-omniscience.md) | [arXiv](https://arxiv.org/abs/2503.17604) |
| **MathArena** | Competition Math | 162 Problems / 7 Competitions | Accuracy / Proof Score | **91.25% (GPT-5 numerical)** | [Notes](./survey/2025-05-29-matharena.md) | [arXiv](https://arxiv.org/abs/2505.23281) |
| **OlymMATH** | Olympiad Math | 200 Problems / EN+ZH / 2 Tiers | Pass@1 | **58.4% EN-HARD (Gemini 2.5 Pro)** | [Notes](./survey/2025-03-27-olymmath.md) | [arXiv](https://arxiv.org/abs/2503.21380) |
| **OMNI-MATH** | Olympiad Math | 4,428 Problems / 33+ Subdomains | Accuracy | **60.54% (o1-mini)** | [Notes](./survey/2024-10-10-omni-math.md) | [arXiv](https://arxiv.org/abs/2410.07985) |
| **RULER** | Long-Context | 13 Tasks / 6 Context Lengths (4K–128K) | Avg Score | **81.2% @ 128K (GPT-4)** | [Notes](./survey/2024-04-09-ruler.md) | [arXiv](https://arxiv.org/abs/2404.06654) |
| **LongBench v2** | Long-Context Reasoning | 503 MCQ / 8K–2M Words | Accuracy | **63.3% (Gemini 2.5 Pro)** | [Notes](./survey/2024-12-19-longbench-v2.md) | [arXiv](https://arxiv.org/abs/2412.15204) |
| **IFBench** | Instruction Following | 58 Constraints / 300 Prompts | IF Accuracy | **54.7% (Qwen 2.5 7B + RLVR)** | [Notes](./survey/2025-07-03-ifbench.md) | [arXiv](https://arxiv.org/abs/2507.02833) |
| **AA-Omniscience** | Cross-Domain Knowledge | 6,000 Qs / 6 Domains / 42 Subtopics | Omniscience Index | **OI 33 (Gemini 3.1 Pro)** | [Notes](./survey/2025-11-17-aa-omniscience.md) | [arXiv](https://arxiv.org/abs/2511.13029) |
| **CritPt** | Frontier Physics Research | 71 Challenges / 190 Checkpoints | Challenge Acc | **30.0% (GPT-5.4 Pro)** | [Notes](./survey/2025-09-30-critpt.md) | [arXiv](https://arxiv.org/abs/2509.26574) |
| **MMLU-Pro** | Multi-Domain Knowledge | 12,032 Qs / 14 Disciplines / 10-option MCQ | Accuracy | **90.99% (Gemini 3.1 Pro)** | [Notes](./survey/2024-06-03-mmlu-pro.md) | [arXiv](https://arxiv.org/abs/2406.01574) |
| **Global MMLU** | Multilingual Knowledge | 601,734 Instances / 42 Languages | Accuracy / Cultural Bias | **CS: 5.7 rank shifts vs. MMLU** | [Notes](./survey/2024-12-04-global-mmlu.md) | [arXiv](https://arxiv.org/abs/2412.03304) |
| **Reasoning Gym** | Reasoning / RLVR Training | 100+ Tasks / 11 Domains | Zero-Shot Score | **63.5% (o3-mini, hard)** | [Notes](./survey/2025-05-30-reasoning-gym.md) | [arXiv](https://arxiv.org/abs/2505.24760) |

### Agentic, Coding & Security
| Name | Task | Dataset | Metric | SOTA (Mar 2026) | Notes | Links |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **ToolBench** | Tool Use | 16,459 APIs | Pass Rate | **SOTA** | [Notes](./survey/2025-01-15-toolbench.md) | [arXiv](https://arxiv.org/abs/2307.16789) |
| **PentestEval** | Cybersecurity | 346 Pentest Tasks | E2E Success % | **31%** | [Notes](./survey/2025-12-15-pentesteval.md) | [arXiv](https://arxiv.org/abs/2512.14233) |
| **SWE-bench Ver.** | Engineering | 500 Issues | Resolved % | **80.8%** | [Notes](./survey/2026-03-23-claude-4-6.md) | [SWE-bench](https://www.swebench.com/) |
| **OSWorld-Ver.** | OS Nav | Desktop Nav | Success % | **75.0%** | [Notes](./survey/2026-03-05-gpt-5-4-report.md) | [OSWorld](https://os-world.github.io/) |
| **Llama 4 Scout** | RAG | 10M Window | TPS | **2600 TPS** | [Notes](./survey/2026-02-20-llama-4-scout.md) | [Meta Llama](https://llama.meta.com/) |
| **RepoReason** | Code Reasoning | 2,492 Tasks | ESV/MCL/DFI | **Baseline** | [Notes](./survey/2026-01-07-reporeason.md) | [arXiv](https://arxiv.org/abs/2601.03731) |
| **PaperArena** | Sci. Lit. Agent | 784 QA Pairs | Accuracy | **38.78%** | [Notes](./survey/2025-10-13-paperarena.md) | [arXiv](https://arxiv.org/abs/2510.10909) |
| **AgentBench** | LLM as Agent | 8 Environments | Task Success % | **ICLR 2024** | [Notes](./survey/2023-08-07-agentbench.md) | [arXiv](https://arxiv.org/abs/2308.03688) |
| **MemBench** | Agent Memory | 53K Questions | Accuracy/Recall | **ACL 2025** | [Notes](./survey/2025-06-20-membench.md) | [arXiv](https://arxiv.org/abs/2506.21605) |
| **ENAMEL** | Code Efficiency | 30 LLMs | eff@k | **ICLR 2025** | [Notes](./survey/2024-06-10-enamel.md) | [arXiv](https://arxiv.org/abs/2406.06647) |
| **SKA-Bench** | Struct. Knowledge | 921 QA × 4 Tests | Accuracy | **EMNLP 2025** | [Notes](./survey/2025-07-23-ska-bench.md) | [arXiv](https://arxiv.org/abs/2507.17178) |
| **LiveCodeBench Pro** | Competitive Programming | Codeforces / ICPC / IOI | Pass@1 | **53% Med / 0% Hard** | [Notes](./survey/2025-06-13-livecodebench-pro.md) | [arXiv](https://arxiv.org/abs/2506.11928) |
| **SciCode** | Scientific Research Coding | 338 Subproblems / 5 Domains | Pass@1 | **4.6% Main (Claude 3.5)** | [Notes](./survey/2024-07-18-scicode.md) | [arXiv](https://arxiv.org/abs/2407.13168) |
| **GDPval** | Real-World Economic Tasks | 1,320 Tasks / 44 Occupations | Expert Win Rate | **47.6% (Claude Opus 4.1)** | [Notes](./survey/2025-10-05-gdpval.md) | [arXiv](https://arxiv.org/abs/2510.04374) |
| **Terminal-Bench** | CLI / Terminal Agent Tasks | 89 Tasks / 10 Categories | Pass Rate | **62.9% (GPT-5.2 + Codex CLI)** | [Notes](./survey/2026-01-17-terminal-bench.md) | [arXiv](https://arxiv.org/abs/2601.11868) |
| **WebArena** | Web Agent Tasks | 812 Tasks / 5 Websites | Task Success Rate | **~58% CUA (vs. 78% Human)** | [Notes](./survey/2023-07-25-webarena.md) | [arXiv](https://arxiv.org/abs/2307.13854) |
| **PaperBench** | AI Research Replication | 20 ICML 2024 Papers / 8,316 Rubric Nodes | Replication Score | **26.0% (o1 Iterative 36h)** | [Notes](./survey/2025-04-02-paperbench.md) | [arXiv](https://arxiv.org/abs/2504.01848) |
| **MultiAgentBench** | Multi-Agent Collab/Compete | 6 Scenarios / 400+ Test Cases | Task Score / Coord Score | **84.13% TS (GPT-4o-mini, Research)** | [Notes](./survey/2025-03-03-multiagentbench.md) | [arXiv](https://arxiv.org/abs/2503.01935) |

---

## VLM Benchmarks

### Multimodal & Physical Reasoning
| Name | Task | Dataset | Metric | SOTA (Mar 2026) | Notes | Links |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **MathVision** | Math | 3k Problems | Acc | **75.95%** | [Notes](./survey/2026-01-14-step3-vl.md) | [arXiv](https://arxiv.org/abs/2402.14804) |
| **Humanity's Last Exam**| Expert | 2.5K Expert Qs / ~10% Multimodal | Accuracy | **44.3% (GPT-5.4-pro)** | [Notes](./survey/2025-01-20-hle-survey.md) | [HLE Site](https://lastexam.ai/) |
| **PhysBench** | World | 10k entries | Dynamics | **Baseline** | [Notes](./survey/2025-02-28-physbench.md) | [GitHub](https://github.com/USC-GVL/PhysBench) |
| **Step3-VL-10B** | Efficient | 1.2T MM Tokens | MMMU/MathV | **80.11%** | [Notes](./survey/2026-01-14-step3-vl.md) | [arXiv](https://arxiv.org/abs/2601.09668) |
| **XLRS-Bench** | Remote Sensing | 45,942 Annotations | VQA / Ground Acc | **Baseline** | [Notes](./survey/2025-03-30-xlrs-bench.md) | [arXiv](https://arxiv.org/abs/2503.23771) |
| **VL-RewardBench** | Reward Models | 1,250 Pref Examples | Judgment Acc | **65.4%** | [Notes](./survey/2024-11-26-vl-rewardbench.md) | [arXiv](https://arxiv.org/abs/2411.17451) |
| **VCBench** | Multi-Image Math | 1,720 Problems | Accuracy | **<50%** | [Notes](./survey/2025-04-24-vcbench.md) | [arXiv](https://arxiv.org/abs/2504.18589) |
| **VLM-RobustBench** | Robustness | 49 Augment Types | Robustness Gap | **-34pp** | [Notes](./survey/2026-03-06-vlm-robustbench.md) | [arXiv](https://arxiv.org/abs/2603.06148) |
| **MathVista** | Visual Math | 6,141 Examples | Accuracy | **49.9%** | [Notes](./survey/2023-10-03-mathvista.md) | [arXiv](https://arxiv.org/abs/2310.02255) |
| **MATHVERSE** | Visual Math Diagrams | 2,612 Problems / 15K Samples | CoT Step Acc | **ECCV 2024** | [Notes](./survey/2024-03-22-mathverse.md) | [arXiv](https://arxiv.org/abs/2403.14624) |
| **VisNumBench** | Number Sense | ~1,900 MCQ / 7 Attributes | Accuracy | **Below Human** | [Notes](./survey/2025-03-19-visnumbench.md) | [arXiv](https://arxiv.org/abs/2503.14939) |
| **Uni-MMMU** | Unified Gen+Understanding | 8 Bidirectional Tasks | Task Accuracy | **Baseline** | [Notes](./survey/2025-10-17-uni-mmmu.md) | [arXiv](https://arxiv.org/abs/2510.13759) |
| **MMFineReason** | Fine-Grained Reasoning | 1.8M Samples / 5.1B Tokens | Reasoning Acc | **8B > 30B-A3B** | [Notes](./survey/2026-01-29-mmfinereason.md) | [arXiv](https://arxiv.org/abs/2601.21821) |
| **DynaMath** | Visual Math Robustness | 5,010 Variants / 9 Topics | Worst-Case Acc | **35.3% (Claude-3.5)** | [Notes](./survey/2024-10-29-dynamath.md) | [arXiv](https://arxiv.org/abs/2411.00836) |
| **R1-Onevision** | Visual Math Reasoning | 155K Samples / 942 Bench Qs | Math Reasoning Acc | **46.4% MathVerse (7B)** | [Notes](./survey/2025-03-13-r1-onevision.md) | [arXiv](https://arxiv.org/abs/2503.10615) |
| **EMMA** | Cross-Modal Reasoning | 2,788 Problems / 4 Domains | Accuracy | **27% Below Human** | [Notes](./survey/2025-01-09-emma.md) | [arXiv](https://arxiv.org/abs/2501.05444) |
| **VLM2-Bench** | Visual Cue Linking | 3,060 QA / 9 Subtasks | Accuracy | **34.8% Below Human** | [Notes](./survey/2025-02-17-vlm2-bench.md) | [arXiv](https://arxiv.org/abs/2502.12084) |
| **VisionArena** | VLM Preference Eval | 230K Convos / 500 Prompts | Preference Acc | **+17 MMMU (SFT)** | [Notes](./survey/2024-12-11-visionarena.md) | [arXiv](https://arxiv.org/abs/2412.08687) |
| **MMMU-Pro** | Expert Multimodal QA | 11.5K Expert Questions | Accuracy | **46.2% (vs 80%+ MMMU)** | [Notes](./survey/2026-03-20-mmmu-pro-survey.md) | [Leaderboard](https://mmmu-benchmark.github.io/#leaderboard) |
| **OlympiadBench** | Bilingual Multimodal Sci. | 8,476 Problems / Math+Physics | Accuracy | **17.23% (GPT-4V)** | [Notes](./survey/2024-02-21-olympiadbench.md) | [arXiv](https://arxiv.org/abs/2402.14008) |
| **MMT-Bench** | Multitask Visual Understanding | 31,325 Qs / 32 Meta-Tasks / 162 Subtasks | Accuracy | **63.4% (InternVL-v1.2-34B)** | [Notes](./survey/2024-04-24-mmt-bench.md) | [arXiv](https://arxiv.org/abs/2404.16006) |

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
| **ROVER** | Embodied Video Reasoning | 543 Videos / 27 Tasks | VQA / Progress Acc | **Baseline** | [Notes](./survey/2025-08-04-rover.md) | [arXiv](https://arxiv.org/abs/2508.01943) |
| **FineVision** | Multimodal Training Data | 24M Samples / 185 Subsets | Avg Score (11 Bench) | **+46.3% vs LLaVA-OV** | [Notes](./survey/2025-10-22-finevision.md) | [arXiv](https://arxiv.org/abs/2510.17269) |

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
- [ ] **Adapt BenchBench** pipeline to auto-generate FoxBrain-specific test suites for manufacturing/logistics verticals.
- [ ] **Stress-test VLM pipeline with VLM-RobustBench** geometric augmentations before any factory-floor visual deployment.
- [ ] **Diagnose RepoReason DFI score** for FoxBrain's cross-file code reasoning ceiling before repository-level agentic tasks.
- [ ] **Evaluate VCBench** multi-image domains (spatial, temporal) for assembly-sequence and process-diagram understanding.
- [ ] **Benchmark PaperArena** to measure FoxBrain's R&D literature-grounded reasoning gap vs. Ph.D. expert baseline.
- [ ] **Run HalluLens extrinsic+intrinsic suites** before any FoxBrain production release touching factual/RAG outputs.
- [ ] **Apply LegalEval-Q** quality scoring to FoxBrain compliance outputs; prioritize reasoning-architecture models over scale.
- [ ] **Pilot SDE Framework** on materials science / process engineering scenarios relevant to Foxconn R&D projects.
- [ ] **Run MemBench factual+reflective suites** before deploying FoxBrain in any long-horizon, multi-session agent workflow.
- [ ] **Score DSR-Bench structural reasoning** on supply chain graphs, BOM trees, and dependency hierarchies before agentic deployment.
- [ ] **Evaluate MultiChallenge** (all 4 categories) in extended-session FoxBrain deployments before any customer-facing release.
- [ ] **Apply Sci2Pol 5-stage taxonomy** to FoxBrain's regulatory/ESG report generation to identify the weakest stage (Verification).
- [ ] **Test Thunder-NUBench negation categories** for any FoxBrain pipeline handling compliance text or QC specifications.
- [ ] **Run SKA-Bench Negative Rejection testbed** against FoxBrain's KG-augmented RAG to prevent hallucination on unsupported queries.
- [ ] **Adopt ENAMEL eff@k metric** as a standard evaluation layer in FoxBrain's code generation pipeline alongside pass@k.
- [ ] **Use AgentBench as the baseline** before and after every major FoxBrain agent architecture upgrade.
- [ ] **Target MathVista >60.3%** (above human baseline) for FoxBrain's visual analytics deployments on engineering charts and figures.
- [ ] **Run MATHVERSE Vision-Only variant** on FoxBrain before any deployment involving engineering schematics or circuit diagrams — confirm genuine diagram reading vs. text shortcutting.
- [ ] **Score VisNumBench number-sense tasks** on FoxBrain; prioritize visual numerical estimation fine-tuning for manufacturing QC (defect density, component counts, gauge readings).
- [ ] **Evaluate Uni-MMMU generation-aided tasks** to test whether FoxBrain can generate intermediate visual outputs (sketches, diagrams) as cognitive scaffolds during reasoning.
- [ ] **Apply ROVER recursive decomposition** to FoxBrain's assembly-line video analysis pipeline to handle long inspection videos at linear compute cost.
- [ ] **Adopt MMFineReason 7%-subset filtering strategy** for FoxBrain's fine-tuning data curation: prioritize 123K high-difficulty manufacturing reasoning traces over larger lower-quality sets.
- [ ] **Adapt FineVision decontamination pipeline** to unify Foxconn's internal visual datasets; validate against 66 benchmark contamination filters before any FoxBrain multimodal fine-tuning run.
- [ ] **Evaluate OmniScience three-stage training pipeline** as a blueprint for FoxBrain-Science: domain pretraining → instruction tuning → reasoning distillation for materials science and R&D verticals.
- [ ] **Study ERNIE 5.0 elastic training paradigm** for FoxBrain's edge-vs-cloud deployment strategy: a single checkpoint family serving both fast factory-floor inference and high-accuracy central analysis.
