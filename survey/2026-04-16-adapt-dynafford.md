# ADAPT: Benchmarking Commonsense Planning under Unspecified Affordance Constraints (2026)

## Problem
Existing embodied AI benchmarks assume static object affordances explicitly specified in task instructions, failing to capture real-world environments where object states change dynamically and affordance constraints are never explicitly stated. Agents must infer which actions are physically possible from current object states — a commonsense capability that prior benchmarks do not systematically evaluate.

## Method
**ADAPT** (arXiv: 2604.14902, April 16, 2026) introduces DynAfford, a benchmark for evaluating agents in environments where affordances change dynamically and are never explicitly stated in instructions. The paper presents a plug-and-play module augmenting existing planners with explicit affordance reasoning, using a domain-adapted LoRA-finetuned vision-language model as the affordance inference backend.

Authors: Pei-An Chen, Yong-Ching Liang, Jia-Fong Yeh, Hung-Ting Su, Yi-Ting Chen, Min Sun, Winston Hsu

## Benchmarks / Datasets
- DynAfford benchmark with dynamically changing object affordances
- Tasks span embodied household planning scenarios with unspecified constraints
- Comparison of LoRA-finetuned VLM vs. commercial LLM (GPT-4o) as affordance backend
- Metrics: task success rate with and without affordance-aware planning module

## Key Results

| Approach | Affordance Backend | Outcome |
|---|---|---|
| Existing planners (baseline) | None | Fails on dynamic affordance constraints |
| ADAPT module + LoRA VLM | Domain-adapted finetuned VLM | Outperforms GPT-4o backend |
| ADAPT module + GPT-4o | Commercial LLM | Strong but below domain-adapted VLM |
| Plug-and-play integration | Any existing planner | Modular affordance reasoning boost |

- **Domain-adapted LoRA-finetuned VLM outperforms GPT-4o as affordance inference backend**
- The plug-and-play affordance module significantly improves success rates on DynAfford vs. base planners
- Unspecified affordance constraints expose a critical gap in current embodied AI planning systems

## FoxBrain Relevance
ADAPT's focus on dynamic, unspecified affordance constraints maps directly to Foxconn's robotics and automated assembly contexts, where a robot arm or mobile platform must infer whether an action is physically feasible given the current state of parts, fixtures, or workpieces — without explicit runtime specification. The benchmark's key finding that domain-adapted finetuned VLMs beat commercial LLMs validates Foxconn's strategy of fine-tuning FoxBrain on manufacturing-specific visual contexts. The plug-and-play affordance module design suggests a practical path for adding constraint-aware planning to existing FoxBrain robotic control pipelines without full architectural overhaul.

---
*Back to [Main Digest](../README.md)*
