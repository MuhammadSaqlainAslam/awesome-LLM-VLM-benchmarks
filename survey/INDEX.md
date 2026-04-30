# Survey Notes — Index by Domain

Deep-dive notes for every paper in the digest, organised by topic area.  
Each file follows the same structure: **Problem → Method → Key Results → Enterprise / Industry Relevance.**

For the full benchmark reference table, see [BENCHMARKS.md](../BENCHMARKS.md).  
For daily and weekly digests, see [README.md](../README.md) and [WEEKLY.md](../WEEKLY.md).

---

## Contents
1. [Reasoning, Mathematics & Knowledge](#1-reasoning-mathematics--knowledge)
2. [Agentic Systems & Tool Use](#2-agentic-systems--tool-use)
3. [Agent Safety & Alignment](#3-agent-safety--alignment)
4. [Multimodal & Visual Reasoning](#4-multimodal--visual-reasoning)
5. [Document, Video & RAG](#5-document-video--rag)
6. [Domain-Specific (Medical, Legal, Finance, Science)](#6-domain-specific-medical-legal-finance-science)
7. [Multilingual & Cross-Cultural](#7-multilingual--cross-cultural)
8. [Speech & Audio](#8-speech--audio)
9. [Coding & Software Engineering](#9-coding--software-engineering)
10. [Frontier Model Reports](#10-frontier-model-reports)
11. [Meta-Evaluation & Methodology](#11-meta-evaluation--methodology)

---

## 1. Reasoning, Mathematics & Knowledge

| Paper | Year | Key Claim | File |
| :--- | :---: | :--- | :--- |
| **GPQA Diamond** | 2023 | PhD-level science QA; human experts at 65% | [📄](./2023-11-20-gpqa-diamond.md) |
| **MathVista** | 2023 | Visual math; models far below human baseline | [📄](./2023-10-03-mathvista.md) |
| **MATHVERSE** | 2024 | Diagram math; CoT step accuracy on visual variants | [📄](./2024-03-22-mathverse.md) |
| **RULER** | 2024 | Long-context retrieval up to 128K tokens | [📄](./2024-04-09-ruler.md) |
| **OMNI-MATH** | 2024 | Olympiad math across 33+ subdomains | [📄](./2024-10-10-omni-math.md) |
| **DynaMath** | 2024 | Visual math robustness across 5,010 variants | [📄](./2024-10-29-dynamath.md) |
| **SimpleQA** | 2024 | Factuality; models only 55% on short factual Qs | [📄](./2024-11-01-simpleqa.md) |
| **LongBench v2** | 2024 | Long-context reasoning up to 2M words | [📄](./2024-12-19-longbench-v2.md) |
| **MMLU-Pro** | 2024 | Multi-domain 10-option MCQ; 14 disciplines | [📄](./2024-06-03-mmlu-pro.md) |
| **Global MMLU** | 2024 | Multilingual MMLU across 42 languages | [📄](./2024-12-04-global-mmlu.md) |
| **MultiChallenge** | 2025 | Multi-turn conversation; 41.4% best pass rate | [📄](./2025-01-29-multichallenge.md) |
| **OmniScience** | 2025 | Expert science QA; three-stage training pipeline | [📄](./2025-03-25-omniscience.md) |
| **OlymMATH** | 2025 | Olympiad math EN+ZH; 2 difficulty tiers | [📄](./2025-03-27-olymmath.md) |
| **DSR-Bench** | 2025 | Structural reasoning; 4,140 instances | [📄](./2025-05-29-dsr-bench.md) |
| **MathArena** | 2025 | Competition math; 162 problems / 7 competitions | [📄](./2025-05-29-matharena.md) |
| **Reasoning Gym** | 2025 | 100+ tasks for RLVR training | [📄](./2025-05-30-reasoning-gym.md) |
| **IFBench** | 2025 | Instruction following; 58 constraints | [📄](./2025-07-03-ifbench.md) |
| **AA-Omniscience** | 2025 | Cross-domain knowledge; Omniscience Index | [📄](./2025-11-17-aa-omniscience.md) |
| **SDE Framework** | 2025 | Scientific discovery across Bio/Chem/Phys | [📄](./2025-12-17-sde-framework.md) |
| **ImplicitMemBench** | 2026 | Implicit memory (procedural/priming/conditioning) | [📄](./2026-04-09-implicitmembench.md) |
| **Riemann-Bench** | 2026 | Research-level math; <10% all frontier models | [📄](./2026-04-08-riemann-bench.md) |
| **TEMPER** | 2026 | Emotional robustness; −2 to −10 pp across 18 models | [📄](./2026-04-09-temper.md) |
| **KDR-Bench** | 2026 | Deep research across structured + unstructured data | [📄](./2026-04-09-kdr-bench.md) |
| **METER** | 2026 | Causal reasoning; Pearl's 3-rung ladder | [📄](./2026-04-13-meter.md) |
| **General365** | 2026 | K-12 reasoning robustness; 1,460 problems | [📄](./2026-04-13-general365.md) |
| **REL** | 2026 | Relational reasoning; arity bottleneck | [📄](./2026-04-14-rel.md) |
| **PolicyBench** | 2026 | Public policy; Bloom's taxonomy levels | [📄](./2026-04-14-policybench.md) |
| **QuantSightBench** | 2026 | Quantitative forecasting with prediction intervals | [📄](./2026-04-17-quantsightbench.md) |
| **KWBench** | 2026 | Unprompted problem recognition; 27.9% best model | [📄](./2026-04-17-kwbench.md) |
| **KnowledgeBerg** | 2026 | Knowledge width + depth; 17 languages | [📄](./2026-04-19-knowledgeberg.md) |
| **MIRROR** | 2026 | Metacognitive calibration; 4-level hierarchy | [📄](./2026-04-23-mirror.md) |
| **CLARITY** | 2026 | NL2SQL under conversational ambiguity | [📄](./2026-04-25-clarity.md) |
| **BLAST** | 2026 | ASP declarative code generation | [📄](./2026-04-25-blast.md) |
| **Rethinking Math Eval** | 2026 | Symbolic eval failures; LLM-as-judge is better | [📄](./2026-04-25-rethinking-math-eval.md) |
| **AutoResearchBench** | 2026 | Scientific lit. discovery; ~9% frontier LLMs | [📄](./2026-04-29-autoresearchbench.md) |
| **DialToM** | 2026 | Theory of Mind; ≥80% literal, ≤25% functional | [📄](./2026-04-22-dialtom.md) |
| **ActuBench** | 2026 | Actuarial science; 50 LLMs on IAA syllabus | [📄](./2026-04-22-actubench.md) |

---

## 2. Agentic Systems & Tool Use

| Paper | Year | Key Claim | File |
| :--- | :---: | :--- | :--- |
| **AgentBench** | 2023 | General agent baseline across 8 environments | [📄](./2023-08-07-agentbench.md) |
| **WebArena** | 2023 | Web agent across 5 realistic websites | [📄](./2023-07-25-webarena.md) |
| **ToolBench** | 2025 | Tool use across 16,459 real-world APIs | [📄](./2025-01-15-toolbench.md) |
| **GDPval** | 2025 | Real-world economic task completion | [📄](./2025-10-05-gdpval.md) |
| **MultiAgentBench** | 2025 | Multi-agent collaboration and competition | [📄](./2025-03-03-multiagentbench.md) |
| **PaperArena** | 2025 | Scientific literature agent; 38.78% accuracy | [📄](./2025-10-13-paperarena.md) |
| **PaperBench** | 2025 | AI research replication from ICML 2024 papers | [📄](./2025-04-02-paperbench.md) |
| **OfficeBench** | 2024 | Office automation across 9 apps | [📄](./2024-07-26-officebench.md) |
| **Terminal-Bench** | 2026 | CLI agent across 89 terminal tasks | [📄](./2026-01-17-terminal-bench.md) |
| **RepoReason** | 2026 | Repository-level code reasoning | [📄](./2026-01-07-reporeason.md) |
| **KnowU-Bench** | 2026 | Personalised mobile GUI agent; 3 tracks | [📄](./2026-04-09-knowu-bench.md) |
| **PilotBench** | 2026 | Safety-critical aviation agent | [📄](./2026-04-10-pilotbench.md) |
| **SAGE** | 2026 | Customer service agent; 27 LLMs on DDG graphs | [📄](./2026-04-10-sage.md) |
| **BankerToolBench** | 2026 | Investment banking E2E workflows | [📄](./2026-04-13-bankertoolbench.md) |
| **AnalysisBench** | 2026 | Software analysis agent; 94% with Gemini-3-Flash | [📄](./2026-04-13-analysisbench.md) |
| **OccuBench** | 2026 | Professional occupational agent; fault injection | [📄](./2026-04-13-occubench.md) |
| **HORIZON** | 2026 | Long-horizon agent failure diagnostics | [📄](./2026-04-13-horizon.md) |
| **AAR** | 2026 | DAG-structured multi-step tool navigation | [📄](./2026-04-11-aar.md) |
| **AlphaEval** | 2026 | Production agent evaluation; 7 companies | [📄](./2026-04-14-alphaeval.md) |
| **Frontier-Eng** | 2026 | Self-evolving engineering design agents | [📄](./2026-04-14-frontier-eng.md) |
| **GeoAgentBench** | 2026 | GIS tool-augmented spatial analysis agent | [📄](./2026-04-15-geoagentbench.md) |
| **RiskWebWorld** | 2026 | GUI agent for e-commerce risk management | [📄](./2026-04-15-riskwebworld.md) |
| **FedGUI** | 2026 | Federated GUI agent across 4 heterogeneity types | [📄](./2026-04-16-fedgui.md) |
| **DR³-Eval** | 2026 | Deep research agent; distractor robustness | [📄](./2026-04-16-dr3-eval.md) |
| **HWE-Bench** | 2026 | Hardware bug repair; Verilog/SystemVerilog | [📄](./2026-04-16-hwe-bench.md) |
| **GTA-2** | 2026 | General tool agent; 14.4% workflow completion | [📄](./2026-04-17-gta-2.md) |
| **AJ-Bench** | 2026 | Agent-as-a-judge; environment-aware verification | [📄](./2026-04-20-aj-bench.md) |
| **WebCompass** | 2026 | Multimodal web code generation/editing/repair | [📄](./2026-04-20-webcompass.md) |
| **AutomationBench** | 2026 | Cross-app enterprise workflow; <10% all models | [📄](./2026-04-21-automationbench.md) |
| **PlayEval** | 2026 | GUI code playability beyond compilation | [📄](./2026-04-21-playeval.md) |
| **Memora** | 2026 | Long-term memory over weeks-to-months | [📄](./2026-04-21-memora.md) |
| **SkillLearnBench** | 2026 | Continual skill learning; self-feedback causes drift | [📄](./2026-04-21-skilllearnbench.md) |
| **MedSkillAudit** | 2026 | Pre-deployment medical skill auditing | [📄](./2026-04-23-medskillaudit.md) |
| **MuDABench** | 2026 | Multi-document analytical QA; 80K+ pages | [📄](./2026-04-25-mudabench.md) |
| **AgentSearchBench** | 2026 | Agent discovery from 10K real agents | [📄](./2026-04-25-agentsearchbench.md) |
| **DV-World** | 2026 | Data visualization agents; <50% all SOTA | [📄](./2026-04-29-dv-world.md) |
| **PSI-Bench** | 2026 | Patient simulator fidelity; framework > model scale | [📄](./2026-04-29-psi-bench.md) |

---

## 3. Agent Safety & Alignment

| Paper | Year | Key Claim | File |
| :--- | :---: | :--- | :--- |
| **HalluLens** | 2025 | Extrinsic + intrinsic hallucination benchmark | [📄](./2025-04-24-hallulens.md) |
| **TraceSafe-Bench** | 2026 | Mid-trajectory tool-calling safety violations | [📄](./2026-04-08-tracesafe-bench.md) |
| **AISafetyBenchExplorer** | 2026 | Meta-catalogue of 195 safety benchmarks | [📄](./2026-04-14-aisafetybenchexplorer.md) |
| **HINTBench** | 2026 | Intrinsic agent safety; step localisation fails | [📄](./2026-04-15-hintbench.md) |
| **SIR-Bench** | 2026 | Security incident response investigation | [📄](./2026-04-13-sir-bench.md) |
| **Terminal Wrench** | 2026 | Reward hacking in terminal environments | [📄](./2026-04-19-terminal-wrench.md) |
| **HarmfulSkillBench** | 2026 | Harmful skills nearly double agent harm score | [📄](./2026-04-16-harmfulskillbench.md) |
| **MemEvoBench** | 2026 | Memory safety degrades over long-horizon runs | [📄](./2026-04-17-memevobench.md) |
| **CodeRQ-Bench** | 2026 | Code reasoning quality beyond correctness | [📄](./2026-04-14-coderq-bench.md) |
| **Cyber Defense Benchmark** | 2026 | SOC threat hunting; 3.8% recall | [📄](./2026-04-21-cyber-defense-benchmark.md) |
| **DeepRed** | 2026 | CTF security; 35% checkpoint completion | [📄](./2026-04-21-deepred.md) |
| **CyberCertBench** | 2026 | Cybersecurity certs; IEC 62443 OT is the gap | [📄](./2026-04-22-cybercertbench.md) |

---

## 4. Multimodal & Visual Reasoning

| Paper | Year | Key Claim | File |
| :--- | :---: | :--- | :--- |
| **MMT-Bench** | 2024 | Multitask visual; 32 meta-tasks / 162 subtasks | [📄](./2024-04-24-mmt-bench.md) |
| **VL-RewardBench** | 2024 | VLM reward model evaluation | [📄](./2024-11-26-vl-rewardbench.md) |
| **VisionArena** | 2024 | VLM human preference evaluation | [📄](./2024-12-11-visionarena.md) |
| **PhysBench** | 2025 | Physical world dynamics understanding | [📄](./2025-02-28-physbench.md) |
| **VLM2-Bench** | 2025 | Visual cue linking across 9 subtasks | [📄](./2025-02-17-vlm2-bench.md) |
| **R1-Onevision** | 2025 | Visual math reasoning with R1-style training | [📄](./2025-03-13-r1-onevision.md) |
| **VisNumBench** | 2025 | Number sense for visual numerical estimation | [📄](./2025-03-19-visnumbench.md) |
| **XLRS-Bench** | 2025 | Remote sensing VLM evaluation | [📄](./2025-03-30-xlrs-bench.md) |
| **EMMA** | 2025 | Cross-modal reasoning; 27% below human | [📄](./2025-01-09-emma.md) |
| **HLE** | 2025 | Humanity's Last Exam; expert multimodal | [📄](./2025-01-20-hle-survey.md) |
| **VCBench** | 2025 | Multi-image mathematics | [📄](./2025-04-24-vcbench.md) |
| **Uni-MMMU** | 2025 | Unified generation + understanding | [📄](./2025-10-17-uni-mmmu.md) |
| **MMFineReason** | 2026 | Fine-grained visual reasoning; 1.8M samples | [📄](./2026-01-29-mmfinereason.md) |
| **MMMU-Pro** | 2026 | Expert multimodal QA; 11.5K questions | [📄](./2026-03-20-mmmu-pro-survey.md) |
| **VLM-RobustBench** | 2026 | Geometric robustness; −34 pp gap | [📄](./2026-03-06-vlm-robustbench.md) |
| **DISSECT** | 2026 | Scientific VLM; perception vs. reasoning diagnosis | [📄](./2026-04-06-dissect.md) |
| **BareBones** | 2026 | Texture-deprived silhouettes; VLM shortcut bias | [📄](./2026-04-12-barebones.md) |
| **MMRareBench** | 2026 | Rare disease multimodal clinical reasoning | [📄](./2026-04-12-mmrarebench.md) |
| **EgoEsportsQA** | 2026 | Egocentric video; tactical reasoning gap | [📄](./2026-04-14-egoesportsqa.md) |
| **DailyClue** | 2026 | Visual clue-driven reasoning in daily scenarios | [📄](./2026-04-15-dailyclue.md) |
| **MirrorBench** | 2026 | MLLM self-recognition and self-representation | [📄](./2026-04-16-mirrorbench.md) |
| **CrossMath** | 2026 | VLMs reason in text space even with images | [📄](./2026-04-17-crossmath.md) |
| **VisualTextTrap** | 2026 | Text overlay hallucination; systematic VLM failure | [📄](./2026-04-19-visualtexttrap.md) |
| **HalluAudio** | 2026 | Audio-language hallucination; music/env. hardest | [📄](./2026-04-21-halluaudio.md) |
| **MM-JudgeBench** | 2026 | Cross-lingual LVLM judge; 25 languages | [📄](./2026-04-21-mm-judgebench.md) |
| **FAS-VFM Bench** | 2026 | Vision foundation models for face anti-spoofing | [📄](./2026-04-21-fas-vfm-bench.md) |
| **OMIBench** | 2026 | Olympiad-level multi-image reasoning | [📄](./2026-04-22-omibench.md) |
| **WildFireVQA** | 2026 | Aerial wildfire RGB+thermal VQA | [📄](./2026-04-22-wildfirevqa.md) |
| **X-PCR** | 2026 | Ophthalmic 6-stage progressive clinical reasoning | [📄](./2026-04-23-x-pcr.md) |
| **CNSL-bench** | 2026 | Chinese sign language MLLMs; all below human | [📄](./2026-04-25-cnsl-bench.md) |
| **SpaMEM** | 2026 | Embodied dynamic spatial reasoning | [📄](./2026-04-25-spamem.md) |
| **LTD / UniVLT** | 2026 | Multi-view roadside traffic VQA | [📄](./2026-04-25-ltd-univlt.md) |
| **DRAGON** | 2026 | Evidence-grounded diagram QA | [📄](./2026-04-29-dragon.md) |

---

## 5. Document, Video & RAG

| Paper | Year | Key Claim | File |
| :--- | :---: | :--- | :--- |
| **VLR-Bench** | 2024 | Vision-RAG evaluation | [📄](./2024-12-10-vlr-bench.md) |
| **MotionBench** | 2025 | Video motion understanding | [📄](./2025-01-06-motionbench.md) |
| **VideoLLM Survey** | 2025 | Comprehensive video LLM review | [📄](./2025-05-03-videollm-survey.md) |
| **olmOCR** | 2025 | Large-scale PDF document parsing | [📄](./2025-10-05-olmocr-survey.md) |
| **ROVER** | 2025 | Embodied video reasoning | [📄](./2025-08-04-rover.md) |
| **FineVision** | 2025 | Multimodal training data quality | [📄](./2025-10-22-finevision.md) |
| **MM-IFEngine** | 2025 | Multimodal instruction following | [📄](./2025-04-10-mm-ifengine.md) |
| **TemporalBench** | 2026 | Video temporal reasoning | [📄](./2026-01-10-temporalbench.md) |
| **OmniDocBench** | 2026 | Enterprise document parsing | [📄](./2026-03-04-omnidocbench.md) |
| **ParseBench** | 2026 | Enterprise document parsing; 5 dimensions | [📄](./2026-04-09-parsebench.md) |
| **VSAS-Bench** | 2026 | Real-time streaming video VLM | [📄](./2026-04-08-vsas-bench.md) |
| **AVID** | 2026 | Audio-visual inconsistency in long video | [📄](./2026-04-15-avid.md) |
| **MCSC-Bench** | 2026 | Video production scripting end-to-end | [📄](./2026-04-16-mcsc-bench.md) |
| **CCTVBench** | 2026 | Traffic video; quadruple-level consistency | [📄](./2026-04-22-cctvbench.md) |
| **MuDABench** | 2026 | Multi-document analytical QA | [📄](./2026-04-25-mudabench.md) |
| **LongSumEval** | 2026 | Long-document summarisation; QA-based eval | [📄](./2026-04-29-longsumeval.md) |

---

## 6. Domain-Specific (Medical, Legal, Finance, Science)

| Paper | Domain | Year | Key Claim | File |
| :--- | :---: | :---: | :--- | :--- |
| **SciCode** | Science | 2024 | Scientific coding; 4.6% Pass@1 (Claude 3.5) | [📄](./2024-07-18-scicode.md) |
| **LegalEval-Q** | Legal | 2025 | Legal text quality; 14B parameter plateau | [📄](./2025-05-30-legaleval-q.md) |
| **SurveyBench** | Science | 2025 | Literature review quality | [📄](./2025-10-03-surveybench.md) |
| **CritPt** | Physics | 2025 | Frontier physics; 30% (GPT-5.4 Pro) | [📄](./2025-09-30-critpt.md) |
| **Sci2Pol** | Policy | 2025 | Science-to-policy translation | [📄](./2025-09-25-sci2pol.md) |
| **PLawBench** | Legal | 2026 | Legal reasoning across 850 cases | [📄](./2026-01-23-plawbench.md) |
| **FrontierScience** | Science | 2026 | Expert science; 25.2% on research tasks | [📄](./2026-01-29-frontierscience.md) |
| **TaxPraBen** | Finance | 2026 | Professional tax practice QA | [📄](./2026-04-10-taxpraben.md) |
| **MMRareBench** | Medical | 2026 | Rare disease clinical reasoning | [📄](./2026-04-12-mmrarebench.md) |
| **CrashSight** | Transport | 2026 | Traffic crash; causal attribution near-chance | [📄](./2026-04-09-crashsight.md) |
| **MARINER** | Maritime | 2026 | Fine-grained vessel classification + VQA | [📄](./2026-04-09-mariner.md) |
| **HM-Bench** | Remote Sensing | 2026 | Hyperspectral remote sensing VLM | [📄](./2026-04-10-hm-bench.md) |
| **PRL-Bench** | Physics | 2026 | End-to-end physics research; <50/100 all models | [📄](./2026-04-16-prl-bench.md) |
| **TPS-CalcBench** | Engineering | 2026 | Hypersonic thermal engineering calculations | [📄](./2026-04-20-tps-calcbench.md) |
| **MedProbeBench** | Medical | 2026 | Medical guideline generation; evidence gap | [📄](./2026-04-20-medprobebench.md) |
| **IndiaFinBench** | Finance | 2026 | Indian financial regulatory reasoning | [📄](./2026-04-21-indiafinbench.md) |
| **SAHM** | Finance | 2026 | Arabic financial + Shari'ah reasoning | [📄](./2026-04-21-sahm.md) |
| **MedSkillAudit** | Medical | 2026 | Pre-deployment medical skill auditing | [📄](./2026-04-23-medskillaudit.md) |
| **ActuBench** | Finance | 2026 | Actuarial science; IAA syllabus | [📄](./2026-04-22-actubench.md) |
| **DPrivBench** | Security | 2026 | Differential privacy reasoning | [📄](./2026-04-17-dprivbench.md) |
| **X-PCR** | Medical | 2026 | Ophthalmic progressive clinical reasoning | [📄](./2026-04-23-x-pcr.md) |
| **SciEval** | Education | 2026 | K-12 science instructional evaluation | [📄](./2026-04-29-scieval.md) |
| **PSI-Bench** | Medical | 2026 | Patient simulator fidelity | [📄](./2026-04-29-psi-bench.md) |

---

## 7. Multilingual & Cross-Cultural

| Paper | Year | Key Claim | File |
| :--- | :---: | :--- | :--- |
| **Global MMLU** | 2024 | MMLU in 42 languages; rank shifts vs. English | [📄](./2024-12-04-global-mmlu.md) |
| **GaoYao Benchmark** | 2026 | 26 languages / 51 nations; Global South gaps | [📄](./2026-04-22-gaoyao-benchmark.md) |
| **IndicDB** | 2026 | Multilingual text-to-SQL; 7 Indic languages | [📄](./2026-04-15-indicdb.md) |
| **SAHM** | 2026 | Arabic financial reasoning; 19 LLMs | [📄](./2026-04-21-sahm.md) |
| **MM-JudgeBench** | 2026 | Cross-lingual LVLM judge; 25 languages | [📄](./2026-04-21-mm-judgebench.md) |
| **RespondeoQA** | 2026 | Latin-English bilingual QA | [📄](./2026-04-23-respondeoqa.md) |
| **CNSL-bench** | 2026 | Chinese sign language; 21 MLLMs | [📄](./2026-04-25-cnsl-bench.md) |

---

## 8. Speech & Audio

| Paper | Year | Key Claim | File |
| :--- | :---: | :--- | :--- |
| **HalluAudio** | 2026 | Audio-language hallucination; music/env. worst | [📄](./2026-04-21-halluaudio.md) |
| **SpeechParaling-Bench** | 2026 | Paralinguistic control; 43.3% of errors from misinterpretation | [📄](./2026-04-23-speechparaling-bench.md) |
| **AVID** | 2026 | Audio-visual inconsistency detection | [📄](./2026-04-15-avid.md) |
| **SOB (Audio)** | 2026 | Structured extraction from audio; 23.7% value accuracy | [📄](./2026-04-29-sob.md) |

---

## 9. Coding & Software Engineering

| Paper | Year | Key Claim | File |
| :--- | :---: | :--- | :--- |
| **ENAMEL** | 2024 | Code efficiency; eff@k metric | [📄](./2024-06-10-enamel.md) |
| **SciCode** | 2024 | Scientific coding; 4.6% Pass@1 | [📄](./2024-07-18-scicode.md) |
| **LiveCodeBench Pro** | 2025 | Competitive programming; 0% Hard | [📄](./2025-06-13-livecodebench-pro.md) |
| **SWE-bench Verified** | 2026 | Software engineering; 80.8% resolved | [📄](./2026-03-23-claude-4-6.md) |
| **CCR-Bench** | 2026 | Complex constraint reasoning; industrial | [📄](./2026-03-09-ccr-bench.md) |
| **QuanBench+** | 2026 | Quantum code generation | [📄](./2026-03-25-quanbench-plus.md) |
| **QuantCode-Bench** | 2026 | Algorithmic trading code | [📄](./2026-04-16-quantcode-bench.md) |
| **CodeSpecBench** | 2026 | Behavioural spec generation; 20.2% repo-level | [📄](./2026-04-14-codespecbench.md) |
| **StructEval** | 2025 | Structured output; 18 formats | [📄](./2025-12-08-structeval.md) |
| **HWE-Bench** | 2026 | Hardware bug repair; Verilog/SystemVerilog | [📄](./2026-04-16-hwe-bench.md) |
| **BLAST** | 2026 | ASP declarative code generation | [📄](./2026-04-25-blast.md) |
| **SOB** | 2026 | Structured data extraction across 3 modalities | [📄](./2026-04-29-sob.md) |

---

## 10. Frontier Model Reports

| Model | Lab | Year | Key Result | File |
| :--- | :--- | :---: | :--- | :--- |
| **GPT-5.4** | OpenAI | 2026 | 75.0% OSWorld-V | [📄](./2026-03-05-gpt-5-4-report.md) |
| **GPT-5.4 mini/nano** | OpenAI | 2026 | Efficiency leader | [📄](./2026-03-22-gpt-5-4-mini.md) |
| **Gemini 3.1 Pro** | Google | 2026 | 77.1% ARC-AGI-2 | [📄](./2026-02-19-gemini-3-1-pro.md) |
| **Claude Opus 4.6** | Anthropic | 2026 | 80.8% SWE-bench Verified | [📄](./2026-03-23-claude-4-6.md) |
| **Phi-4 Reasoning** | Microsoft | 2026 | Strong MathVista at 15B | [📄](./2026-03-15-phi-4-reasoning.md) |
| **DeepSeek-V3.2** | DeepSeek | 2026 | RL-based logic | [📄](./2026-03-24-deepseek-v3-2.md) |
| **ARC-AGI-2** | ARC Prize | 2026 | Non-semantic visual abduction | [📄](./2026-03-24-arc-agi-2.md) |
| **ERNIE 5.0** | Baidu | 2026 | Trillion-param MoE | [📄](./2026-02-07-ernie-5.md) |
| **Emu3.5** | BAAI | 2025 | 94.03 TIIF-Bench | [📄](./2025-10-30-emu3-5.md) |
| **Qwen3.5-Omni** | Alibaba | 2025 | 119 languages; WER 1.11 | [📄](./2025-09-22-qwen3-5-omni.md) |
| **DeepSeek-V3** | DeepSeek | 2025 | 75.1% MMLU-Pro | [📄](./2025-05-15-deepseek-v3.md) |
| **Llama 4 Scout** | Meta | 2026 | 10M context / 2,600 TPS | [📄](./2026-02-20-llama-4-scout.md) |

---

## 11. Meta-Evaluation & Methodology

| Paper | Year | Key Claim | File |
| :--- | :---: | :--- | :--- |
| **BenchHub** | 2025 | Unifies 839K Qs across 54 benchmarks | [📄](./2025-06-01-benchhub.md) |
| **BenchBench** | 2026 | Measures benchmark discriminability | [📄](./2026-03-21-benchbench.md) |
| **AISafetyBenchExplorer** | 2026 | 195 safety benchmarks; 70% stale repos | [📄](./2026-04-14-aisafetybenchexplorer.md) |
| **LiveBench 2026** | 2026 | Contamination-free monthly benchmark | [📄](./2026-01-20-livebench-v6.md) |
| **Rethinking Math Eval** | 2026 | Symbolic eval failures; LLM-as-judge better | [📄](./2026-04-25-rethinking-math-eval.md) |
| **LongSumEval** | 2026 | QA-based summarisation evaluation framework | [📄](./2026-04-29-longsumeval.md) |

---

*← Back to [README.md](../README.md) &nbsp;|&nbsp; 📚 [Benchmark Reference](../BENCHMARKS.md) &nbsp;|&nbsp; 📅 [Archive](../ARCHIVE.md)*
