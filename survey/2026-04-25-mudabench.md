# MuDABench: Navigating Large-Scale Document Collections for Multi-Document Analytical QA (2026)

## Problem
Enterprise knowledge work often requires synthesizing and performing quantitative analysis across large collections of documents — not just retrieving a single fact from one source. Standard retrieval-augmented generation (RAG) pipelines treat document collections as a flat pool and fail at tasks that require cross-document reasoning and structured aggregation. No benchmark had specifically targeted this class of multi-document analytical question answering at scale.

## Method
**MuDABench** (arXiv: 2604.22239, April 25, 2026) is a benchmark for analytical question answering requiring synthesis of information across numerous documents to perform quantitative analysis. It comprises 332 analytical QA instances drawn from over 80,000 pages of source documents. The benchmark evaluates both final answer accuracy and intermediate-fact coverage, the latter serving as a diagnostic signal for understanding where RAG pipelines break down. The authors also propose a multi-agent workflow as an improved solution and identify the two primary performance bottlenecks.

## Benchmarks / Datasets
- 332 analytical QA instances requiring cross-document quantitative synthesis
- Over 80,000 pages of source documents
- Two evaluation metrics: final answer accuracy and intermediate-fact coverage
- Multi-agent workflow proposed as a baseline solution
- Tasks require aggregation, counting, comparison, and synthesis across multiple documents

## Key Results

| Evaluation Dimension | Key Finding |
|---|---|
| Standard RAG performance | Poor — flat document pooling fails on analytical tasks |
| Multi-agent workflow | Substantially improves both process and outcome metrics |
| Primary bottleneck 1 | Single-document information extraction accuracy |
| Primary bottleneck 2 | Insufficient domain-specific knowledge in current systems |
| Human vs. model gap | Significant performance gap remains even with multi-agent approach |

- **Standard RAG systems treating documents as a flat pool perform poorly on multi-document analytical tasks — the core architecture is insufficient for synthesis at scale**
- The proposed multi-agent workflow substantially improves both process quality (intermediate-fact coverage) and outcome quality (final answer accuracy)
- Two primary bottlenecks identified: (1) per-document extraction accuracy limits what information is available for synthesis; (2) domain knowledge gaps cause models to fail at quantitative reasoning even when facts are available
- A significant performance gap versus human experts persists even with the best proposed approach

## FoxBrain Relevance
Foxconn generates massive volumes of internal documents — engineering reports, supplier specifications, quality audit records, procurement contracts, and production logs — that span thousands of pages across many files. MuDABench directly measures the capability FoxBrain would need to answer analytical questions like "Which supplier had the highest defect rate across Q1–Q3 reports?" or "Summarize all compliance failures mentioned across the 2025 audit documents." The benchmark's finding that flat RAG fails and multi-agent pipelines are needed guides FoxBrain's document intelligence architecture toward structured multi-agent extraction and synthesis workflows rather than single-pass retrieval.

---
*Back to [Main Digest](../README.md)*
