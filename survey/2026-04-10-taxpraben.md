# TaxPraBen: Structured Evaluation of LLMs on Chinese Real-World Tax Practice (2026)

## Problem
Tax practice represents one of the most demanding real-world professional knowledge domains for LLMs: it requires mastery of dense regulatory text, numerical calculation accuracy, multi-step reasoning across interacting rules, and domain-specific judgment that cannot be replaced by generic language understanding. Existing LLM benchmarks for legal/regulatory domains use simplified or synthetic tasks; no benchmark evaluated LLM capabilities across the full spectrum of professional tax practice — from basic NLP tasks to complex real-world scenarios like tax risk prevention, inspection analysis, and strategic tax planning.

## Method
**TaxPraBen** (arXiv: 2604.08948, April 10, 2026) constructs a **scalable benchmark** across **14 datasets** spanning **10 traditional NLP tax tasks + 3 novel real-world scenarios**, structured according to **Bloom's Taxonomy** (6 cognitive levels: Remember → Understand → Apply → Analyze → Evaluate → Create) to ensure systematic difficulty progression. The 3 novel real-world scenarios are:

1. **Tax Risk Prevention** — identify tax compliance risks in business transaction descriptions
2. **Tax Inspection Analysis** — interpret and reason over tax audit findings
3. **Tax Strategy Planning** — generate optimal tax strategies given business context and regulatory constraints

Evaluation uses structured parsing-field alignment for extraction tasks and exact numerical/textual matching for calculation tasks. Authors: Gang Hu, Yating Chen, Haiyan Ding, Wang Gao et al. (8 total).

## Benchmarks / Datasets
- **7,300 instances** across 14 datasets
- **10 traditional NLP tasks:** Named entity recognition, relation extraction, text classification, QA, etc.
- **3 novel real-world scenarios:** Tax risk prevention, inspection analysis, strategy planning
- **Bloom's Taxonomy** difficulty structure (6 cognitive levels)
- **Metrics:** Structured parsing-field alignment; numerical/textual exact matching

## Key Results

| Model Category | Performance | Notes |
|---|---|---|
| **Closed-source large-param LLMs** | **Best overall** | Lead on complex reasoning scenarios |
| **Chinese-specialised LLMs (Qwen2.5)** | **Best among Chinese models** | Outperform multilingual alternatives on Chinese tax text |
| Multilingual general LLMs | Lower on Chinese tasks | Language-specific knowledge gap |
| All models | Weakest on Tax Strategy Planning | Highest cognitive level (Bloom's Create) |

- **Closed-source large-parameter LLMs generally outperform** open-source alternatives across all 14 datasets
- **Chinese-specialised models (Qwen2.5) outperform multilingual alternatives** on Chinese regulatory tax text, confirming domain-language alignment matters
- **Tax Strategy Planning** (Bloom's Level 6: Create) is the hardest scenario — requires integrating multiple regulatory constraints to generate novel strategies, not just retrieve or classify
- The Bloom's Taxonomy structure reveals a consistent performance cliff at Level 5 (Evaluate) → Level 6 (Create) for all evaluated models

## FoxBrain Relevance
TaxPraBen directly benchmarks the regulatory compliance reasoning capabilities needed for Foxconn's tax, finance, and legal operations across Asian markets. The finding that Chinese-specialised models outperform multilingual ones is critical for FoxBrain's deployment in Taiwan, China, and Japan — generic multilingual models underperform on jurisdiction-specific regulatory text. The Bloom's Taxonomy framework provides a structured capability ladder for FoxBrain's compliance features: verify competence at each cognitive level (Remember → Create) before deploying in increasingly complex regulatory reasoning tasks. The 3 novel scenarios (risk prevention, inspection analysis, strategy planning) map directly onto Foxconn's compliance workflow priorities.

---
*Back to [Main Digest](../README.md)*
