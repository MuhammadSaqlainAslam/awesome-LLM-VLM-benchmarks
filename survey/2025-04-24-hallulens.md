# HalluLens: LLM Hallucination Benchmark (2025)

## Problem
Hallucination evaluation in LLMs has lacked a principled taxonomy, leading to fragmented benchmarks that conflate distinct failure modes. Without distinguishing between extrinsic hallucination (outputs inconsistent with world knowledge from training) and intrinsic hallucination (outputs inconsistent with the provided input context), it is impossible to diagnose or systematically address the problem.

## Method
HalluLens introduces a comprehensive benchmark built on a two-way taxonomy: **extrinsic hallucination** (evaluated via PreciseWikiQA, LongWiki, and NonExistentEntities tasks) and **intrinsic hallucination** (evaluated via context-contradiction tasks). A key innovation is dynamic test set generation that regenerates evaluation instances periodically to prevent data leakage and benchmark gaming. Published as a long paper at ACL 2025.

## Benchmarks / Datasets
- **PreciseWikiQA:** Fact-seeking QA requiring precise factual retrieval.
- **LongWiki:** Long-form factual generation evaluated for extrinsic consistency.
- **NonExistentEntities:** Detection of hallucinated entities that do not exist in reference sources.
- **Intrinsic Tasks:** Context-contradiction detection in RAG-style settings.
- **Metrics:** Accuracy, hallucination rate, entity existence F1; dynamically regenerated test sets.
- **GitHub:** https://github.com/facebookresearch/HalluLens

## Key Results
The taxonomy reveals that models with low extrinsic hallucination rates can still exhibit high intrinsic hallucination under context contradiction, and vice versa — confirming these are distinct failure modes requiring targeted mitigation. Dynamic test regeneration exposes significant benchmark inflation in models reportedly achieving low hallucination rates on static sets.

## FoxBrain Relevance
Essential for FoxBrain's reliability roadmap. Before deploying FoxBrain in any factual or RAG-based application, both hallucination axes must be tested. The NonExistentEntities task is particularly relevant for enterprise knowledge base applications where FoxBrain might plausibly fabricate product names, specifications, or process steps that sound credible but do not exist.

---
*Back to [Main Digest](../README.md)*
