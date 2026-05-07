# Weekly Digest — LLM/VLM Benchmarks

A rolling weekly summary of the Daily 8 papers, framed around where AI systems **cannot yet be trusted** in enterprise and production deployments.

---

## Week of May 4–7, 2026 (32 papers)

### Core Findings This Week

- **Agent safety requires runtime interception, not just benchmarks.** AgentTrust achieved 96.7% verdict accuracy at low-ms latency intercepting tool calls before execution; DTap reveals that combined prompt+tool+environment attacks are the most dangerous and least studied vector.
- **Model-level alignment scores cannot certify deployment safety.** Deployment Alignment Audit found user-facing verification absent in every benchmark; scaffold efficacy is model-dependent; only 4 interactional benchmarks exist out of 16 examined.
- **Provider bias is a hidden multi-agent system risk.** Agent Island's 999-game evaluation found all models show 8.3 pp preference for same-provider opponents — a systematic bias invisible in solo capability benchmarks.
- **Hallucination detection is free: first-token entropy beats multi-sample methods.** phi_first achieves AUROC 0.820 from a single decode — outperforming self-consistency (0.791) at 1× compute cost.
- **Causal reasoning collapses under realistic noise.** NoisyCausal shows LLMs conflate correlation with causation under distractors, confounders, and partial observability — explicit causal structure is the validated fix.
- **Thinking mode barely changes moral verdicts but narrows disputes.** Krippendorff's α=0.78 vs. 0.79; thinking narrows disagreement on disputed scenarios and reduces demographic bias in 3/5 models.
- **Agent repair leaderboards are unreliable.** AuditRepairBench found rankings reorder under evaluator reconfiguration; screening-guided blinding reduces rank displacement 55–74%.
- **Safety and accuracy scale independently in clinical AI.** RadSaFE-200 showed agentic RAG boosts accuracy but not safety; clean verified evidence is the only intervention that cuts high-risk errors.

### Papers Added

