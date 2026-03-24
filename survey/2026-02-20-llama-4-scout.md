# Paper Overview: Meta Llama 4 Scout: The High-Throughput Generalist

## Problem
Most long-context models are too slow for interactive research loops. Llama 4 Scout focuses on maximizing **Tokens per Second (TPS)** without sacrificing the 10M token context posture.

## Method
A **Mixture of Experts (MoE)** architecture activating 17B parameters out of 109B. It features a natively multimodal "early fusion" design and is optimized for **2600+ TPS** on modern H100 clusters, the highest recorded speed for a model of this intelligence class.

## Benchmarks / Datasets
* **Long-Context Eval:** Stable retrieval and reasoning up to 10,000,000 tokens.
* **MMLU Pro:** **75.2%**.
* **Speed:** **2600 tok/s** (Fastest in the 70B+ class).

## FoxBrain Relevance
Llama 4 Scout is the ideal **Inference Engine** for our internal R&D chat. Its speed allows for near-instantaneous search across our entire PDF documentation library.

---
*Back to [Main Digest](../README.md)*
