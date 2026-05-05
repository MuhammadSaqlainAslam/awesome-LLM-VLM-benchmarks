# EditPropBench: Measuring Factual Edit Propagation in Scientific Manuscripts (2026)

## Problem
When a factual claim in a scientific document changes — a dataset grows from 10K to 12K samples, a metric improves from 82% to 84% — all dependent statements throughout the document must be updated to remain consistent. This "edit propagation" problem is invisible to standard editing benchmarks that measure only whether the directly edited sentence is correct. In production document editing workflows, LLMs that successfully update the primary fact but miss cascading dependent statements produce internally inconsistent documents — a critical quality failure for technical and regulatory writing.

## Method
**EditPropBench** (arXiv: 2605.02083, May 2026) introduces a benchmark of synthetic ML/NLP manuscripts with **controlled fact graphs**, **targeted edits**, and **sentence-level dependency labels**. Three editing protocols are evaluated across **five LLM editing systems**. A new metric — **Edit-Ripple Adherence (ERA)** — measures the fraction of required cascade updates that are correctly propagated. Adversarial metric probes and stress-test variants are included. A corpus study of recent arXiv computer science papers establishes how prevalent fact-dependent qualitative claims are in real scientific writing.

## Benchmarks / Datasets
- Synthetic ML/NLP manuscripts with controlled fact graphs
- Sentence-level dependency labels (ground truth cascade paths)
- Three editing protocols
- Adversarial metric probes + stress-test variants
- Primary metric: Edit-Ripple Adherence (ERA)
- 5 LLM editing systems evaluated
- Corpus study: recent arXiv computer science papers

## Key Results

| System | ERA Score |
|---|---|
| Weakest LLM editor | 0.148 |
| Strongest LLM editor | **0.705** |
| Gap to perfect (1.0) | ~30% missed cascades even at best |

| Corpus Study Finding | Result |
|---|---|
| arXiv CS papers with fact-dependent qualitative claims | **37.2%** |

- **The strongest LLM editing system achieves ERA of 0.705 — missing approximately 30% of required cascade updates even at best performance**
- ERA range of 0.148–0.705 across five systems reveals large unexplained variation in editing cascade capability — editing reliability is not correlated with general capability
- 37.2% of recent arXiv computer science papers contain fact-dependent qualitative claims — edit propagation failures affect the majority of real scientific documents
- The weakest system (ERA 0.148) propagates fewer than 1 in 6 required cascades — documents edited by such systems are systematically inconsistent

## Enterprise / Industry Relevance
Foxconn produces large volumes of technical documentation where factual changes cascade through dependent statements: engineering specifications where a material property change ripples through tolerance tables and process parameters, regulatory filings where a production volume figure cascades through compliance calculations, and supplier contracts where pricing terms affect multiple downstream clauses. EditPropBench's finding that even the best LLM editing system misses 30% of required cascade updates is a direct warning for FoxBrain's document editing workflows. FoxBrain cannot be trusted to produce internally consistent documents after factual edits without explicit cascade verification — any FoxBrain document editing workflow must include a post-edit consistency check step that verifies all numerically or factually dependent claims have been updated. The ERA metric is directly adoptable as a FoxBrain document quality KPI.

---
*Back to [Main Digest](../README.md)*
