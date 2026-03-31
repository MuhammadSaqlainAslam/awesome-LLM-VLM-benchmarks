# LegalEval-Q: A Benchmark for Quality Evaluation of LLM-Generated Legal Text (2025)

## Problem
Legal LLM evaluation has focused primarily on factual accuracy and task completion, neglecting the linguistic quality dimensions — clarity, coherence, and proper legal terminology — that determine whether AI-generated legal text is actually usable by practitioners. No benchmark existed to measure these quality axes at scale across a broad range of LLMs.

## Method
LegalEval-Q introduces a regression-model-based quality scoring framework that evaluates LLM outputs on three dimensions: clarity, coherence, and terminology correctness. The framework is applied to evaluate **49 LLMs** of varying sizes (from small to 72B+ parameter models), with fine-grained analysis of the effects of model scale, quantization, and reasoning architecture on legal text quality.

## Benchmarks / Datasets
- **LegalEval-Q:** Specialized legal question set; outputs from 49 LLMs scored by regression quality model.
- **Dimensions:** Clarity, coherence, legal terminology correctness.
- **Metrics:** Regression-based quality scores per dimension; aggregated quality rank.
- **GitHub:** https://github.com/lyxx3rd/LegalEval-Q

## Key Results
Quality plateaus sharply around **14B parameters**, with only a **+2.7% gain** at 72B — suggesting diminishing returns from scaling for legal text quality specifically. Engineering choices like quantization have negligible impact on quality scores. **Reasoning model architectures consistently outperform base models** of comparable size, confirming that chain-of-thought reasoning is the decisive factor for legal text quality.

## FoxBrain Relevance
Actionable insight for FoxBrain's legal or compliance-adjacent applications: prioritize reasoning-capable model architectures (CoT/RL-trained) over raw parameter count for legal text tasks. The 14B quality plateau is a practical signal that scaling beyond that threshold for legal quality alone is cost-inefficient; invest in architectural improvements instead.

---
*Back to [Main Digest](../README.md)*
