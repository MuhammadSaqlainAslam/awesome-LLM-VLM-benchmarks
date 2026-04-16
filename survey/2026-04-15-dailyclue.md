# DailyClue: Seek-and-Solve Benchmarking MLLMs for Visual Clue-Driven Reasoning in Daily Scenarios (2026)

## Problem
Multimodal large language models are typically evaluated on tasks where answers are directly perceivable in images, but fail to assess whether models can actively identify and extract the specific visual clues necessary to solve a question — a process requiring active search and selective attention rather than passive perception. No existing benchmark required models to first locate decisive visual evidence before performing multi-step reasoning, leaving an important capability unmeasured.

## Method
**DailyClue** (arXiv: 2604.14041, April 15, 2026) introduces a benchmark spanning 4 major daily-life domains and 16 distinct subtasks that require models to perform "seek-and-solve" reasoning: identifying decisive visual clues embedded in realistic daily scenario images before answering questions. The benchmark provides comprehensive evaluation across both standard MLLMs and agentic models, with task designs that specifically prevent surface-level perception shortcuts.

Authors: Xiaomin Li, Tala Wang, Zichen Zhong, Ying Zhang, Zirui Zheng, Takashi Isobe, Dezhuang Li, Huchuan Lu, You He, Xu Jia

## Benchmarks / Datasets
- 4 major daily-life domains with 16 distinct subtasks
- Tasks requiring explicit visual clue identification before reasoning
- Evaluation of both standard MLLMs and agentic models
- Challenge design prevents surface-level perception shortcuts
- Covers real-world everyday visual reasoning scenarios

## Key Results

| Model Type | Visual Clue ID Accuracy | Overall Reasoning Performance |
|---|---|---|
| Top MLLMs | Significantly below human | Formidable challenge across all subtasks |
| Agentic models | Marginally better | Better clue localization but still limited |
| Human baseline | High clue accuracy | Strong reasoning from identified clues |

- Accurate identification of visual clues is identified as the critical bottleneck: models that fail to locate the right clue consistently fail the downstream reasoning task.
- The benchmark presents a "formidable challenge" to current state-of-the-art MLLMs, with all tested models falling well below human-level performance across all 16 subtasks.
- Agentic models show modest improvement over standard MLLMs on clue identification, indicating that iterative search strategies partially compensate for passive perception limitations.

## FoxBrain Relevance
DailyClue's seek-and-solve paradigm maps directly to Foxconn's quality control inspection workflows, where FoxBrain agents must identify specific visual defect indicators in product images before making pass/fail decisions — a process that requires targeted attention, not generic image understanding. The 16-subtask structure provides a template for designing FoxBrain visual inspection benchmarks that separate clue-finding capability from post-clue reasoning, enabling more targeted model diagnostics. The benchmark's emphasis on daily-scenario reasoning also validates FoxBrain's coverage for employee-facing applications such as factory-floor troubleshooting assistants and equipment maintenance guidance tools. Understanding where current MLLMs fail on clue-driven reasoning helps prioritize fine-tuning investments for FoxBrain's inspection AI systems.

---
*Back to [Main Digest](../README.md)*
