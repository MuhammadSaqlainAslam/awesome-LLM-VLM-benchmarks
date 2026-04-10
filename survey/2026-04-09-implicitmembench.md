# ImplicitMemBench: Evaluating Implicit Memory Mechanisms in Large Language Models (2026)

## Problem
Research on LLM memory has focused almost exclusively on explicit/declarative memory — whether models can recall facts they were told. But human cognition critically depends on *implicit* (unconscious) memory: procedural skills, priming effects, and conditioned associations that shape behaviour without conscious retrieval. No benchmark existed to test whether LLMs exhibit analogous implicit memory mechanisms or whether they systematically fail at them, despite these mechanisms being essential for coherent long-horizon agentic behaviour.

## Method
**ImplicitMemBench** (arXiv: 2604.08064, April 9, 2026) introduces a unified **Learning/Priming–Interfere–Test** (LIT) protocol to probe three distinct implicit memory types in LLMs, mirroring cognitive psychology paradigms:

1. **Procedural Memory** — Skill retention after interference: models learn a task procedure, are given an interfering task, then are retested. Measures whether skill degrades under interference (as it does in humans with procedural amnesia).
2. **Priming** — Theme-driven response bias: models are exposed to a semantic theme, then tested on ambiguous stimuli. Measures whether prior exposure systematically biases output (preference priming: 75.0%; inhibition priming: 17.6%).
3. **Classical Conditioning** — Stimulus-response associations: models are conditioned on paired stimuli, then tested for stimulus-triggered response patterns.

The evaluation suite contains 300 items. Authors: Chonghan Qin, Xiachong Feng, Weitao Ma, Xiaocheng Feng, Lingpeng Kong.

## Benchmarks / Datasets
- **300-item evaluation suite** across three implicit memory types
- **Protocol:** Learning/Priming–Interfere–Test (LIT) per task
- **Memory types:** Procedural, Priming (preference + inhibition), Classical Conditioning
- **18 models evaluated** spanning 1B to frontier scale
- **Metrics:** First-attempt accuracy; preference vs. inhibition asymmetry; conditioning transfer score

## Key Results

| Model | Overall Acc | Notes |
|---|---|---|
| **DeepSeek-R1** | **65.3%** | Top performer |
| Qwen3-32B | 64.1% | |
| GPT-5 | 63.0% | |
| Frontier average | ~60% | No model exceeds 66% |

- **Dramatic asymmetry between preference priming (75.0%) and inhibition priming (17.6%)** — models are far better at being nudged toward something than being conditioned to avoid it
- No model exceeds **66% overall** — implicit memory mechanisms are significantly weaker than explicit recall across all architectures
- Larger models show stronger procedural retention but not stronger inhibition priming
- Classical conditioning transfer is the weakest capability across all tested models

## FoxBrain Relevance
ImplicitMemBench reveals a fundamental gap in LLM memory architecture directly relevant to FoxBrain's long-horizon agent deployments: while FoxBrain may explicitly recall instructions, it may fail to retain procedural skills across distractor tasks (critical for multi-step factory workflows) and may be easily primed toward incorrect outputs by upstream context. The 17.6% inhibition priming score is particularly concerning for FoxBrain safety features — the model may be unable to sustain "avoid X" constraints when distractor content is present. Recommended: add ImplicitMemBench's LIT protocol to FoxBrain's regression suite before any production deployment involving sequential multi-task agents.

---
*Back to [Main Digest](../README.md)*