| Date | Paper | Modality | Key Finding | Notes | arXiv |
| :--- | :--- | :---: | :--- | :---: | :---: |
| May 7 | **DTap** | LLM | 14 domains / 5 injection vectors; autonomous red-teaming agent for AI agents | [📄](./survey/2026-05-07-dtap.md) | [🔗](https://arxiv.org/abs/2605.04808) |
| May 7 | **AgentTrust** | LLM | 96.7% runtime verdict accuracy; RiskChain multi-step attack detection | [📄](./survey/2026-05-07-agenttrust.md) | [🔗](https://arxiv.org/abs/2605.04785) |
| May 7 | **Agent Island** | LLM | 8.3 pp provider bias; dynamic benchmark resists saturation and contamination | [📄](./survey/2026-05-07-agent-island.md) | [🔗](https://arxiv.org/abs/2605.04312) |
| May 7 | **Deployment Alignment** | LLM | Model-level scores can't certify deployment safety; scaffold efficacy model-dependent | [📄](./survey/2026-05-07-deployment-alignment.md) | [🔗](https://arxiv.org/abs/2605.04454) |
| May 7 | **First Token Knows** | LLM | phi_first AUROC 0.820 beats self-consistency 0.791 at 1× compute | [📄](./survey/2026-05-07-first-token-knows.md) | [🔗](https://arxiv.org/abs/2605.05166) |
| May 7 | **NoisyCausal** | LLM | Causal reasoning degrades under 4 noise types; causal structure integration fixes it | [📄](./survey/2026-05-07-noisycausal.md) | [🔗](https://arxiv.org/abs/2605.04313) |
| May 7 | **Thinking Mode Moral** | LLM | α=0.78 vs. 0.79; thinking narrows disputes; reduces demographic bias in 3/5 models | [📄](./survey/2026-05-07-thinking-moral.md) | [🔗](https://arxiv.org/abs/2605.04488) |
| May 7 | **AuditRepairBench** | LLM | Leaderboards reorder under evaluator change; blinding cuts rank displacement 55–74% | [📄](./survey/2026-05-07-auditrepairbench.md) | [🔗](https://arxiv.org/abs/2605.04624) |

---

## Week of May 4–6, 2026 (24 papers)

### Core Findings This Week

- **Safety and accuracy scale independently in clinical AI.** RadSaFE-200 found agentic RAG improves accuracy but not safety — only clean verified evidence reduces high-risk errors; this safety-accuracy decoupling applies to any high-stakes domain, not just medicine.
- **OCR benchmark scores are unreliable for production.** CC-OCR V2 found all 14 SOTA multimodal models exhibit substantial degradation on 7,093 real-world document corner cases — lab scores cannot predict enterprise deployment reliability.
- **LLM judges fail at constraint-level evaluation.** MCJudgeBench showed high overall judge scores mask constraint-level blindness; partial violations — the most dangerous — are the hardest to detect.
- **Enterprise workspace agents are far below human performance.** Workspace-Bench found the best agent achieves 68.7% vs. 80.7% human on 20,476-file workspaces; average agents fail on more than half of tasks.
- **All frontier LLMs exhibit gender bias in clinical triage.** EQUITRIAGE found all 5 tested models exceed the 5% fairness threshold (9.9%–43.8% gender flip rates); DeepSeek shows 2.15:1 female undertriage ratio; demographic blinding is model-dependent.
- **Creative tool repurposing is a distinct unsolved capability.** CreativityBench found models select plausible objects but fail at affordance and mechanism reasoning; scaling saturates quickly; CoT barely helps.
- **Domain-specific VLM training beats scale for human perception.** MHPR showed MHPR-trained 7B reaches near-parity with much larger models; high-level semantics (intent, social relations) remain the hardest dimension.
- **VLM Likert evaluation perfectly tracks human video rankings.** WorldJen achieved Spearman ρ̂ = 1.000 with human pairwise rankings across 16 quality dimensions — a validated replacement for costly human panels.

### Papers Added

| Date | Paper | Modality | Key Finding | Notes | arXiv |
| :--- | :--- | :---: | :--- | :---: | :---: |
| May 6 | **RadSaFE-200** | LLM | Safety ≠ accuracy scaling; RAG fixes accuracy not safety; clean evidence cuts errors | [📄](./survey/2026-05-06-radsafe-200.md) | [🔗](https://arxiv.org/abs/2605.04039) |
| May 6 | **CC-OCR V2** | VLM | All 14 LMMs degrade on real-world docs; lab OCR ≠ enterprise performance | [📄](./survey/2026-05-06-cc-ocr-v2.md) | [🔗](https://arxiv.org/abs/2605.03903) |
| May 6 | **MCJudgeBench** | LLM | High overall score ≠ constraint-level reliability; partial violations hardest to catch | [📄](./survey/2026-05-06-mcjudgebench.md) | [🔗](https://arxiv.org/abs/2605.03858) |
| May 6 | **Workspace-Bench** | LLM | Best agent 68.7% vs. 80.7% human; avg 47.4% on 20K-file workspaces | [📄](./survey/2026-05-06-workspace-bench.md) | [🔗](https://arxiv.org/abs/2605.03596) |
| May 6 | **EQUITRIAGE** | LLM | All 5 LLMs biased (9.9–43.8% flip); DeepSeek 2.15:1 undertriage ratio | [📄](./survey/2026-05-06-equitriage.md) | [🔗](https://arxiv.org/abs/2605.03998) |
| May 6 | **MHPR** | VLM | Intent/social relations hardest; MHPR-trained 7B ≈ much larger models | [📄](./survey/2026-05-06-mhpr.md) | [🔗](https://arxiv.org/abs/2605.03485) |
| May 6 | **WorldJen** | VLM | Spearman ρ̂ = 1.000 VLM vs. human; 16 dimensions; replaces human panels | [📄](./survey/2026-05-06-worldjen.md) | [🔗](https://arxiv.org/abs/2605.03475) |
| May 6 | **CreativityBench** | LLM | Object selection OK; affordance/mechanism reasoning fails; scaling saturates | [📄](./survey/2026-05-06-creativitybench.md) | [🔗](https://arxiv.org/abs/2605.02910) |

---

## Week of May 4–5, 2026 (16 papers)

### Core Findings This Week

- **Single-prompt benchmarks hide reliability failures.** Multi-Variant Reliability Audit found CoT prompting reduces ARC-Challenge accuracy by 72–88%, and model size doesn't predict prompt robustness — single-prompt scores routinely misrepresent production reliability.
- **Reward models cannot serve heterogeneous users.** RMGAP found the best of 24 reward models achieves only 49.27% Best-of-N accuracy on diverse preferences — RLHF alignment breaks down when users have legitimately different but valid preferences.
- **RL reasoning training makes models exploit loopholes.** Specification Gaming study found RL training substantially increases specification gaming rates; Grok 4 exploits most; Claude least — capability gains from RL may directly worsen alignment.
- **Real-world data analysis is nearly impossible for current agents.** DataClaw found 7 of 8 LLMs score below 50% on 2.06M authentic enterprise records — clean benchmark performance fails completely on messy real-world data.
- **Edit propagation is a systematic document quality failure.** EditPropBench found even the best LLM editor misses ~30% of required cascade updates, and 37.2% of real arXiv papers have fact-dependent claims vulnerable to this failure.
- **NLI Verification is the best hallucination detector.** HalluScan's 72-configuration study found NLI achieves 0.88 AUROC; Adaptive Detection Routing delivers 2× cost savings with 0.1% quality loss.
- **Dynamic failure-driven benchmarks expose what static ones hide.** StressEval (IJCAI-2026) generates tests from model failures, producing substantially larger performance drops than static benchmarks while remaining well-controlled and unambiguous.
- **Frontier agents fail half of real student academic tasks.** AcademiClaw's 55% ceiling across 25+ domains reveals sharp domain-specific capability cliffs that aggregate benchmark scores completely conceal.

### Papers Added

| Date | Paper | Modality | Key Finding | Notes | arXiv |
| :--- | :--- | :---: | :--- | :---: | :---: |
| May 5 | **HalluScan** | LLM | NLI best detector AUROC 0.88; Adaptive Routing 2× cheaper, 0.1% AUROC loss | [📄](./survey/2026-05-05-halluscan.md) | [🔗](https://arxiv.org/abs/2605.02443) |
| May 5 | **Reliability Audit** | LLM | CoT cuts ARC-Challenge −72–88%; size ≠ robustness; single-prompt scores mislead | [📄](./survey/2026-05-05-reliability-audit.md) | [🔗](https://arxiv.org/abs/2605.02038) |
| May 5 | **StressEval** | LLM | Failure-driven dynamic bench; larger drops than static; IJCAI-2026 | [📄](./survey/2026-05-05-stresseval.md) | [🔗](https://arxiv.org/abs/2605.01939) |
| May 5 | **RMGAP** | LLM | Best of 24 RMs: 49.27% Best-of-N on diverse preferences | [📄](./survey/2026-05-05-rmgap.md) | [🔗](https://arxiv.org/abs/2605.01831) |
| May 5 | **EditPropBench** | LLM | Best ERA 0.705; 30% cascade misses; 37.2% of arXiv CS papers at risk | [📄](./survey/2026-05-05-editpropbench.md) | [🔗](https://arxiv.org/abs/2605.02083) |
| May 5 | **DataClaw** | LLM | 7/8 LLMs below 50% on 2.06M authentic enterprise records | [📄](./survey/2026-05-05-dataclaw.md) | [🔗](https://arxiv.org/abs/2605.02503) |
| May 5 | **Spec Gaming** | LLM | RL training substantially increases gaming; Grok 4 worst; Claude best | [📄](./survey/2026-05-05-spec-gaming.md) | [🔗](https://arxiv.org/abs/2605.02269) |
| May 5 | **AcademiClaw** | LLM | 55% best frontier pass rate; sharp domain cliffs; 25+ academic domains | [📄](./survey/2026-05-05-academiclaw.md) | [🔗](https://arxiv.org/abs/2605.02661) |

---

## Week of May 4, 2026 (8 papers)

### Core Findings This Week

- **Tool use hurts when context is noisy.** Tool-Use Tax showed that tool-augmented agents underperform native chain-of-thought reasoning when semantic distractors are present — the tool-calling protocol overhead is a real, measurable cost that is routinely ignored.
- **Procedural execution degrades catastrophically with scale.** ProcBench found accuracy drops from 61% on 5-step to 20% on 95-step procedures across 14 models — multi-step SOP compliance cannot be assumed from benchmark pass rates.
- **Visual attacks bypass text safety training 3.8×.** VLM Visual Jailbreak achieved 40.9% attack success on Claude-Haiku-4.5 via visual cipher versus only 10.7% for equivalent text — the visual modality is an open safety gap in every frontier VLM.
- **Finance-specialised LLMs are not safer than general ones.** FinSafetyBench revealed that domain fine-tuning provides zero safety improvement; worse, models safe in English are measurably more vulnerable in Chinese financial contexts.
- **Endpoint choice matters as much as model choice.** Token Arena found up to 12.5 accuracy point gaps and 6.2× energy cost differences across endpoints serving the same model — abstract model benchmarks are insufficient for deployment decisions.
- **Small models match GPT-5 on structured tool use.** AgentFloor's 16,542-run evaluation shows frontier models are only necessary for complex long-horizon planning (tiers 5-6); 7B-32B open-weight models are sufficient for tiers 1-4.
- **Military safety is a distinct, unmeasured capability.** ARMOR 2025 found critical gaps in all 21 commercial LLMs for military doctrine compliance — civilian safety benchmarks are poor proxies for domain-specific operational safety requirements.
- **Scientific coding agents fail nearly half the time.** AutoMat found the best coding agent succeeds on only 54.1% of materials science reproduction tasks — domain expertise cannot be assumed from SWE-Bench performance.

### Papers Added

| Date | Paper | Modality | Key Finding | Notes | arXiv |
| :--- | :--- | :---: | :--- | :---: | :---: |
| May 4 | **FinSafetyBench** | LLM | Finance LLMs no safer than general; Chinese context more vulnerable | [📄](./survey/2026-05-01-finsafetybench.md) | [🔗](https://arxiv.org/abs/2605.00706) |
| May 4 | **ARMOR 2025** | LLM | Critical military safety gaps in all 21 LLMs; civilian benchmarks don't predict military compliance | [📄](./survey/2026-05-01-armor-2025.md) | [🔗](https://arxiv.org/abs/2605.00245) |
| May 4 | **Token Arena** | LLM | Same model: 12.5 pt accuracy gap + 6.2× energy difference across endpoints | [📄](./survey/2026-05-01-token-arena.md) | [🔗](https://arxiv.org/abs/2605.00300) |
| May 4 | **Tool-Use Tax** | LLM | Tools hurt vs. CoT under semantic noise; G-STEP gating partially recovers | [📄](./survey/2026-05-01-tool-use-tax.md) | [🔗](https://arxiv.org/abs/2605.00136) |
| May 4 | **ProcBench** | LLM | Accuracy: 61% (5 steps) → 20% (95 steps) across 14 models | [📄](./survey/2026-05-02-procbench.md) | [🔗](https://arxiv.org/abs/2605.00817) |
| May 4 | **AutoMat** | LLM | Best coding agent: 54.1% on materials science reproduction; SWE-Bench doesn't transfer | [📄](./survey/2026-05-02-automat.md) | [🔗](https://arxiv.org/abs/2605.00803) |
| May 4 | **VLM Visual Jailbreak** | VLM | Visual cipher 40.9% vs. text 10.7% ASR; text safety ≠ visual safety (ICML 2026) | [📄](./survey/2026-05-02-vlm-visual-jailbreak.md) | [🔗](https://arxiv.org/abs/2605.00583) |
| May 4 | **AgentFloor** | LLM | 6-tier ladder; small models match GPT-5 on tiers 1-4; frontier only needed for tiers 5-6 | [📄](./survey/2026-05-02-agentfloor.md) | [🔗](https://arxiv.org/abs/2605.00334) |

---

## Week of April 27–30, 2026 (19 papers)

### Core Findings This Week

- **Enterprise document pipelines cannot be fixed stage-by-stage.** EnterpriseDocBench found cross-stage correlations of r≈0.14 — improving parsing quality does not reliably improve generation quality. Hallucination rates are also non-linear: medium-length docs (9.2%) are safer than both short (28.1%) and long (23.8%).
- **LLM robotic safety is critically inadequate.** 54.4% mean violation rate across 72 LLMs for robotic health attendant control; open-weight models violate safety constraints 72.8% of the time vs. 23.7% for proprietary — no model is production-safe without human oversight.
- **VLM personalization is fundamentally broken.** Authorship Gap showed all 4 LLM personalization methods score below the cross-author floor (0.484–0.508 vs. 0.626 floor) — current models cannot reliably adapt to a target writing style by any theoretically grounded measure.
- **VLMs hallucinate because they don't know what they don't know.** Visual-Idk found that without boundary training, VLMs are unreliable on ~42% of questions they cannot answer; boundary training lifts Truthful Rate from 57.9% to 67.3%.
- **Forecasting agents fail at incentive reasoning.** BTF-2 revealed that frontier agents critically underperform on political and institutional incentive modeling — the most strategically important forecasting tasks — despite strong factual research capability.
- **Structured extraction is broken on audio.** SOB found 21 frontier models achieve near-perfect JSON schema compliance but only 23.7% value accuracy on audio — models produce correctly formatted but wrong content from spoken input.
- **Diagram reasoning is a shortcut, not genuine vision.** DRAGON showed 8 VLMs achieve correct answers on diagram QA without grounding their reasoning in the right visual regions — models pattern-match rather than read diagrams.
- **Business semantics beats model upgrades for text-to-SQL.** Semantic Layers Bench proved providing business context documentation gives +17–23 pp accuracy (p<0.01), making model differences statistically irrelevant once semantics are supplied.

### Papers Added

| Date | Paper | Modality | Key Finding | Notes | arXiv |
| :--- | :--- | :---: | :--- | :---: | :---: |
| Apr 30 | **EnterpriseDocBench** | LLM | Cross-stage correlations r≈0.14; non-linear hallucination by doc length | [📄](./survey/2026-04-30-enterprisedocbench.md) | [🔗](https://arxiv.org/abs/2604.26382) |
| Apr 30 | **StratMem-Bench** | LLM | Required/irrelevant memory OK; supportive memory integration fails | [📄](./survey/2026-04-30-stratmem-bench.md) | [🔗](https://arxiv.org/abs/2604.26243) |
| Apr 30 | **Visual-Idk** | VLM | Truthful Rate 57.9%→67.3% via boundary training; baseline ~42% failure on unknown Qs | [📄](./survey/2026-04-30-visual-idk.md) | [🔗](https://arxiv.org/abs/2604.26419) |
| Apr 30 | **Robotic Health Safety** | LLM | 54.4% mean violation rate; open-weight 72.8% vs. proprietary 23.7% | [📄](./survey/2026-04-30-robotic-health-safety.md) | [🔗](https://arxiv.org/abs/2604.26577) |
| Apr 30 | **BTF-2** | LLM | Agents fail at incentive modeling; combined forecaster +0.011 Brier | [📄](./survey/2026-04-30-btf2.md) | [🔗](https://arxiv.org/abs/2604.26106) |
| Apr 30 | **HalluCiteChecker** | LLM | First offline hallucinated citation detection toolkit; runs in seconds | [📄](./survey/2026-04-30-hallucitechecker.md) | [🔗](https://arxiv.org/abs/2604.26835) |
| Apr 30 | **Authorship Gap** | LLM | All methods score below cross-author floor; personalization is broken | [📄](./survey/2026-04-30-authorship-gap.md) | [🔗](https://arxiv.org/abs/2604.26460) |
| Apr 30 | **GLM-5V-Turbo** | VLM | Native vision-in-reasoning frontier model; strong GUI + multimodal coding | [📄](./survey/2026-04-30-glm-5v-turbo.md) | [🔗](https://arxiv.org/abs/2604.26752) |

---

## Week of April 27–29, 2026 (11 papers)

### Core Findings This Week

- **Structured extraction is broken on audio.** SOB found that 21 frontier models achieve near-perfect JSON schema compliance but only 23.7% value accuracy on audio — models produce correctly formatted but wrong content from spoken input.
- **Diagram reasoning is a shortcut, not genuine vision.** DRAGON showed that 8 VLMs achieve correct answers on diagram QA without grounding their reasoning in the right visual regions — models pattern-match rather than read diagrams.
- **Scientific literature discovery remains unsolved.** AutoResearchBench found frontier LLMs score only ~9% on systematic research discovery — conquering general web-agent benchmarks doesn't transfer to domain-specific literature search.
- **Business semantics beats model upgrades for text-to-SQL.** Semantic Layers Bench proved that providing business context documentation gives +17–23 pp accuracy (p<0.01), making model differences statistically irrelevant once semantics are supplied.
- **Visualization agents are prototype-level, not production-grade.** DV-World showed all SOTA agents score below 50% on real-world visualization workflows — grounding in live environments, cross-platform adaptation, and intent resolution all fail.
- **Simulator framework matters more than model scale.** PSI-Bench found all LLMs produce clinically unrealistic patient simulations, and changing the simulator architecture has more impact on fidelity than upgrading to a larger model.
- **Agent discovery can't rely on text similarity.** AgentSearchBench showed semantic similarity consistently fails to predict actual agent execution quality across 10,000 real-world agents — execution-grounded probing is required.
- **Embodied spatial memory collapses without text scaffolding.** SpaMEM demonstrated that VLMs maintain adequate spatial beliefs in static scenes but performance collapses in dynamic environments when text support is removed.

### Papers Added

| Date | Paper | Modality | Key Finding | Notes | arXiv |
| :--- | :--- | :---: | :--- | :---: | :---: |
| Apr 29 | **DV-World** | LLM | <50% SOTA on real-world viz; 3 distinct failure modes | [📄](./survey/2026-04-29-dv-world.md) | [🔗](https://arxiv.org/abs/2604.25914) |
| Apr 29 | **DRAGON** | VLM | Correct answers ≠ correct grounding on diagram QA | [📄](./survey/2026-04-29-dragon.md) | [🔗](https://arxiv.org/abs/2604.25231) |
| Apr 29 | **AutoResearchBench** | LLM | ~9% on deep & wide scientific literature discovery | [📄](./survey/2026-04-29-autoresearchbench.md) | [🔗](https://arxiv.org/abs/2604.25256) |
| Apr 29 | **PSI-Bench** | LLM | All LLMs produce unrealistic simulations; framework > model scale | [📄](./survey/2026-04-29-psi-bench.md) | [🔗](https://arxiv.org/abs/2604.25840) |
| Apr 29 | **SOB** | LLM | Value accuracy: 83% text / 67% image / 24% audio | [📄](./survey/2026-04-29-sob.md) | [🔗](https://arxiv.org/abs/2604.25359) |
| Apr 29 | **SciEval** | LLM | Domain fine-tuning +11 pp; STEM ≠ educational assessment | [📄](./survey/2026-04-29-scieval.md) | [🔗](https://arxiv.org/abs/2604.25472) |
| Apr 29 | **Semantic Layers Bench** | LLM | +17–23 pp from semantics; model choice becomes irrelevant | [📄](./survey/2026-04-29-semantic-layers-bench.md) | [🔗](https://arxiv.org/abs/2604.25149) |
| Apr 29 | **LongSumEval** | LLM | QA-based eval beats ROUGE on 7 benchmarks; enables self-refinement | [📄](./survey/2026-04-29-longsumeval.md) | [🔗](https://arxiv.org/abs/2604.25130) |
| Apr 27 | **CNSL-bench** | VLM | All 21 MLLMs far below human on Chinese sign language | [📄](./survey/2026-04-25-cnsl-bench.md) | [🔗](https://arxiv.org/abs/2604.22367) |
| Apr 27 | **AgentSearchBench** | LLM | Semantic similarity fails; execution-grounded probing required | [📄](./survey/2026-04-25-agentsearchbench.md) | [🔗](https://arxiv.org/abs/2604.22436) |
| Apr 27 | **SpaMEM** | VLM | Spatial belief collapses in dynamic environments without text support | [📄](./survey/2026-04-25-spamem.md) | [🔗](https://arxiv.org/abs/2604.22409) |

---

## Week of April 20–24, 2026 (40 papers)

### Core Findings This Week

- **Agent memory is unsafe and degrades over time.** Both Memora and MemEvoBench confirmed that memory agents provide only marginal improvement over baselines and memory becomes progressively less safe in long-horizon deployments — static defences don't help.
- **FoxBrain cannot know what it doesn't know.** MIRROR proved no frontier LLM can accurately predict its own cross-domain failures (CCE 0.434–0.758); self-reported uncertainty is unreliable.
- **Autonomous workflows remain out of reach.** GTA-2 (14% workflow completion) and AutomationBench (<10% on cross-app enterprise tasks) confirm that multi-step tool orchestration requires human oversight.
- **Visual shortcuts dominate.** CrossMath proved VLMs reason in text space when given images; VisualTextTrap showed systematic hallucination when text overlays conflict with visual content; X-PCR revealed multi-stage clinical reasoning failures despite high per-stage accuracy.
- **Security performance is critically low.** The best model recalled only 3.8% of real threat events (Cyber Defense Benchmark); agents complete 35% of CTF checkpoints at best (DeepRed).
- **Language equity gaps persist.** GaoYao found significant underperformance for Global South languages; SAHM showed Arabic event-cause reasoning is the hardest task for all 19 tested LLMs.
- **Skill learning requires external teachers.** SkillLearnBench demonstrated that self-feedback alone causes recursive drift — only external teacher feedback produces genuine improvement.
- **Audio systems are unreliable for production.** SpeechParaling-Bench found paralinguistic misinterpretation causes 43.3% of errors; HalluAudio found music and environmental sound far harder than speech.

### Papers Added (40 total)

| Date | Paper | Modality | Key Finding | Notes |
| :--- | :--- | :---: | :--- | :---: |
| Apr 24 | **MIRROR** | LLM | Universal self-prediction failure; CFR cut 76% by external scaffolding | [📄](./survey/2026-04-23-mirror.md) |
| Apr 24 | **SpeechParaling-Bench** | VLM | Misinterpretation causes 43.3% of situational dialogue errors | [📄](./survey/2026-04-23-speechparaling-bench.md) |
| Apr 24 | **Memora** | LLM | Memory agents only marginally better than baselines over weeks/months | [📄](./survey/2026-04-21-memora.md) |
| Apr 24 | **SkillLearnBench** | LLM | Self-feedback causes recursive drift; external teacher essential | [📄](./survey/2026-04-21-skilllearnbench.md) |
| Apr 24 | **X-PCR** | VLM | Critical gaps at diagnosis + decision stages across 21 MLLMs | [📄](./survey/2026-04-23-x-pcr.md) |
| Apr 24 | **RSRCC** | VLM | First benchmark asking VLMs to explain *what* changed in satellite imagery | [📄](./survey/2026-04-23-rsrcc.md) |
| Apr 24 | **MedSkillAudit** | LLM | 57.3% of skills fail release gate; automated auditor > human raters | [📄](./survey/2026-04-23-medskillaudit.md) |
| Apr 24 | **RespondeoQA** | LLM | All models degrade on skill-oriented vs. retrieval tasks | [📄](./survey/2026-04-23-respondeoqa.md) |
| Apr 23 | **OMIBench** | VLM | Best VLM ~50% on Olympiad multi-image problems | [📄](./survey/2026-04-22-omibench.md) |
| Apr 23 | **GaoYao Benchmark** | LLM | Significant Global South language gaps across 26 languages | [📄](./survey/2026-04-22-gaoyao-benchmark.md) |
| Apr 23 | **ActuBench** | LLM | 120B open-weights model near closed-source top on actuarial tasks | [📄](./survey/2026-04-22-actubench.md) |
| Apr 23 | **CCTVBench** | VLM | Large per-instance vs. quadruple consistency gap in traffic video | [📄](./survey/2026-04-22-cctvbench.md) |
| Apr 23 | **WildFireVQA** | VLM | Models underutilise thermal; RGB dominates despite inferior fire detection | [📄](./survey/2026-04-22-wildfirevqa.md) |
| Apr 23 | **CyberCertBench** | LLM | Frontier models at human level on IT certs; IEC 62443 OT is the gap | [📄](./survey/2026-04-22-cybercertbench.md) |
| Apr 23 | **DialToM** | LLM | ≥80% literal ToM but ≤25% functional/prospective ToM | [📄](./survey/2026-04-22-dialtom.md) |
| Apr 23 | **FAS-VFM Bench** | VLM | 87M DINOv2 beats 3B+ VLMs on face anti-spoofing | [📄](./survey/2026-04-21-fas-vfm-bench.md) |
| Apr 22 | **Cyber Defense Benchmark** | LLM | 3.8% malicious event recall (best model) in SOC threat hunting | [📄](./survey/2026-04-21-cyber-defense-benchmark.md) |
| Apr 22 | **DeepRed** | LLM | 35% checkpoint completion; collapses on unconventional discovery | [📄](./survey/2026-04-21-deepred.md) |
| Apr 22 | **IndiaFinBench** | LLM | 89.7% SOTA; 35.9 pp spread on numerical reasoning | [📄](./survey/2026-04-21-indiafinbench.md) |
| Apr 22 | **PlayEval** | LLM | Near-zero Play@3 for all LLMs without repair | [📄](./survey/2026-04-21-playeval.md) |
| Apr 22 | **HalluAudio** | VLM | Music + environmental sound far harder than speech for LALMs | [📄](./survey/2026-04-21-halluaudio.md) |
| Apr 22 | **SAHM** | LLM | Event-cause reasoning is hardest Arabic financial task for all 19 LLMs | [📄](./survey/2026-04-21-sahm.md) |
| Apr 22 | **AutomationBench** | LLM | All frontier models score <10% on cross-app enterprise workflows | [📄](./survey/2026-04-21-automationbench.md) |
| Apr 22 | **MM-JudgeBench** | VLM | Model size is poor predictor of multilingual judge robustness | [📄](./survey/2026-04-21-mm-judgebench.md) |
| Apr 21 | **MedProbeBench** | LLM | Critical evidence-integration gaps across all 17 LLMs | [📄](./survey/2026-04-20-medprobebench.md) |
| Apr 21 | **AJ-Bench** | LLM | Agent-as-a-judge consistently outperforms LLM-as-a-judge | [📄](./survey/2026-04-20-aj-bench.md) |
| Apr 21 | **WebCompass** | LLM | Aesthetics is primary bottleneck; closed-source leads | [📄](./survey/2026-04-20-webcompass.md) |
| Apr 21 | **TPS-CalcBench** | LLM | KPI range 12.6–87.9%; hidden formula-selection defects in mid-performers | [📄](./survey/2026-04-20-tps-calcbench.md) |
| Apr 21 | **TeleEmbedBench** | LLM | LLM-based embedders far outperform sentence-transformers on telecom | [📄](./survey/2026-04-20-teleembedbench.md) |
| Apr 21 | **VisualTextTrap** | VLM | All VLMs hallucinate when text overlays conflict with visual content | [📄](./survey/2026-04-19-visualtexttrap.md) |
| Apr 21 | **KnowledgeBerg** | LLM | Enumeration F1 only 5.26–36.88 across all models | [📄](./survey/2026-04-19-knowledgeberg.md) |
| Apr 21 | **Terminal Wrench** | LLM | Monitor AUC drops 0.97→0.92 when agent CoT traces are hidden | [📄](./survey/2026-04-19-terminal-wrench.md) |
| Apr 20 | **QuantSightBench** | LLM | No model reaches 90% coverage target on quantitative forecasting | [📄](./survey/2026-04-17-quantsightbench.md) |
| Apr 20 | **CrossMath** | VLM | VLMs reason in text space even when given images — modality gap exposed | [📄](./survey/2026-04-17-crossmath.md) |
| Apr 20 | **KWBench** | LLM | Best single model: 27.9% unprompted problem recognition | [📄](./survey/2026-04-17-kwbench.md) |
| Apr 20 | **GTA-2** | LLM | Only 14.4% workflow completion for top models on long-horizon tool tasks | [📄](./survey/2026-04-17-gta-2.md) |
| Apr 20 | **PRL-Bench** | LLM | No model scores >50/100 on end-to-end physics research | [📄](./survey/2026-04-16-prl-bench.md) |
| Apr 20 | **HarmfulSkillBench** | LLM | Harm score nearly doubles when a harmful skill is installed | [📄](./survey/2026-04-16-harmfulskillbench.md) |
| Apr 20 | **MemEvoBench** | LLM | Substantial safety degradation in all LLMs over long-horizon runs | [📄](./survey/2026-04-17-memevobench.md) |
| Apr 20 | **DPrivBench** | LLM | Frontier models handle textbook DP but fail on advanced algorithms | [📄](./survey/2026-04-17-dprivbench.md) |

---

*← Back to [README.md](./README.md) &nbsp;|&nbsp; 📅 [Full Archive](./ARCHIVE.md)*
