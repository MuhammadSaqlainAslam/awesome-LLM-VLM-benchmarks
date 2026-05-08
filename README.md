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

## 🚀 Today's Daily 8 (May 8, 2026)

| Paper | Modality | Key Finding | Notes | arXiv |
| :--- | :---: | :--- | :---: | :---: |
| **Cited Not Verified** | LLM | Deep-research agents verify only 39–77% of cited facts; accuracy drops 42% beyond 150 tool calls — citation volume is not a reliability proxy | [📄](./survey/2026-05-08-cited-not-verified.md) | [🔗](https://arxiv.org/abs/2605.06635) |
| **SeQuOR** | LLM | Multi-turn constraint following collapses: >11% drop for single constraints, >40% for multiple simultaneous constraints, >9% for dynamic updates mid-conversation | [📄](./survey/2026-05-08-sequor.md) | [🔗](https://arxiv.org/abs/2605.06353) |
| **TableVista** | LLM/VLM | 30,000-variant table reasoning benchmark (3,000 tables × 10 variants); structural complexity causes pronounced degradation across all 29 tested models | [📄](./survey/2026-05-08-tablevista.md) | [🔗](https://arxiv.org/abs/2605.05955) |
| **Policy Invariance** | LLM | Safety judges flip 9.1% of verdicts from content-preserving rewrites; 18–43% changes on unambiguous cases — evaluator prompt sensitivity is a systemic governance risk | [📄](./survey/2026-05-08-policy-invariance.md) | [🔗](https://arxiv.org/abs/2605.06161) |
| **DBE** | LLM | Dynamic Boundary Evaluation eliminates ceiling + floor effects simultaneously; SGBS algorithm locates capability boundaries via API-only access across 4 safety/alignment dimensions | [📄](./survey/2026-05-08-dbe.md) | [🔗](https://arxiv.org/abs/2605.06213) |
| **BioMedArena** | LLM | Modular 6-layer agent evaluation toolkit: 147 benchmarks, 75 tools; standardisation alone yields **+15.03 pp** average SOTA improvement — prior gains were largely implementation variance | [📄](./survey/2026-05-08-biomedArena.md) | [🔗](https://arxiv.org/abs/2605.06177) |
| **Black-Box CoT Confidence** | LLM | 3-channel trajectory confidence (Coverage + Geometry + Verbalization): AUC 0.78 vs. 0.71 self-consistency; K=4 beats K=8 at half the compute — no logits required | [📄](./survey/2026-05-08-blackbox-confidence.md) | [🔗](https://arxiv.org/abs/2605.06308) |
| **SpatialEpiBench** | LLM | Most spatiotemporal epidemic models underperform a last-value baseline at all horizons (1 day – 1 month); geographic adjacency provides limited signal; 3 systematic failure modes identified | [📄](./survey/2026-05-08-spatialepibench.md) | [🔗](https://arxiv.org/abs/2605.06530) |

> 📋 **[See the full weekly digest →](./WEEKLY.md)** &nbsp;|&nbsp; 📅 **[Full archive →](./ARCHIVE.md)**

---

## 📑 Frontier Model Technical Reports

| Model | Lab | Key Result | Notes | Link |
| :--- | :--- | :--- | :---: | :---: |
| **Kimi-K2.6** | Moonshot AI | 54.0 HLE-Full (beats GPT-5.4) / 58.6 SWE-Bench Pro (best open-weight) / 96.4 AIME 2026 / 1T MoE / Mod. MIT | [📄](./survey/2026-04-27-kimi-k2-6.md) | [🔗](https://huggingface.co/moonshotai/Kimi-K2.6) |
| **Mistral Medium 3.5** | Mistral AI | 77.6% SWE-Bench Verified / 91.4% τ³-Telecom / 128B dense / replaces 3 prior models / per-request reasoning | [📄](./survey/2026-04-30-mistral-medium-3-5.md) | [🔗](https://huggingface.co/mistralai/Mistral-Medium-3.5-128B) |
| **Qwen3.6-27B** | Alibaba | 77.2% SWE-Bench Verified at 27B / 94.1 AIME 2026 / 70.3% AndroidWorld / 1M-token context / Apache-2.0 | [📄](./survey/2026-04-28-qwen3-6-27b.md) | [🔗](https://huggingface.co/Qwen/Qwen3.6-27B) |
| **GPT-5.4** | OpenAI | 75.0% OSWorld-V | [📄](./survey/2026-03-05-gpt-5-4-report.md) | [🔗](https://openai.com/index/introducing-gpt-5-4/) |
| **GPT-5.4 mini/nano** | OpenAI | OSWorld-mini efficiency leader | [📄](./survey/2026-03-22-gpt-5-4-mini.md) | [🔗](https://openai.com/index/introducing-gpt-5-4-mini-and-nano/) |
| **Gemini 3.1 Pro** | Google | 77.1% ARC-AGI-2 | [📄](./survey/2026-02-19-gemini-3-1-pro.md) | [🔗](https://deepmind.google/technologies/gemini/) |
| **Phi-4 Reasoning** | Microsoft | 15B model, strong MathVista | [📄](./survey/2026-03-15-phi-4-reasoning.md) | [🔗](https://www.microsoft.com/en-us/research/wp-content/uploads/2026/03/Phi-4-reasoning-vision-15B-Tech-Report.pdf) |
| **DeepSeek-V4-Pro** | DeepSeek | 93.5 LiveCodeBench / 80.6% SWE-Verified / 1M-token context at 27% V3.2 FLOPs / MIT licence | [📄](./survey/2026-04-28-deepseek-v4.md) | [🔗](https://huggingface.co/deepseek-ai/DeepSeek-V4-Pro) |
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
