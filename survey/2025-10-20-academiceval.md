# Paper Overview: AcademicEval: Live Long-Context LLM Benchmark

## Problem
Standard long-context benchmarks suffer from **label leakage** (data contamination) and rigid context lengths. AcademicEval aims to evaluate LLMs on real-world, hierarchical academic writing tasks using a "live" data stream to ensure models haven't memorized the answers.

## Method
Introduces a live benchmark that pulls the latest papers from **arXiv**. It tasks models with generating Titles, Abstracts, Introductions, and Related Work based on long-context inputs. It utilizes a **co-author graph** to provide flexible, expert-curated few-shot demonstrations.

## Benchmarks / Datasets
* **Data Source:** Live arXiv feed (periodically updated to prevent leakage).
* **Metrics:** BERTScore, ROUGE-L, and **LLM-as-a-Judge** (assessing novelty, consistency, and style).
* **Findings:** Performance drops sharply as input length grows; Retrieval-Augmented Generation (RAG) is preferred for Related Work, while long-context LLMs perform better on Abstracts.

## FoxBrain Relevance
We can use the **AcademicEval pipeline** to test FoxBrain's ability to summarize our internal R&D technical reports and white papers without worrying about the model relying on pre-trained "leaked" knowledge.

---
*Back to [Main Digest](../README.md)*
