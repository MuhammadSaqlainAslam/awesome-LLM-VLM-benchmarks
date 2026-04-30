# KnowledgeBerg: Evaluating Systematic Knowledge Coverage and Compositional Reasoning in Large Language Models (2026)

## Problem
Existing LLM knowledge benchmarks test isolated facts but do not evaluate whether models maintain systematic coverage of entire knowledge categories (e.g., all capital cities, all chemical elements) or can compose multiple retrieved facts into coherent multi-step reasoning chains. This leaves a critical gap in understanding whether LLMs possess structured, encyclopedic knowledge or merely recognize high-frequency facts.

## Method
**KnowledgeBerg** (arXiv: 2604.17621, April 19, 2026) introduces a benchmark of 4,800 multiple-choice questions derived from 1,183 enumeration seeds across 10 knowledge domains and 17 languages. Two evaluation tracks are defined: universe enumeration (knowledge width — can the model enumerate all members of a category?) and knowledge-grounded compositional reasoning (knowledge depth — can it combine multiple facts into a correct multi-step answer?). Evaluation is grounded in authoritative sources to prevent annotation noise.

Authors: Xiao Zhang, Qianru Meng, Yongjian Chen, Yumeng Wang, Johan Bos

## Benchmarks / Datasets
- 4,800 multiple-choice questions from 1,183 enumeration seeds
- 10 knowledge domains, 17 languages
- Two tracks: universe enumeration (width) + compositional reasoning (depth)
- Key metrics: Universe Enumeration F1, Compositional Reasoning Accuracy, Test-Time Compute Gain, RAG Gain

## Key Results

| Track | Score Range (Across Models) | Best Intervention |
|---|---|---|
| Universe Enumeration (F1) | 5.26 – 36.88 | RAG +3.78 pts |
| Compositional Reasoning (Acc) | 16.00 – 44.19 | Test-time compute +4.35 pts |

- **Universe enumeration F1 ranges only 5.26–36.88, exposing massive systematic knowledge gaps even in leading LLMs**
- Compositional reasoning accuracy of 16.00–44.19 shows that composing multiple facts remains a hard unsolved problem
- Test-time compute scaling improves compositional reasoning by up to 4.35 points but provides diminishing returns on enumeration
- Retrieval augmentation helps enumeration (+3.78 pts) more than test-time compute, suggesting different remedies for different knowledge failure modes

## Enterprise / Industry Relevance
Foxconn's supply chain management requires systematic knowledge of all approved suppliers, component specifications, certification standards, and regulatory requirements across multiple domains — precisely the "universe enumeration" capability KnowledgeBerg measures. FoxBrain's ability to reliably list all relevant ISO standards for a given product category, or enumerate every approved vendor for a specific component, directly impacts procurement accuracy and compliance. KnowledgeBerg's finding that RAG is the best remedy for enumeration gaps aligns with Foxconn's investment in retrieval-augmented enterprise knowledge bases, and the benchmark provides a concrete way to measure FoxBrain's systematic knowledge coverage before deploying it in supplier qualification or audit workflows.

---
*Back to [Main Digest](../README.md)*
