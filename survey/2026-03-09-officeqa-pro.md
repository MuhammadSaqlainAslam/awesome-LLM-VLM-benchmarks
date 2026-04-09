# OfficeQA Pro: Evaluating LLMs on Long-Form Financial Document QA (2026)

## Problem
Most document QA benchmarks use short documents (< 50 pages) and synthetic question-answer pairs, failing to evaluate the challenges posed by real-world enterprise corpora that span decades, thousands of pages, and millions of numerical values. Financial, legal, and regulatory knowledge work routinely requires reasoning across massive heterogeneous document collections — a scenario where frontier LLMs' parametric knowledge, web-augmented retrieval, and document-access capabilities all fail to meet professional standards.

## Method
OfficeQA Pro constructs **133 expert-validated questions** over the complete corpus of US Treasury Department Bulletins — a real-world financial regulatory archive spanning approximately 100 years, **89,000 pages**, and over **26 million numerical values**. Questions require multi-document reasoning, temporal aggregation, and numerical comparison across the full corpus. Three evaluation conditions are assessed:
1. **Parametric** — model answers from memorised training knowledge alone (no retrieval)
2. **Web-Augmented** — model uses web search to find relevant excerpts
3. **Document-Access** — model is provided the relevant document sections directly

A fourth condition tests **structured document representation** — converting raw PDF/HTML document content into structured formats (tables, key-value stores) before retrieval — measuring the gain from structured preprocessing. Published March 9, 2026 by Krista Opsahl-Ong, Arnav Singhvi, Jasmine Collins et al. (Databricks; arXiv: 2603.08655).

## Benchmarks / Datasets
- **133 expert-validated questions** over 89,000-page US Treasury Bulletin corpus
- **26M+ numerical values** requiring precise retrieval and cross-document aggregation
- **4 evaluation conditions:** Parametric, Web-Augmented, Document-Access, Structured Document Representation
- **Corpus:** ~100 years of US Treasury regulatory filings (heterogeneous PDF/HTML)

## Key Results

**Average accuracy across frontier models:**

| Condition | Avg Accuracy | Notes |
|---|---|---|
| **Structured Document Access** | **~50%** | +16.1% relative gain over raw document access |
| **Document Access (raw)** | **34.1%** | Best standard condition |
| **Web-Augmented** | **<12%** | Search fails on archival/obscure documents |
| **Parametric** | **<5%** | Near-zero memorisation of archival financial data |

- **Structured document representation** provides a +16.1% relative accuracy gain over raw document access — the single largest improvement factor in the study
- **No frontier model** achieves >60% even with full document access, indicating that long-form numerical reasoning over 89K-page corpora remains unsolved
- Web augmentation fails because archival Treasury documents are poorly indexed or absent from search indexes
- **Parametric accuracy <5%** confirms that no model has meaningfully memorised Treasury Bulletin content, ruling out data contamination

## FoxBrain Relevance
OfficeQA Pro directly models FoxBrain's hardest enterprise document reasoning tasks: answering questions over Foxconn's internal technical specifications, historical procurement records, quality audit archives, and regulatory compliance filings — all of which span thousands of documents and millions of numerical data points. The benchmark's structured document representation finding (+16.1% relative gain) provides a clear deployment strategy: FoxBrain's document QA pipeline should convert internal PDFs, SAP exports, and ERP records into structured key-value or tabular representations before retrieval, rather than passing raw documents to the model. The <5% parametric accuracy finding confirms that FoxBrain cannot rely on memorisation for proprietary Foxconn financial and technical data — structured RAG pipelines are mandatory for enterprise document tasks.

---
*Back to [Main Digest](../README.md)*
