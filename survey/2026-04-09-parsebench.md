# ParseBench: Evaluating Document Parsing for AI Agents (2026)

## Problem
Modern AI agents rely heavily on document parsing to extract structured information from enterprise documents (PDFs, insurance forms, financial reports, government filings). Existing parsing benchmarks use text-similarity metrics (BLEU, ROUGE, exact match) that fail to capture *semantic correctness* — a parsed table with reformatted but equivalent values may score poorly under text-similarity despite being functionally correct. No benchmark evaluated parsing across the five distinct capability dimensions that enterprise agents actually require: table extraction, chart data reading, content faithfulness, semantic formatting, and visual grounding. This left a critical blind spot for teams deploying document AI in production.

## Method
**ParseBench** (arXiv: 2604.08538, April 9, 2026) curates **~2,000 human-verified enterprise document pages** from insurance, finance, and government domains — the three highest-volume sectors for document AI deployment. Evaluation spans **five capability dimensions** using semantic correctness rather than text-similarity:

1. **Table Parsing** — extracting structured tabular data with correct row/column alignment
2. **Chart Data Extraction** — reading numeric values from bar, line, and pie charts
3. **Content Faithfulness** — preserving factual accuracy without hallucination or omission
4. **Semantic Formatting** — maintaining document structure (headings, sections, lists) in output
5. **Visual Grounding** — correctly attributing extracted content to specific page regions

**14 parsing methods evaluated**, including proprietary APIs (LlamaParse, Azure Document Intelligence), open-source models (Marker, Nougat), and multimodal LLM-based approaches.

Authors: Boyang Zhang, Sebastián G. Acosta, Preston Carlson, Sacha Bron, Pierre-Loïc Doulcet, Simon Suo.

## Benchmarks / Datasets
- **~2,000 human-verified enterprise document pages** (insurance, finance, government)
- **5 capability dimensions:** Table Parsing, Chart Extraction, Content Faithfulness, Semantic Formatting, Visual Grounding
- **14 methods evaluated** (proprietary APIs, open-source, LLM-based)
- **Metric:** Semantic correctness per dimension (not text-similarity)

## Key Results

| Method | Overall Score | Notes |
|---|---|---|
| **LlamaParse Agentic** | **Highest overall** | Best across most dimensions |
| Azure Document Intelligence | Strong on tables | Weak on chart extraction |
| Marker (open-source) | Competitive | Strong on formatting |
| Nougat | Weak on charts | Strong on academic PDFs |
| Multimodal LLM-based | Variable | Best on visual grounding |

- **LlamaParse Agentic achieves the highest overall score** but **no method performs consistently well across all five dimensions** — the choice of parser must be matched to the document type and target dimension
- **Chart data extraction** is the weakest dimension across all tested methods — even best-in-class tools fail on complex multi-series charts
- **Visual grounding** (attributing content to page regions) is uniquely well-served by multimodal LLM approaches vs. traditional parsers
- Open-source tools lag significantly on financial document tables with merged cells and irregular layouts

## FoxBrain Relevance
ParseBench is directly applicable to FoxBrain's document AI pipeline: Foxconn processes high volumes of supplier invoices, quality audit reports, engineering specifications, and regulatory compliance filings — all of which require accurate multi-dimensional parsing. The benchmark's finding that no single parser excels on all five dimensions motivates a hybrid pipeline strategy for FoxBrain: use LlamaParse Agentic as the primary parser with targeted fallbacks to multimodal LLM approaches for charts and visual grounding tasks. The semantic correctness evaluation methodology should replace BLEU/ROUGE in FoxBrain's internal document QA evaluation to avoid rewarding formally similar but factually incorrect extractions.

---
*Back to [Main Digest](../README.md)*
