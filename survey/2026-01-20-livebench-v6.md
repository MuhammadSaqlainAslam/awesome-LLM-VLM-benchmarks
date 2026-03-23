# Paper Overview: LiveBench: A Contamination-Free Benchmark for LLMs

## Problem
What problem does this paper solve? (1–2 sentences)
As LLMs are trained on vast portions of the internet, they frequently encounter the questions and answers of static benchmarks (like MMLU), leading to artificially inflated scores. LiveBench solves this by releasing new, high-quality tasks every month based on recent data and proprietary reasoning problems that the models could not have seen during training.

## Method
What approach did they use? (1–2 sentences)
The framework automatically collects new problems from recent sources (like new LeetCode contests, recent news, and ArXiv papers) and converts them into standardized test formats. It uses a "zero-contamination" pipeline that forces models to rely on zero-shot reasoning rather than memory, with all tasks being verifiable through objective ground-truth answers.

## Benchmarks / Datasets
List all benchmarks and datasets used.
* **Reasoning:** Math problems from 2025/2026 Olympiads and Logic puzzles.
* **Coding:** Problems from LeetCode and AtCoder released after Jan 2026.
* **Language:** Instruction following and long-context retrieval from recent news.
* **Comparison:** LiveBench scores are routinely compared against MMLU-Pro and GPQA to highlight the "Memorization Gap."

## Key Results
At least one concrete number.
Models that score 90%+ on MMLU often drop to **45–55% on LiveBench**, proving that static benchmarks significantly overestimate true reasoning capabilities. As of the Jan 2026 refresh, **GPT-5 and DeepSeek-V3.2** are the only models maintaining a >60% average on the most difficult reasoning tiers.

## FoxBrain Relevance
Is there anything we can learn or apply to FoxBrain?
Critical for our internal validation. To ensure FoxBrain models are actually "smart" and not just "memorizing," we should adopt the LiveBench methodology: **never test a model on data that was available before its training cutoff.** We should implement a "Dynamic Evaluation" layer in our roadmap that pulls fresh problems monthly.

---
*Back to [Main Digest](../README.md)*
