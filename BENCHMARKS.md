# Benchmark Reference — LLM & VLM Evaluation

A curated, stable reference of 200+ benchmarks organised by capability domain.  
For the daily digest and new additions, see [README.md](./README.md) and [ARCHIVE.md](./ARCHIVE.md).  
For deep-dive notes on each paper, see [survey/INDEX.md](./survey/INDEX.md).

---

## Contents
- [LLM Benchmarks](#llm-benchmarks)
  - [Reasoning, Knowledge & Logic](#reasoning-knowledge--logic)
  - [Agentic, Coding & Security](#agentic-coding--security)
  - [Safety, Alignment & Robustness](#safety-alignment--robustness)
- [VLM Benchmarks](#vlm-benchmarks)
  - [Multimodal & Physical Reasoning](#multimodal--physical-reasoning)
  - [Document, Video & RAG](#document-video--rag)
  - [Domain-Specific Visual](#domain-specific-visual)
- [Meta-Evaluation & Methodology](#meta-evaluation--methodology)

---

## LLM Benchmarks

### Reasoning, Knowledge & Logic

| Benchmark | Task | Scale | Key Metric | Added | Notes | Link |
| :--- | :--- | :--- | :--- | :---: | :---: | :---: |
| **GPQA Diamond** | PhD-level science QA | 198 QA | Accuracy | 2023 | [📄](./survey/2023-11-20-gpqa-diamond.md) | [🔗](https://arxiv.org/abs/2311.12022) |
| **MMLU-Pro** | Multi-domain knowledge | 12,032 Qs / 14 disciplines | Accuracy | 2024 | [📄](./survey/2024-06-03-mmlu-pro.md) | [🔗](https://arxiv.org/abs/2406.01574) |
| **Global MMLU** | Multilingual knowledge | 601,734 instances / 42 languages | Accuracy / Bias | 2024 | [📄](./survey/2024-12-04-global-mmlu.md) | [🔗](https://arxiv.org/abs/2412.03304) |
| **RULER** | Long-context retrieval | 13 tasks / 4K–128K context | Avg Score | 2024 | [📄](./survey/2024-04-09-ruler.md) | [🔗](https://arxiv.org/abs/2404.06654) |
| **LongBench v2** | Long-context reasoning | 503 MCQ / 8K–2M words | Accuracy | 2024 | [📄](./survey/2024-12-19-longbench-v2.md) | [🔗](https://arxiv.org/abs/2412.15204) |
| **OMNI-MATH** | Olympiad mathematics | 4,428 problems / 33+ subdomains | Accuracy | 2024 | [📄](./survey/2024-10-10-omni-math.md) | [🔗](https://arxiv.org/abs/2410.07985) |
| **SimpleQA** | Open-domain factuality | 4,326 fact QA | F1 Score | 2024 | [📄](./survey/2024-11-01-simpleqa.md) | [🔗](https://arxiv.org/abs/2411.04368) |
| **MultiChallenge** | Multi-turn conversation | 273 conversations / 4 categories | Pass Rate | 2025 | [📄](./survey/2025-01-29-multichallenge.md) | [🔗](https://arxiv.org/abs/2501.17399) |
| **OmniScience** | Cross-domain science | Expert science QA | Accuracy | 2025 | [📄](./survey/2025-03-25-omniscience.md) | [🔗](https://arxiv.org/abs/2503.17604) |
| **OlymMATH** | Olympiad mathematics | 200 problems / EN+ZH | Pass@1 | 2025 | [📄](./survey/2025-03-27-olymmath.md) | [🔗](https://arxiv.org/abs/2503.21380) |
| **HalluLens** | Hallucination detection | Dynamic evaluation sets | Extrinsic + Intrinsic | 2025 | [📄](./survey/2025-04-24-hallulens.md) | [🔗](https://arxiv.org/abs/2504.17550) |
| **MathArena** | Competition mathematics | 162 problems / 7 competitions | Accuracy / Proof Score | 2025 | [📄](./survey/2025-05-29-matharena.md) | [🔗](https://arxiv.org/abs/2505.23281) |
| **DSR-Bench** | Structural reasoning | 4,140 instances | Structural Accuracy | 2025 | [📄](./survey/2025-05-29-dsr-bench.md) | [🔗](https://arxiv.org/abs/2505.24069) |
| **Reasoning Gym** | Reasoning / RLVR training | 100+ tasks / 11 domains | Zero-Shot Score | 2025 | [📄](./survey/2025-05-30-reasoning-gym.md) | [🔗](https://arxiv.org/abs/2505.24760) |
| **LegalEval-Q** | Legal text quality | 49 LLMs evaluated | Clarity / Coherence | 2025 | [📄](./survey/2025-05-30-legaleval-q.md) | [🔗](https://arxiv.org/abs/2505.24826) |
| **BenchHub** | Meta-evaluation | 839K Qs / 54 benchmarks | Customizable | 2025 | [📄](./survey/2025-06-01-benchhub.md) | [🔗](https://arxiv.org/abs/2506.00482) |
| **Thunder-NUBench** | Negation understanding | 1,261 MCQ items | Accuracy | 2025 | [📄](./survey/2025-06-17-thunder-nubench.md) | [🔗](https://arxiv.org/abs/2506.14397) |
| **IFBench** | Instruction following | 58 constraints / 300 prompts | IF Accuracy | 2025 | [📄](./survey/2025-07-03-ifbench.md) | [🔗](https://arxiv.org/abs/2507.02833) |
| **SurveyBench** | Literature review | 11.3K papers | Quality | 2025 | [📄](./survey/2025-10-03-surveybench.md) | [🔗](https://arxiv.org/abs/2510.03120) |
| **AcademicEval** | Academic writing | arXiv papers | Judge Score | 2025 | [📄](./survey/2025-10-20-academiceval.md) | [🔗](https://arxiv.org/abs/2510.17725) |
| **AA-Omniscience** | Cross-domain knowledge | 6,000 Qs / 42 subtopics | Omniscience Index | 2025 | [📄](./survey/2025-11-17-aa-omniscience.md) | [🔗](https://arxiv.org/abs/2511.13029) |
| **SDE Framework** | Scientific discovery | Bio / Chem / Phys | Project-level Accuracy | 2025 | [📄](./survey/2025-12-17-sde-framework.md) | [🔗](https://arxiv.org/abs/2512.15567) |
| **OfficeQA Pro** | Long-form document QA | 89K-page corpus / 26M+ values | Accuracy | 2026 | [📄](./survey/2026-03-09-officeqa-pro.md) | [🔗](https://arxiv.org/abs/2603.08655) |
| **BenchBench** | Meta-evaluation | 9 variants / 15K Qs | Discriminability | 2026 | [📄](./survey/2026-03-21-benchbench.md) | [🔗](https://arxiv.org/abs/2603.20807) |
| **LiveMathematicianBench** | Theorem proving (live) | Recent arXiv papers | Sub-Resistant Accuracy | 2026 | [📄](./survey/2026-04-02-livemathematicianbench.md) | [🔗](https://arxiv.org/abs/2604.01754) |
| **Riemann-Bench** | Research-level mathematics | 25 expert problems | Pass Rate (<10% all models) | 2026 | [📄](./survey/2026-04-08-riemann-bench.md) | [🔗](https://arxiv.org/abs/2604.06802) |
| **ImplicitMemBench** | Implicit memory | 300 items / 3 memory types | First-Attempt Accuracy | 2026 | [📄](./survey/2026-04-09-implicitmembench.md) | [🔗](https://arxiv.org/abs/2604.08064) |
| **TEMPER** | Emotional robustness | 5,400 neutral vs. emotional pairs | Accuracy Delta | 2026 | [📄](./survey/2026-04-09-temper.md) | [🔗](https://arxiv.org/abs/2604.07801) |
| **KDR-Bench** | Deep research | 41 expert Qs / 9 domains | Knowledge-Centric Score | 2026 | [📄](./survey/2026-04-09-kdr-bench.md) | [🔗](https://arxiv.org/abs/2604.07720) |
| **TaxPraBen** | Professional tax practice | 7,300 instances / 10 tasks | Exact Match | 2026 | [📄](./survey/2026-04-10-taxpraben.md) | [🔗](https://arxiv.org/abs/2604.08948) |
| **METER** | Causal reasoning | Pearl's 3-rung causal ladder | Accuracy per Rung | 2026 | [📄](./survey/2026-04-13-meter.md) | [🔗](https://arxiv.org/abs/2604.11502) |
| **General365** | K-12 general reasoning | 1,460 problems / 8 categories | Accuracy / Generalisation Gap | 2026 | [📄](./survey/2026-04-13-general365.md) | [🔗](https://arxiv.org/abs/2604.11778) |
| **REL** | Relational reasoning | Algebra + Chemistry + Biology | Accuracy by Arity | 2026 | [📄](./survey/2026-04-14-rel.md) | [🔗](https://arxiv.org/abs/2604.12176) |
| **PolicyBench** | Public policy comprehension | 21,000 cases / Bloom's taxonomy | Accuracy per Cognitive Level | 2026 | [📄](./survey/2026-04-14-policybench.md) | [🔗](https://arxiv.org/abs/2604.12995) |
| **AISafetyBenchExplorer** | Safety benchmark meta-catalogue | 195 safety benchmarks | Coverage / Maintenance Status | 2026 | [📄](./survey/2026-04-14-aisafetybenchexplorer.md) | [🔗](https://arxiv.org/abs/2604.12875) |
| **IndicDB** | Multilingual text-to-SQL | 15,617 tasks / 7 Indic languages | Execution Accuracy | 2026 | [📄](./survey/2026-04-15-indicdb.md) | [🔗](https://arxiv.org/abs/2604.13686) |
| **QuantSightBench** | Quantitative forecasting | 11 models / multi-domain | Empirical Coverage Rate | 2026 | [📄](./survey/2026-04-17-quantsightbench.md) | [🔗](https://arxiv.org/abs/2604.15859) |
| **KWBench** | Unprompted problem recognition | 223 tasks / 16 LLMs | Recognition Accuracy | 2026 | [📄](./survey/2026-04-17-kwbench.md) | [🔗](https://arxiv.org/abs/2604.15760) |
| **DPrivBench** | Differential privacy reasoning | Textbook → advanced DP | Verification Accuracy | 2026 | [📄](./survey/2026-04-17-dprivbench.md) | [🔗](https://arxiv.org/abs/2604.15851) |
| **PRL-Bench** | Physics research workflows | 100 PRL papers / 5 subfields | End-to-End Research Score | 2026 | [📄](./survey/2026-04-16-prl-bench.md) | [🔗](https://arxiv.org/abs/2604.15411) |
| **KnowledgeBerg** | Knowledge width & depth | 4,800 MCQ / 17 languages | Enumeration F1 | 2026 | [📄](./survey/2026-04-19-knowledgeberg.md) | [🔗](https://arxiv.org/abs/2604.17621) |
| **TPS-CalcBench** | Engineering calculations | 420 core items / 13 models | KPI Score | 2026 | [📄](./survey/2026-04-20-tps-calcbench.md) | [🔗](https://arxiv.org/abs/2604.17966) |
| **MedProbeBench** | Medical guideline generation | 1,200+ rubric criteria / 17 LLMs | Evidence Integration Score | 2026 | [📄](./survey/2026-04-20-medprobebench.md) | [🔗](https://arxiv.org/abs/2604.18418) |
| **IndiaFinBench** | Indian financial reasoning | 406 QA pairs / 12 LLMs | Task Accuracy | 2026 | [📄](./survey/2026-04-21-indiafinbench.md) | [🔗](https://arxiv.org/abs/2604.19298) |
| **SAHM** | Arabic financial / Shari'ah reasoning | 14,380 instances / 19 LLMs | Accuracy per Task | 2026 | [📄](./survey/2026-04-21-sahm.md) | [🔗](https://arxiv.org/abs/2604.19098) |
| **GaoYao Benchmark** | Multilingual reasoning | 182,300 samples / 26 languages | Cross-National Performance Gap | 2026 | [📄](./survey/2026-04-22-gaoyao-benchmark.md) | [🔗](https://arxiv.org/abs/2604.20225) |
| **ActuBench** | Actuarial science | 200 items / 50 LLMs | MCQ + Open-Ended Rubric | 2026 | [📄](./survey/2026-04-22-actubench.md) | [🔗](https://arxiv.org/abs/2604.20273) |
| **DialToM** | Theory of Mind | 41,601 MCQs / 13 LLMs | Literal vs. Functional ToM | 2026 | [📄](./survey/2026-04-22-dialtom.md) | [🔗](https://arxiv.org/abs/2604.20443) |
| **MIRROR** | Metacognitive calibration | 16 models / ~250K instances | Compositional Calibration Error | 2026 | [📄](./survey/2026-04-23-mirror.md) | [🔗](https://arxiv.org/abs/2604.19809) |
| **RespondeoQA** | Bilingual Latin-English QA | ~7,800 QA pairs | Skill-Oriented Task Accuracy | 2026 | [📄](./survey/2026-04-23-respondeoqa.md) | [🔗](https://arxiv.org/abs/2604.20738) |
| **CLARITY** | NL2SQL under ambiguity | Spider + BIRD / multi-turn | NL2SQL Accuracy Under Ambiguity | 2026 | [📄](./survey/2026-04-25-clarity.md) | [🔗](https://arxiv.org/abs/2604.22313) |
| **MuDABench** | Multi-document analytical QA | 332 instances / 80,000+ pages | Final Answer Accuracy | 2026 | [📄](./survey/2026-04-25-mudabench.md) | [🔗](https://arxiv.org/abs/2604.22239) |
| **AgentSearchBench** | AI agent discovery | ~10,000 real-world agents | Retrieval Ranking Accuracy | 2026 | [📄](./survey/2026-04-25-agentsearchbench.md) | [🔗](https://arxiv.org/abs/2604.22436) |
| **BLAST** | ASP code generation | 10 problems / 8 LLMs | Semantic Correctness | 2026 | [📄](./survey/2026-04-25-blast.md) | [🔗](https://arxiv.org/abs/2604.22306) |
| **Rethinking Math Eval** | Math evaluation methodology | Lighteval + SimpleRL failures | LLM-Judge Consistency | 2026 | [📄](./survey/2026-04-25-rethinking-math-eval.md) | [🔗](https://arxiv.org/abs/2604.22597) |
| **AutoResearchBench** | Scientific literature discovery | Deep + Wide research tasks | Discovery Accuracy (~9%) | 2026 | [📄](./survey/2026-04-29-autoresearchbench.md) | [🔗](https://arxiv.org/abs/2604.25256) |
| **PSI-Bench** | Patient simulation fidelity | 7 LLMs / 3 diagnostic levels | Behavioural Diversity | 2026 | [📄](./survey/2026-04-29-psi-bench.md) | [🔗](https://arxiv.org/abs/2604.25840) |
| **SOB** | Structured output quality | 21 models / text+image+audio | Value Accuracy | 2026 | [📄](./survey/2026-04-29-sob.md) | [🔗](https://arxiv.org/abs/2604.25359) |
| **SciEval** | K-12 science instructional eval | 273 lessons / 13 criteria | Rubric Evaluation Accuracy | 2026 | [📄](./survey/2026-04-29-scieval.md) | [🔗](https://arxiv.org/abs/2604.25472) |
| **Semantic Layers Bench** | Text-to-SQL with semantics | 100 NL Qs / 3 frontier models | SQL Accuracy (+17–23 pp) | 2026 | [📄](./survey/2026-04-29-semantic-layers-bench.md) | [🔗](https://arxiv.org/abs/2604.25149) |
| **LongSumEval** | Long-document summarisation | 7 benchmarks / QA-based eval | Human Judgment Correlation | 2026 | [📄](./survey/2026-04-29-longsumeval.md) | [🔗](https://arxiv.org/abs/2604.25130) |

---

### Agentic, Coding & Security

| Benchmark | Task | Scale | Key Metric | Added | Notes | Link |
| :--- | :--- | :--- | :--- | :---: | :---: | :---: |
| **AgentBench** | General agent | 8 environments | Task Success % | 2023 | [📄](./survey/2023-08-07-agentbench.md) | [🔗](https://arxiv.org/abs/2308.03688) |
| **WebArena** | Web agent | 812 tasks / 5 websites | Task Success % | 2023 | [📄](./survey/2023-07-25-webarena.md) | [🔗](https://arxiv.org/abs/2307.13854) |
| **SciCode** | Scientific coding | 338 subproblems / 5 domains | Pass@1 | 2024 | [📄](./survey/2024-07-18-scicode.md) | [🔗](https://arxiv.org/abs/2407.13168) |
| **OfficeBench** | Office automation | 300 tasks / 9 apps | Task Success % | 2024 | [📄](./survey/2024-07-26-officebench.md) | [🔗](https://arxiv.org/abs/2407.19056) |
| **ENAMEL** | Code efficiency | 30 LLMs | eff@k | 2024 | [📄](./survey/2024-06-10-enamel.md) | [🔗](https://arxiv.org/abs/2406.06647) |
| **PaperBench** | AI research replication | 20 ICML 2024 papers | Replication Score | 2025 | [📄](./survey/2025-04-02-paperbench.md) | [🔗](https://arxiv.org/abs/2504.01848) |
| **MultiAgentBench** | Multi-agent collaboration | 6 scenarios / 400+ cases | Task + Coordination Score | 2025 | [📄](./survey/2025-03-03-multiagentbench.md) | [🔗](https://arxiv.org/abs/2503.01935) |
| **LiveCodeBench Pro** | Competitive programming | Codeforces / ICPC / IOI | Pass@1 | 2025 | [📄](./survey/2025-06-13-livecodebench-pro.md) | [🔗](https://arxiv.org/abs/2506.11928) |
| **ToolBench** | Tool use | 16,459 APIs | Pass Rate | 2025 | [📄](./survey/2025-01-15-toolbench.md) | [🔗](https://arxiv.org/abs/2307.16789) |
| **MemBench** | Agent memory | 53K questions | Accuracy / Recall | 2025 | [📄](./survey/2025-06-20-membench.md) | [🔗](https://arxiv.org/abs/2506.21605) |
| **GDPval** | Real-world economic tasks | 1,320 tasks / 44 occupations | Expert Win Rate | 2025 | [📄](./survey/2025-10-05-gdpval.md) | [🔗](https://arxiv.org/abs/2510.04374) |
| **PaperArena** | Scientific literature agent | 784 QA pairs | Accuracy | 2025 | [📄](./survey/2025-10-13-paperarena.md) | [🔗](https://arxiv.org/abs/2510.10909) |
| **SKA-Bench** | Structured knowledge | 921 QA × 4 tests | Accuracy | 2025 | [📄](./survey/2025-07-23-ska-bench.md) | [🔗](https://arxiv.org/abs/2507.17178) |
| **PentestEval** | Cybersecurity pentesting | 346 pentest tasks | E2E Success % | 2025 | [📄](./survey/2025-12-15-pentesteval.md) | [🔗](https://arxiv.org/abs/2512.14233) |
| **StructEval** | Structured output generation | 18 formats (JSON/YAML/HTML…) | Schema Fidelity | 2025 | [📄](./survey/2025-12-08-structeval.md) | — |
| **SWE-bench Verified** | Software engineering | 500 issues | Resolved % | 2026 | [📄](./survey/2026-03-23-claude-4-6.md) | [🔗](https://www.swebench.com/) |
| **Terminal-Bench** | CLI / terminal agents | 89 tasks / 10 categories | Pass Rate | 2026 | [📄](./survey/2026-01-17-terminal-bench.md) | [🔗](https://arxiv.org/abs/2601.11868) |
| **RepoReason** | Code repository reasoning | 2,492 tasks | ESV / MCL / DFI | 2026 | [📄](./survey/2026-01-07-reporeason.md) | [🔗](https://arxiv.org/abs/2601.03731) |
| **CCR-Bench** | Complex constraint reasoning | 174 industrial samples | Pass Rate | 2026 | [📄](./survey/2026-03-09-ccr-bench.md) | [🔗](https://arxiv.org/abs/2603.07886) |
| **VSAS-Bench** | Streaming video VLM | 18,000+ annotations | Accuracy-Latency Tradeoff | 2026 | [📄](./survey/2026-04-08-vsas-bench.md) | [🔗](https://arxiv.org/abs/2604.07634) |
| **TraceSafe-Bench** | Mid-trajectory tool safety | 1,000+ multi-step instances | Guardrail Efficacy | 2026 | [📄](./survey/2026-04-08-tracesafe-bench.md) | [🔗](https://arxiv.org/abs/2604.07223) |
| **KnowU-Bench** | Personalised mobile GUI agent | 192 tasks / 3 tracks | Track Success Rate | 2026 | [📄](./survey/2026-04-09-knowu-bench.md) | [🔗](https://arxiv.org/abs/2604.08455) |
| **QuanBench+** | Quantum code generation | 42 tasks / 3 frameworks | Pass@1 | 2026 | [📄](./survey/2026-03-25-quanbench-plus.md) | [🔗](https://arxiv.org/abs/2604.08570) |
| **PilotBench** | Aviation agent safety | 708 real trajectories | Pilot Score | 2026 | [📄](./survey/2026-04-10-pilotbench.md) | [🔗](https://arxiv.org/abs/2604.08987) |
| **SAGE** | Customer service agent | 6 scenarios / 27 LLMs | Path Coverage | 2026 | [📄](./survey/2026-04-10-sage.md) | [🔗](https://arxiv.org/abs/2604.09285) |
| **BankerToolBench** | Investment banking agent | E2E workflows / 502 validators | Rubric Pass Rate | 2026 | [📄](./survey/2026-04-13-bankertoolbench.md) | [🔗](https://arxiv.org/abs/2604.11304) |
| **AnalysisBench** | Software analysis agent | 35 tool-project pairs | Task Success Rate | 2026 | [📄](./survey/2026-04-13-analysisbench.md) | [🔗](https://arxiv.org/abs/2604.13270) |
| **OccuBench** | Professional occupational agent | 100 scenarios / 10 industries | Task Completion Rate | 2026 | [📄](./survey/2026-04-13-occubench.md) | [🔗](https://arxiv.org/abs/2604.10866) |
| **HORIZON** | Long-horizon agent diagnostics | 3,100+ trajectories | Failure Type Distribution | 2026 | [📄](./survey/2026-04-13-horizon.md) | [🔗](https://arxiv.org/abs/2604.11978) |
| **SIR-Bench** | Security incident response | 794 test cases | TPR / FPR Rejection | 2026 | [📄](./survey/2026-04-13-sir-bench.md) | [🔗](https://arxiv.org/abs/2604.12040) |
| **AAR** | DAG-structured tool navigation | 1,400 instances | Finish-Line Accuracy | 2026 | [📄](./survey/2026-04-11-aar.md) | [🔗](https://arxiv.org/abs/2604.10261) |
| **AlphaEval** | Production agent (enterprise) | 94 tasks / 7 companies | Task Success per Domain | 2026 | [📄](./survey/2026-04-14-alphaeval.md) | [🔗](https://arxiv.org/abs/2604.12162) |
| **Frontier-Eng** | Self-evolving engineering agent | 47 tasks / industrial simulators | Normalised Reward | 2026 | [📄](./survey/2026-04-14-frontier-eng.md) | [🔗](https://arxiv.org/abs/2604.12290) |
| **CodeSpecBench** | Behavioral spec generation | Real-world OSS Python | Pass Rate (Spec Execution) | 2026 | [📄](./survey/2026-04-14-codespecbench.md) | [🔗](https://arxiv.org/abs/2604.12268) |
| **CodeRQ-Bench** | Code reasoning quality | 1,069 mismatch cases / 3 tasks | AUC-ROC | 2026 | [📄](./survey/2026-04-14-coderq-bench.md) | [🔗](https://arxiv.org/abs/2604.12379) |
| **HINTBench** | Intrinsic agent safety | 629 trajectories / 5-constraint taxonomy | Strict-F1 (Step Localisation) | 2026 | [📄](./survey/2026-04-15-hintbench.md) | [🔗](https://arxiv.org/abs/2604.13954) |
| **GeoAgentBench** | GIS / spatial analysis agent | 117 tools / 53 tasks | Parameter Execution Accuracy | 2026 | [📄](./survey/2026-04-15-geoagentbench.md) | [🔗](https://arxiv.org/abs/2604.13888) |
| **RiskWebWorld** | GUI agent — e-commerce risk | 1,513 tasks / 8 risk domains | Task Success Rate | 2026 | [📄](./survey/2026-04-15-riskwebworld.md) | [🔗](https://arxiv.org/abs/2604.13531) |
| **FedGUI** | Federated GUI agent | 6 datasets / 4 heterogeneity types | Federated Accuracy | 2026 | [📄](./survey/2026-04-16-fedgui.md) | [🔗](https://arxiv.org/abs/2604.14956) |
| **HWE-Bench** | Hardware bug repair agent | 417 bug-fix PRs / 7 LLMs | Task Resolution Rate | 2026 | [📄](./survey/2026-04-16-hwe-bench.md) | [🔗](https://arxiv.org/abs/2604.14709) |
| **DR³-Eval** | Deep research agent | Multi-document / distractor noise | Information Recall | 2026 | [📄](./survey/2026-04-16-dr3-eval.md) | [🔗](https://arxiv.org/abs/2604.14683) |
| **QuantCode-Bench** | Algorithmic trading code | 400 tasks / multi-turn | Semantic Alignment | 2026 | [📄](./survey/2026-04-16-quantcode-bench.md) | [🔗](https://arxiv.org/abs/2604.15151) |
| **HarmfulSkillBench** | Harmful skills in agent ecosystems | 200 harmful skills / 6 LLMs | Harm Score Delta | 2026 | [📄](./survey/2026-04-16-harmfulskillbench.md) | [🔗](https://arxiv.org/abs/2604.15415) |
| **GTA-2** | General tool agent | Atomic + long-horizon workflows | Workflow Completion % | 2026 | [📄](./survey/2026-04-17-gta-2.md) | [🔗](https://arxiv.org/abs/2604.15715) |
| **MemEvoBench** | Memory safety degradation | 7 domains / 36 risk categories | Safety Degradation Rate | 2026 | [📄](./survey/2026-04-17-memevobench.md) | [🔗](https://arxiv.org/abs/2604.15774) |
| **Terminal Wrench** | Reward hacking — terminal agents | 331 environments / 3 models | Monitor AUC | 2026 | [📄](./survey/2026-04-19-terminal-wrench.md) | [🔗](https://arxiv.org/abs/2604.17596) |
| **TeleEmbedBench** | Telecom RAG embedding | 9,000 Q-chunk pairs / 3 corpora | Retrieval Accuracy | 2026 | [📄](./survey/2026-04-20-teleembedbench.md) | [🔗](https://arxiv.org/abs/2604.17778) |
| **AJ-Bench** | Agent-as-a-judge | 155 tasks / 3 domains | Verification Accuracy | 2026 | [📄](./survey/2026-04-20-aj-bench.md) | [🔗](https://arxiv.org/abs/2604.18240) |
| **WebCompass** | Multimodal web coding | 15 domains / 3 modalities | Execution Pass Rate | 2026 | [📄](./survey/2026-04-20-webcompass.md) | [🔗](https://arxiv.org/abs/2604.18224) |
| **AutomationBench** | Cross-app enterprise workflows | Zapier-based / 6 domains | End-State Verification | 2026 | [📄](./survey/2026-04-21-automationbench.md) | [🔗](https://arxiv.org/abs/2604.18934) |
| **Cyber Defense Benchmark** | Agentic threat hunting | 26 campaigns / 5 frontier models | Malicious Event Recall (3.8%) | 2026 | [📄](./survey/2026-04-21-cyber-defense-benchmark.md) | [🔗](https://arxiv.org/abs/2604.19533) |
| **DeepRed** | CTF security agents | 10 VM challenges / 10 LLMs | Checkpoint Completion % | 2026 | [📄](./survey/2026-04-21-deepred.md) | [🔗](https://arxiv.org/abs/2604.19354) |
| **PlayEval** | GUI code playability | 43 apps / 10 code LLMs | Play@k | 2026 | [📄](./survey/2026-04-21-playeval.md) | [🔗](https://arxiv.org/abs/2604.19742) |
| **Memora** | Long-term agent memory | Weeks-to-months conversations | FAMA | 2026 | [📄](./survey/2026-04-21-memora.md) | [🔗](https://arxiv.org/abs/2604.20006) |
| **SkillLearnBench** | Continual skill learning | 20 tasks / 15 sub-domains | Skill Quality | 2026 | [📄](./survey/2026-04-21-skilllearnbench.md) | [🔗](https://arxiv.org/abs/2604.20087) |
| **CyberCertBench** | Cybersecurity certification | IT + OT + IEC 62443 | MCQA Accuracy | 2026 | [📄](./survey/2026-04-22-cybercertbench.md) | [🔗](https://arxiv.org/abs/2604.20389) |
| **MedSkillAudit** | Medical agent skill auditing | 75 skills / 5 categories | Pre-Release Gate Pass Rate | 2026 | [📄](./survey/2026-04-23-medskillaudit.md) | [🔗](https://arxiv.org/abs/2604.20441) |
| **DV-World** | Data visualization agents | 260 tasks / 3 workflow types | Task Success (<50% SOTA) | 2026 | [📄](./survey/2026-04-29-dv-world.md) | [🔗](https://arxiv.org/abs/2604.25914) |

---

### Safety, Alignment & Robustness

| Benchmark | Task | Scale | Key Metric | Added | Notes | Link |
| :--- | :--- | :--- | :--- | :---: | :---: | :---: |
| **LiveBench 2026** | Contamination-free eval | Monthly update | Avg Score | 2026 | [📄](./survey/2026-01-20-livebench-v6.md) | [🔗](https://livebench.ai/) |
| **SteerEval** | Behavioral steering | 5,000+ steering prompts | Control % | 2026 | [📄](./survey/2026-03-03-steereval.md) | — |
| **NC-Bench** | Narrative consistency | IBM patterns | Pattern Accuracy | 2026 | [📄](./survey/2026-01-06-nc-bench.md) | [🔗](https://arxiv.org/abs/2601.06426) |
| **PLawBench** | Legal reasoning | 850 cases | Rubric Score | 2026 | [📄](./survey/2026-01-23-plawbench.md) | [🔗](https://arxiv.org/abs/2601.16669) |
| **LPFQA** | Technical forum QA | 430 tasks | Reasoning | 2026 | [📄](./survey/2026-01-08-lpfqa.md) | [🔗](https://arxiv.org/abs/2511.06346) |

---

## VLM Benchmarks

### Multimodal & Physical Reasoning

| Benchmark | Task | Scale | Key Metric | Added | Notes | Link |
| :--- | :--- | :--- | :--- | :---: | :---: | :---: |
| **MathVista** | Visual mathematics | 6,141 examples | Accuracy | 2023 | [📄](./survey/2023-10-03-mathvista.md) | [🔗](https://arxiv.org/abs/2310.02255) |
| **OlympiadBench** | Bilingual multimodal science | 8,476 problems | Accuracy | 2024 | [📄](./survey/2024-02-21-olympiadbench.md) | [🔗](https://arxiv.org/abs/2402.14008) |
| **MATHVERSE** | Visual math diagrams | 2,612 problems / 15K samples | CoT Step Accuracy | 2024 | [📄](./survey/2024-03-22-mathverse.md) | [🔗](https://arxiv.org/abs/2403.14624) |
| **MMT-Bench** | Multitask visual understanding | 31,325 Qs / 162 subtasks | Accuracy | 2024 | [📄](./survey/2024-04-24-mmt-bench.md) | [🔗](https://arxiv.org/abs/2404.16006) |
| **VL-RewardBench** | VLM reward models | 1,250 preference examples | Judgment Accuracy | 2024 | [📄](./survey/2024-11-26-vl-rewardbench.md) | [🔗](https://arxiv.org/abs/2411.17451) |
| **DynaMath** | Visual math robustness | 5,010 variants / 9 topics | Worst-Case Accuracy | 2024 | [📄](./survey/2024-10-29-dynamath.md) | [🔗](https://arxiv.org/abs/2411.00836) |
| **VisionArena** | VLM preference evaluation | 230K convos / 500 prompts | Preference Accuracy | 2024 | [📄](./survey/2024-12-11-visionarena.md) | [🔗](https://arxiv.org/abs/2412.08687) |
| **PhysBench** | Physical world understanding | 10K entries | Dynamics Accuracy | 2025 | [📄](./survey/2025-02-28-physbench.md) | [🔗](https://github.com/USC-GVL/PhysBench) |
| **VLM2-Bench** | Visual cue linking | 3,060 QA / 9 subtasks | Accuracy | 2025 | [📄](./survey/2025-02-17-vlm2-bench.md) | [🔗](https://arxiv.org/abs/2502.12084) |
| **R1-Onevision** | Visual math reasoning | 155K samples | Math Reasoning Accuracy | 2025 | [📄](./survey/2025-03-13-r1-onevision.md) | [🔗](https://arxiv.org/abs/2503.10615) |
| **VisNumBench** | Number sense | ~1,900 MCQ / 7 attributes | Accuracy | 2025 | [📄](./survey/2025-03-19-visnumbench.md) | [🔗](https://arxiv.org/abs/2503.14939) |
| **XLRS-Bench** | Remote sensing QA | 45,942 annotations | VQA / Grounding Accuracy | 2025 | [📄](./survey/2025-03-30-xlrs-bench.md) | [🔗](https://arxiv.org/abs/2503.23771) |
| **EMMA** | Cross-modal reasoning | 2,788 problems / 4 domains | Accuracy | 2025 | [📄](./survey/2025-01-09-emma.md) | [🔗](https://arxiv.org/abs/2501.05444) |
| **HLE** | Expert-level multimodal | 2.5K expert Qs / ~10% multimodal | Accuracy | 2025 | [📄](./survey/2025-01-20-hle-survey.md) | [🔗](https://lastexam.ai/) |
| **VCBench** | Multi-image mathematics | 1,720 problems | Accuracy (<50%) | 2025 | [📄](./survey/2025-04-24-vcbench.md) | [🔗](https://arxiv.org/abs/2504.18589) |
| **Uni-MMMU** | Unified gen + understanding | 8 bidirectional tasks | Task Accuracy | 2025 | [📄](./survey/2025-10-17-uni-mmmu.md) | [🔗](https://arxiv.org/abs/2510.13759) |
| **MMFineReason** | Fine-grained reasoning | 1.8M samples / 5.1B tokens | Reasoning Accuracy | 2026 | [📄](./survey/2026-01-29-mmfinereason.md) | [🔗](https://arxiv.org/abs/2601.21821) |
| **MMMU-Pro** | Expert multimodal QA | 11.5K expert questions | Accuracy | 2026 | [📄](./survey/2026-03-20-mmmu-pro-survey.md) | [🔗](https://mmmu-benchmark.github.io/) |
| **MathVision** | Visual math | 3K problems | Accuracy | 2026 | [📄](./survey/2026-01-14-step3-vl.md) | [🔗](https://arxiv.org/abs/2402.14804) |
| **VLM-RobustBench** | Robustness | 49 augmentation types | Robustness Gap | 2026 | [📄](./survey/2026-03-06-vlm-robustbench.md) | [🔗](https://arxiv.org/abs/2603.06148) |
| **DISSECT** | Scientific VLM diagnosis | 12,000 Qs / Chem + Bio | Perception / Integration Score | 2026 | [📄](./survey/2026-04-06-dissect.md) | [🔗](https://arxiv.org/abs/2604.06250) |
| **BareBones** | Geometric shape comprehension | 26 VLMs / 6 datasets | Texture Bias Cliff | 2026 | [📄](./survey/2026-04-12-barebones.md) | [🔗](https://arxiv.org/abs/2604.10528) |
| **MMRareBench** | Rare disease multimodal | 1,756 QA / 7,958 images | Two-Level Accuracy | 2026 | [📄](./survey/2026-04-12-mmrarebench.md) | [🔗](https://arxiv.org/abs/2604.10755) |
| **EgoEsportsQA** | Egocentric video reasoning | 1,745 QA / 3 FPS games | Task Accuracy | 2026 | [📄](./survey/2026-04-14-egoesportsqa.md) | [🔗](https://arxiv.org/abs/2604.12320) |
| **DailyClue** | Visual clue-driven reasoning | 4 domains / 16 subtasks | Clue ID Accuracy | 2026 | [📄](./survey/2026-04-15-dailyclue.md) | [🔗](https://arxiv.org/abs/2604.14041) |
| **MirrorBench** | MLLM self-recognition | Tiered self-representation tasks | Self-Recognition Rate | 2026 | [📄](./survey/2026-04-16-mirrorbench.md) | [🔗](https://arxiv.org/abs/2604.14785) |
| **CrossMath** | VLM modality gap | Same math in 3 formats | Modality Gap | 2026 | [📄](./survey/2026-04-17-crossmath.md) | [🔗](https://arxiv.org/abs/2604.16256) |
| **VisualTextTrap** | Text overlay hallucination | 6,057 samples / 5-level intensity | Hallucination Rate | 2026 | [📄](./survey/2026-04-19-visualtexttrap.md) | [🔗](https://arxiv.org/abs/2604.17375) |
| **HalluAudio** | Audio-language hallucination | 5,000+ QA pairs / 4 task types | Hallucination Rate | 2026 | [📄](./survey/2026-04-21-halluaudio.md) | [🔗](https://arxiv.org/abs/2604.19300) |
| **MM-JudgeBench** | Multilingual LVLM judge | 60,000+ instances / 25 languages | Cross-Lingual Consistency | 2026 | [📄](./survey/2026-04-21-mm-judgebench.md) | [🔗](https://arxiv.org/abs/2604.19405) |
| **FAS-VFM Bench** | Face anti-spoofing VFMs | 15 models / 4 datasets | HTER / AUC | 2026 | [📄](./survey/2026-04-21-fas-vfm-bench.md) | [🔗](https://arxiv.org/abs/2604.19196) |
| **SpeechParaling-Bench** | Paralinguistic speech generation | 1,000+ queries / 100+ features | Control Accuracy | 2026 | [📄](./survey/2026-04-23-speechparaling-bench.md) | [🔗](https://arxiv.org/abs/2604.20842) |
| **X-PCR** | Ophthalmic clinical reasoning | 177,868 QA / 52 diseases / 21 MLLMs | Progressive Accuracy per Stage | 2026 | [📄](./survey/2026-04-23-x-pcr.md) | [🔗](https://arxiv.org/abs/2604.20350) |
| **OMIBench** | Olympiad multi-image reasoning | Olympiad-level multi-image | Reasoning Accuracy | 2026 | [📄](./survey/2026-04-22-omibench.md) | [🔗](https://arxiv.org/abs/2604.20806) |
| **WildFireVQA** | Wildfire monitoring (RGB+Thermal) | 6,097 image pairs / 207,298 MCQs | Task Accuracy | 2026 | [📄](./survey/2026-04-22-wildfirevqa.md) | [🔗](https://arxiv.org/abs/2604.20190) |
| **CNSL-bench** | Sign language MLLMs | Official CNSL dict / 21 MLLMs | Comprehension Accuracy | 2026 | [📄](./survey/2026-04-25-cnsl-bench.md) | [🔗](https://arxiv.org/abs/2604.22367) |
| **SpaMEM** | Embodied spatial reasoning | 10.6M images / 25,000+ sequences | Spatial Belief Coherence | 2026 | [📄](./survey/2026-04-25-spamem.md) | [🔗](https://arxiv.org/abs/2604.22409) |
| **LTD / UniVLT** | Multi-view traffic VQA | 11,600 VQA pairs / roadside cameras | Open-Ended Reasoning Accuracy | 2026 | [📄](./survey/2026-04-25-ltd-univlt.md) | [🔗](https://arxiv.org/abs/2604.22260) |
| **DRAGON** | Evidence-grounded diagram QA | 11,664 instances / 8 VLMs | Grounding Accuracy | 2026 | [📄](./survey/2026-04-29-dragon.md) | [🔗](https://arxiv.org/abs/2604.25231) |

---

### Document, Video & RAG

| Benchmark | Task | Scale | Key Metric | Added | Notes | Link |
| :--- | :--- | :--- | :--- | :---: | :---: | :---: |
| **VLR-Bench** | Vision-RAG | 300 RAG VQA | RAG Accuracy | 2024 | [📄](./survey/2024-12-10-vlr-bench.md) | [🔗](https://arxiv.org/abs/2412.10151) |
| **TemporalBench** | Video temporal reasoning | 10K QA | Binary Accuracy | 2026 | [📄](./survey/2026-01-10-temporalbench.md) | [🔗](https://neurips.cc/virtual/2024/103554) |
| **MotionBench** | Video motion understanding | 5,000 videos | Motion QA Accuracy | 2025 | [📄](./survey/2025-01-06-motionbench.md) | [🔗](https://arxiv.org/abs/2501.02955) |
| **olmOCR** | Document parsing | 1.4M PDFs | Pass % | 2025 | [📄](./survey/2025-10-05-olmocr-survey.md) | [🔗](https://olmocr.allenai.org/) |
| **ROVER** | Embodied video reasoning | 543 videos / 27 tasks | VQA / Progress Accuracy | 2025 | [📄](./survey/2025-08-04-rover.md) | [🔗](https://arxiv.org/abs/2508.01943) |
| **FineVision** | Multimodal training data | 24M samples / 185 subsets | Avg Score (11 benchmarks) | 2025 | [📄](./survey/2025-10-22-finevision.md) | [🔗](https://arxiv.org/abs/2510.17269) |
| **MM-IFEngine** | Multimodal instruction following | 23K SFT/DPO | Constraint % | 2025 | [📄](./survey/2025-04-10-mm-ifengine.md) | [🔗](https://github.com/SYuan03/MM-IFEngine) |
| **VideoLLM Survey** | Meta-survey | Comprehensive review | Review | 2025 | [📄](./survey/2025-05-03-videollm-survey.md) | [🔗](https://arxiv.org/abs/2505.03829) |
| **OmniDocBench** | Enterprise document parsing | 1,355 images | OCR Accuracy | 2026 | [📄](./survey/2026-03-04-omnidocbench.md) | [🔗](https://arxiv.org/abs/2601.21957) |
| **ParseBench** | Enterprise document parsing | ~2,000 pages / 5 dimensions | Semantic Correctness | 2026 | [📄](./survey/2026-04-09-parsebench.md) | [🔗](https://arxiv.org/abs/2604.08538) |
| **AVID** | Audio-visual inconsistency | 11,200 videos / 39,400 events | BLEU-4 / mIoU | 2026 | [📄](./survey/2026-04-15-avid.md) | [🔗](https://arxiv.org/abs/2604.13593) |
| **MCSC-Bench** | Video production scripting | 11,000+ annotated videos | Script Quality | 2026 | [📄](./survey/2026-04-16-mcsc-bench.md) | [🔗](https://arxiv.org/abs/2604.15127) |
| **CCTVBench** | Traffic video QA consistency | Paired real + counterfactual videos | Quadruple-Level Consistency | 2026 | [📄](./survey/2026-04-22-cctvbench.md) | [🔗](https://arxiv.org/abs/2604.20460) |

---

### Domain-Specific Visual

| Benchmark | Task | Scale | Key Metric | Added | Notes | Link |
| :--- | :--- | :--- | :--- | :---: | :---: | :---: |
| **MARINER** | Maritime fine-grained VLM | 16,629 images / 63 vessel categories | Classification + VQA Accuracy | 2026 | [📄](./survey/2026-04-09-mariner.md) | [🔗](https://arxiv.org/abs/2604.08615) |
| **CrashSight** | Traffic crash video understanding | 250 videos / 13,000 MCQ | Tier 1 + Tier 2 Accuracy | 2026 | [📄](./survey/2026-04-09-crashsight.md) | [🔗](https://arxiv.org/abs/2604.08457) |
| **HM-Bench** | Hyperspectral remote sensing | 19,337 QA / 13 task categories | Task Accuracy | 2026 | [📄](./survey/2026-04-10-hm-bench.md) | [🔗](https://arxiv.org/abs/2604.08884) |
| **ADAPT** | Embodied planning under affordances | DynAfford / household planning | Task Success Rate | 2026 | [📄](./survey/2026-04-16-adapt-dynafford.md) | [🔗](https://arxiv.org/abs/2604.14902) |
| **RSRCC** | Remote sensing change comprehension | 126,000 QA / bi-temporal satellite | Change Description Accuracy | 2026 | [📄](./survey/2026-04-23-rsrcc.md) | [🔗](https://arxiv.org/abs/2604.20623) |

---

## Meta-Evaluation & Methodology

| Benchmark | What It Evaluates | Added | Notes | Link |
| :--- | :--- | :---: | :---: | :---: |
| **BenchHub** | Benchmark suite unification | 2025 | [📄](./survey/2025-06-01-benchhub.md) | [🔗](https://arxiv.org/abs/2506.00482) |
| **BenchBench** | Benchmark discriminability | 2026 | [📄](./survey/2026-03-21-benchbench.md) | [🔗](https://arxiv.org/abs/2603.20807) |
| **AISafetyBenchExplorer** | AI safety benchmark landscape | 2026 | [📄](./survey/2026-04-14-aisafetybenchexplorer.md) | [🔗](https://arxiv.org/abs/2604.12875) |
| **Rethinking Math Eval** | Math evaluation methodology | 2026 | [📄](./survey/2026-04-25-rethinking-math-eval.md) | [🔗](https://arxiv.org/abs/2604.22597) |

---

*← Back to [README.md](./README.md) &nbsp;|&nbsp; 📅 [Full Archive](./ARCHIVE.md) &nbsp;|&nbsp; 🗂️ [Survey Index](./survey/INDEX.md)*
