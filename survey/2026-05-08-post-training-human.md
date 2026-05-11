# Post-Training Makes Large Language Models Less Human-Like (2026)

## Problem
Large language models are frequently proposed as surrogate participants in behavioural research — standing in for human subjects in psychology experiments, user studies, and social science surveys. This assumption requires that LLMs accurately capture human behavioural patterns. Post-training (RLHF, instruction tuning, safety fine-tuning) is the process that converts base models into practical assistants, but its effect on human-like behavioural alignment has never been rigorously measured at scale. If post-training degrades behavioural alignment, then LLMs cannot serve as valid human surrogates — and the growing practice of replacing human participants with LLMs in research produces invalid results.

## Method
**Psych-201** (arXiv: 2605.07632, May 2026) introduces a new dataset enabling large-scale measurement of behavioural alignment between LLMs and humans across model families, model sizes, and training objectives. The study spans **70+ authors** and evaluates alignment before and after post-training across multiple model generations, enabling causal attribution of misalignment to training stages. Persona-induction techniques — commonly proposed as fixes for individual-level alignment — are also evaluated. Newer model generations are compared against older ones to determine whether alignment trends are improving or worsening over time.

## Benchmarks / Datasets
- Psych-201 dataset (novel; covers multiple behavioural psychology tasks)
- Multiple LLM families compared (base vs. post-trained variants)
- Multiple model generations compared across release timelines
- Persona-induction techniques evaluated as individual-level alignment fixes

## Key Results

| Condition | Finding |
|---|---|
| Base models | Improving behavioural alignment with newer generations |
| Post-trained models | Consistent alignment reduction across all model families |
| Newer generation post-trained vs. older | Wider misalignment despite improved base model alignment |
| Persona-induction as fix | Fails to improve individual-level behavioural prediction |

- **Post-training consistently reduces alignment with human behaviour across all tested model families — the process that makes LLMs useful as assistants simultaneously makes them worse human surrogates**
- Misalignment widens in newer model generations even as base models continue to improve — the post-training penalty is growing, not shrinking
- Persona-induction techniques, widely proposed as fixes for individual-level prediction, fail to improve alignment at the individual level
- Base model behavioural alignment improves with scale and recency, but this improvement is systematically erased by post-training

## Enterprise / Industry Relevance
For Foxconn's FoxBrain, two implications are direct: First, using FoxBrain (a post-trained model) to simulate or predict human operator behaviour, consumer responses, or worker decision-making in scenario planning is methodologically invalid — post-training degrades exactly the human-like behavioural patterns needed for such simulations. Second, Psych-201's finding that persona-induction fails means that prompting FoxBrain with worker or consumer personas will not produce reliable human-behaviour predictions. Any FoxBrain application that relies on the model acting as a human surrogate — for market research, operator behaviour modelling, or HR scenario simulation — requires validation against actual human data, not just persona-prompted outputs.

---
*Back to [Main Digest](../README.md)*
