# SOTA LLM/VLM Benchmarks Digest

A curated dashboard of the frontier in AI evaluation. **Updated Daily — Target 8 Papers/Day.**

---

## 🗺️ Navigate the Repo

| Resource | Description |
| :--- | :--- |
| 📅 **[Full Archive](./ARCHIVE.md)** | Chronological history of every Daily 8 entry |
| 📚 **[Benchmark Reference](./BENCHMARKS.md)** | Curated stable reference — 200+ benchmarks by domain |
| 🗂️ **[Survey Index](./survey/INDEX.md)** | All deep-dive notes organised by topic area |
| 📋 **[Weekly Digest](./WEEKLY.md)** | Rolling weekly summary with industry trust gaps |

---

## 🚀 Today's Daily 8 (April 30, 2026)

| Paper | Modality | Key Finding | Notes | arXiv |
| :--- | :---: | :--- | :---: | :---: |
| **EnterpriseDocBench** | LLM | Cross-stage pipeline correlations are near-zero (r≈0.14) — fixing parsing doesn't fix generation; hallucination is non-linear: medium docs (9.2%) safer than short (28.1%) or long (23.8%) | [📄](./survey/2026-04-30-enterprisedocbench.md) | [🔗](https://arxiv.org/abs/2604.26382) |
| **StratMem-Bench** | LLM | LLMs handle required vs. irrelevant memory fine but fail at supportive memory integration — the judgment of when and how to enrich a response is beyond current capability | [📄](./survey/2026-04-30-stratmem-bench.md) | [🔗](https://arxiv.org/abs/2604.26243) |
| **Visual-Idk** | VLM | VLM Truthful Rate improves 57.9%→67.3% via knowledge boundary training; without it, models hallucinate ~42% of the time on questions they cannot actually answer | [📄](./survey/2026-04-30-visual-idk.md) | [🔗](https://arxiv.org/abs/2604.26419) |
| **Robotic Health Safety** | LLM | 54.4% mean violation rate across 72 LLMs for robotic health attendant control; open-weight models (72.8%) nearly 3× less safe than proprietary (23.7%) | [📄](./survey/2026-04-30-robotic-health-safety.md) | [🔗](https://arxiv.org/abs/2604.26577) |
| **BTF-2** | LLM | Frontier forecasting agents critically fail at political/business incentive modelling; combined forecaster beats any single model (+0.011 Brier) — no model dominates | [📄](./survey/2026-04-30-btf2.md) | [🔗](https://arxiv.org/abs/2604.26106) |
| **HalluCiteChecker** | LLM | First NLP toolkit for hallucinated citation detection; runs fully offline in seconds — critical for AI-generated document integrity at scale | [📄](./survey/2026-04-30-hallucitechecker.md) | [🔗](https://arxiv.org/abs/2604.26835) |
| **Authorship Gap** | LLM | All 4 LLM personalization methods score below the cross-author floor (0.484–0.508 vs. floor 0.626) — current models cannot reliably personalize writing style | [📄](./survey/2026-04-30-authorship-gap.md) | [🔗](https://arxiv.org/abs/2604.26460) |
| **GLM-5V-Turbo** | VLM | First frontier model integrating vision as a native reasoning component (not an add-on); strong multimodal coding, visual tool use, and GUI agent performance | [📄](./survey/2026-04-30-glm-5v-turbo.md) | [🔗](https://arxiv.org/abs/2604.26752) |

> 📋 **[See the full weekly digest →](./WEEKLY.md)** &nbsp;|&nbsp; 📅 **[Full archive →](./ARCHIVE.md)**

---

## 📑 Frontier Model Technical Reports

| Model | Lab | Key Result | Notes | Link |
| :--- | :--- | :--- | :---: | :---: |
| **GPT-5.4** | OpenAI | 75.0% OSWorld-V | [📄](./survey/2026-03-05-gpt-5-4-report.md) | [🔗](https://openai.com/index/introducing-gpt-5-4/) |
| **GPT-5.4 mini/nano** | OpenAI | OSWorld-mini efficiency leader | [📄](./survey/2026-03-22-gpt-5-4-mini.md) | [🔗](https://openai.com/index/introducing-gpt-5-4-mini-and-nano/) |
| **Gemini 3.1 Pro** | Google | 77.1% ARC-AGI-2 | [📄](./survey/2026-02-19-gemini-3-1-pro.md) | [🔗](https://deepmind.google/technologies/gemini/) |
| **Phi-4 Reasoning** | Microsoft | 15B model, strong MathVista | [📄](./survey/2026-03-15-phi-4-reasoning.md) | [🔗](https://www.microsoft.com/en-us/research/wp-content/uploads/2026/03/Phi-4-reasoning-vision-15B-Tech-Report.pdf) |
| **DeepSeek-V3.2** | DeepSeek | RL-based logic, MMLU-Pro + IMO | [📄](./survey/2026-03-24-deepseek-v3-2.md) | [🔗](https://arxiv.org/abs/2512.02556) |
| **ARC-AGI-2** | ARC Prize | Non-semantic visual abduction | [📄](./survey/2026-03-24-arc-agi-2.md) | [🔗](https://arxiv.org/abs/2603.06590) |
| **ERNIE 5.0** | Baidu | Trillion-param unified MoE | [📄](./survey/2026-02-07-ernie-5.md) | [🔗](https://arxiv.org/abs/2602.04705) |
| **Emu3.5** | BAAI | 94.03 TIIF-Bench; 20× gen speedup | [📄](./survey/2025-10-30-emu3-5.md) | [🔗](https://arxiv.org/abs/2510.26583) |
| **Qwen3.5-Omni** | Alibaba | WER 1.11 Librispeech; 119 languages | [📄](./survey/2025-09-22-qwen3-5-omni.md) | [🔗](https://arxiv.org/abs/2509.17765) |

---

## 🏭 Enterprise Evaluation Roadmap

A prioritised checklist of benchmarks to run against enterprise LLM/VLM deployments — ordered by deployment risk and evaluation ROI.

### 🔴 Pre-Deployment Gates (Run Before Any Production Release)
- [ ] **[SimpleQA](./survey/2024-11-01-simpleqa.md)** — hallucination stress-test on every checkpoint before release
- [ ] **[HalluLens](./survey/2025-04-24-hallulens.md)** — extrinsic + intrinsic hallucination suites for any RAG or factual output pipeline
- [ ] **[TraceSafe-Bench](./survey/2026-04-08-tracesafe-bench.md)** — mid-trajectory tool-calling safety before any agentic deployment
- [ ] **[HINTBench](./survey/2026-04-15-hintbench.md)** — intrinsic agent safety validation on long agentic trajectories
- [ ] **[MemEvoBench](./survey/2026-04-17-memevobench.md)** — memory safety degradation check before persistent agent deployment
- [ ] **[MedSkillAudit](./survey/2026-04-23-medskillaudit.md)** — pre-release skill audit gate (target: <57% below threshold)

### 🟡 Capability Baselines (Establish Before Fine-Tuning)
- [ ] **[MMLU-Pro](./survey/2024-06-03-mmlu-pro.md)** — multi-domain knowledge baseline across 14 disciplines
- [ ] **[AgentBench](./survey/2023-08-07-agentbench.md)** — agent capability baseline before and after every major architecture upgrade
- [ ] **[SWE-bench Verified](./survey/2026-03-23-claude-4-6.md)** — code engineering capability baseline
- [ ] **[StructEval](./survey/2025-12-08-structeval.md)** — structured output reliability across 18 formats
- [ ] **[MIRROR](./survey/2026-04-23-mirror.md)** — metacognitive calibration; measure Compositional Calibration Error before deployment
- [ ] **[SOB](./survey/2026-04-29-sob.md)** — structured extraction accuracy on text/image/audio before any data pipeline deployment
- [ ] **[KWBench](./survey/2026-04-17-kwbench.md)** — unprompted problem recognition in professional knowledge work

### 🟢 Domain-Specific Evaluations (Before Vertical Deployments)
- [ ] **[MATHVERSE Vision-Only](./survey/2024-03-22-mathverse.md)** — confirm genuine diagram reading vs. text shortcuts before engineering schematics deployment
- [ ] **[VLM-RobustBench](./survey/2026-03-06-vlm-robustbench.md)** — geometric robustness before any factory-floor visual deployment
- [ ] **[TPS-CalcBench](./survey/2026-04-20-tps-calcbench.md)** — engineering calculation accuracy before safety-critical design tasks
- [ ] **[IndicDB](./survey/2026-04-15-indicdb.md)** / **[Semantic Layers Bench](./survey/2026-04-29-semantic-layers-bench.md)** — text-to-SQL accuracy; build semantic layer before deployment
- [ ] **[AutomationBench](./survey/2026-04-21-automationbench.md)** — cross-app workflow orchestration; expect <10% without specialised training
- [ ] **[GTA-2](./survey/2026-04-17-gta-2.md)** — multi-step tool workflow completion; expect <15% for complex workflows
- [ ] **[LongSumEval](./survey/2026-04-29-longsumeval.md)** — QA-based summarisation fidelity before document summarisation deployment
- [ ] **[Cyber Defense Benchmark](./survey/2026-04-21-cyber-defense-benchmark.md)** — threat-hunting recall before any SOC/security assistant deployment
- [ ] **[MuDABench](./survey/2026-04-25-mudabench.md)** — multi-document analytical QA before enterprise knowledge base deployment
- [ ] **[AgentSearchBench](./survey/2026-04-25-agentsearchbench.md)** — agent discovery accuracy before routing layer deployment in multi-agent systems

---

*Built with ❤️ for the AI evaluation community. Contributions welcome — see [ARCHIVE.md](./ARCHIVE.md) for the full history.*
