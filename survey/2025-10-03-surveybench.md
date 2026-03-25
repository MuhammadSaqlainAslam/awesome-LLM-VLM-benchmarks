# Paper Overview: SurveyBench: Can LLM-Agents Write Academic Surveys?

## Problem
While agents can draft text, human-quality academic surveys require deep synthesis, logical chapter planning, and meticulously categorized literature. Existing benchmarks fail to capture the "insight gap" where AI summaries remain surface-level.

## Method
A fine-grained, **quiz-driven evaluation framework**. It features 4,947 high-quality human surveys as references. The evaluation uses a multifaceted hierarchy to assess outline quality, coverage breadth, and "associative reasoning" (the ability to connect cross-domain concepts).

## Benchmarks / Datasets
* **Scale:** 11,343 arXiv papers and ~5k surveys.
* **Key Finding:** AI-generated surveys score **21% lower than humans** in content-based evaluations, particularly struggling with synthesis and abstraction.

## FoxBrain Relevance
This benchmark provides a roadmap for our **DeepResearch Agent**. By implementing the "quiz-driven validation" from SurveyBench, we can ensure our agents aren't just summarizing but actually "understanding" the technical papers they read.

---
*Back to [Main Digest](../README.md)*
