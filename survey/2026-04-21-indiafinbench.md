# IndiaFinBench: An Evaluation Benchmark for Large Language Model Performance on Indian Financial Regulatory Text (2026)

## Problem
Existing financial NLP benchmarks focus almost exclusively on Western markets and regulatory frameworks, leaving a critical gap for the world's fifth-largest economy. LLMs deployed in Indian financial services must interpret regulatory documents from SEBI, RBI, IRDAI, and other authorities — requiring regulatory interpretation, numerical reasoning, contradiction detection, and temporal reasoning skills that no prior benchmark tested in this jurisdiction.

## Method
**IndiaFinBench** (arXiv: 2604.19298, April 21, 2026) is the first publicly available evaluation benchmark for assessing LLM performance on Indian financial regulatory text, containing 406 expert-annotated question-answer pairs across four task types: regulatory interpretation (174 items), numerical reasoning (92 items), contradiction detection (62 items), and temporal reasoning (78 items). All models are evaluated under zero-shot conditions to measure out-of-the-box regulatory reasoning capability.

Authors: Rajveer Singh Pall

## Benchmarks / Datasets
- 406 expert-annotated QA pairs covering Indian financial regulatory documents
- 4 task types: regulatory interpretation, numerical reasoning, contradiction detection, temporal reasoning
- 12 LLMs evaluated under zero-shot conditions
- Human baseline established at 60.0% accuracy

## Key Results

| Model | Accuracy |
|---|---|
| Gemini 2.5 Flash (best) | 89.7% |
| Human Baseline | 60.0% |
| Gemma 4 E4B (weakest) | 70.4% |
| Numerical Reasoning Spread | 35.9 pp (widest gap) |

- **Top model (Gemini 2.5 Flash) achieves 89.7%, surpassing the 60.0% human baseline by nearly 30 percentage points**
- All 12 tested LLMs exceed the human baseline, though performance tiers vary significantly
- Numerical reasoning exhibits the widest performance spread at 35.9 percentage points between strongest and weakest models
- Inter-annotator agreement of kappa=0.611 (76.7% overall) confirms benchmark quality

## FoxBrain Relevance
Foxconn's Shareholder Services, treasury operations, and supplier finance workflows in India require compliance with SEBI listing obligations, RBI foreign exchange regulations, and IRDAI insurance mandates. FoxBrain could be deployed to automate regulatory interpretation and compliance checking for Foxconn India's rapidly expanding manufacturing presence (including the iPhone assembly plant in Tamil Nadu). The numerical reasoning task type directly maps to FoxBrain's use case of parsing and validating financial figures in supplier contracts and regulatory filings. The benchmark's contradiction detection task is particularly relevant for catching inconsistencies in multi-document procurement compliance packages.

---
*Back to [Main Digest](../README.md)*
