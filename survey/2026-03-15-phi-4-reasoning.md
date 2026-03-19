# Paper Overview: Phi-4 Reasoning-Vision

## Problem
What problem does this paper solve?
Existing small-scale multimodal models struggle with complex multi-step reasoning and typically rely on massive parameter counts to achieve high accuracy.

## Method
What approach did they use?
Microsoft used a "reasoning-first" training approach with interleaved vision-text data and synthetic data generation to boost Chain-of-Thought (CoT) capabilities.

## Benchmarks / Datasets
List all benchmarks and datasets used.
* **Benchmarks:** MMMU, MathVista, Blink, AI2D.
* **Datasets:** Interleaved Vision-Text, synthetic reasoning-heavy datasets.

## Key Results
At least one concrete number.
Achieves **76.1% on MathVista**, outperforming several models twice its size (+5.4% over previous 15B SOTA).

## FoxBrain Relevance
Is there anything we can learn or apply to FoxBrain?
Highly relevant. We can apply their "interleaved data" strategy to our internal training pipelines to improve 15B-class model efficiency.
