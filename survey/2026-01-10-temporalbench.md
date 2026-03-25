# Paper Overview: TemporalBench: Fine-grained Temporal Understanding

## Problem
Existing video benchmarks lack fine-grained temporal annotations. Consequently, models often use "language priors" (guessing based on the caption) rather than actually "seeing" the temporal dynamics.

## Method
A benchmark for fine-grained temporal event understanding. It consists of **10,000 QA pairs** derived from 2,000 high-quality human captions. It tests action frequency, motion magnitude, and event order.

## Benchmarks / Datasets
* **MBA Accuracy:** GPT-4o achieves only **38.0% accuracy** on multiple-binary QA.
* **Gap:** Highlights a ~30% gap between human and AI temporal understanding.

## FoxBrain Relevance
TemporalBench reveals a major blind spot in current VLMs. For FoxBrain's **Security Video agents**, we must implement the "Multiple Binary Accuracy" (MBA) check from this paper to ensure our models are actually seeing the events in order.

---
*Back to [Main Digest](../README.md)*
