# Rollout Cards: A Reproducibility Standard for Agent Research (2026)

## Problem
Agent benchmark papers report final scores while making the underlying rollout records that generated those scores impossible to inspect. Identical agent behaviour can receive different reported scores depending on which portion of a rollout is evaluated, how failed or errored runs are handled, and what reporting rules are applied — yet these choices are rarely disclosed. This means benchmark leaderboards reflect a combination of actual agent capability and undisclosed reporting decisions, making it impossible to determine whether performance differences between published results represent genuine capability differences or artefacts of incompatible reporting. The field has no standard for what evidence must be preserved and disclosed alongside a reported score.

## Method
**Rollout Cards** (arXiv: 2605.12131, May 2026) introduces a publication standard requiring **rollout card bundles** that preserve complete rollout records and explicitly declare: (1) the **views** used (which portions of the rollout count toward the score), (2) the **reporting rules** applied (how edge cases, failures, and partial completions are handled), and (3) the **drops manifest** (which runs were excluded and why). The authors audited **50 popular agent training and evaluation repositories** and documented 37 cases where reporting rule variation altered task-success rates or timing measurements. A reference implementation is provided in the Ergon framework.

## Benchmarks / Datasets
- 50 popular agent training/evaluation repositories (structured audit)
- 4 partial public rollout releases (tool safety, multi-agent, theorem proving, search)
- Re-grading experiments: short-answer, code-generation, and tool-use tasks
- Benchmarks covered: tool use, software engineering, web interaction, multi-agent, safety, search

## Key Results

| Metric | Finding |
|---|---|
| Repos reporting failed/errored/skipped runs | **0 of 50** (zero) |
| Score change from reporting rule variation alone | Up to **±20.9 absolute percentage points** |
| Cases where reporting rules inverted frontier model rankings | Documented in multiple tasks |

- **Zero of 50 audited agent repositories disclose failed, errored, or skipped runs — the field systematically omits evidence that would reduce reported scores**
- **Reporting rule changes alone shift scores by up to 20.9 absolute percentage points** — without any change in agent behaviour — and can invert which frontier model leads the leaderboard
- 37 cases of reporting rule variation altering task-success rates or timing measurements were documented across the 50-repo audit
- Rollout cards solve this by making the evidentiary basis of every score fully inspectable and reproducible

## Enterprise / Industry Relevance
Foxconn's FoxBrain procurement and model selection decisions rely on published benchmark scores from model vendors and leaderboards. Rollout Cards' finding that these scores can differ by up to 20.9 pp from reporting rule choices alone — without any underlying capability difference — means FoxBrain model selection based on leaderboard rankings is unreliable. More critically, zero of 50 audited repositories disclose their failed run handling, which systematically inflates all published agent scores. For Foxconn's internal FoxBrain evaluation pipeline, adopting rollout card standards is immediately actionable: require vendors to provide rollout records (not just scores), declare which runs were dropped and why, and specify the reporting rules applied. This converts FoxBrain vendor evaluation from opaque score comparison to reproducible evidence auditing.

---
*Back to [Main Digest](../README.md)*
