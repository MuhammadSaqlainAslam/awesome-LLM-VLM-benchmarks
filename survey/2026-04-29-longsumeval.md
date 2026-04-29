# LongSumEval: Question-Answering Based Evaluation and Feedback-Driven Refinement for Long Document Summarization (2026)

## Problem
Evaluating summaries of long documents is a persistent challenge: conventional metrics (ROUGE, BERTScore) measure text overlap rather than information coverage and factual fidelity, producing scores that correlate poorly with human judgments. For enterprise and scientific use cases where summaries of long reports or documents must be accurate and complete, there is no reliable automated framework that both evaluates quality and provides actionable feedback for iterative improvement.

## Method
**LongSumEval** (arXiv: 2604.25130, April 29, 2026) introduces a framework that evaluates long document summaries through generated question-answering pairs, measuring both answerability (whether key information is present) and factual alignment (whether present information is correct). The framework generates interpretable scores and structured feedback identifying specific coverage gaps and inconsistencies. It is tested across seven summarisation benchmarks, demonstrating substantially stronger agreement with human judgments than established metrics, and enables self-refinement of summaries using the structured feedback as executable instructions.

## Benchmarks / Datasets
- Evaluated across seven summarisation benchmarks
- QA-based evaluation measuring answerability + factual alignment
- Structured feedback generation for coverage gaps and inconsistencies
- Self-refinement loop: feedback used as executable improvement instructions
- Human judgment correlation compared against established metrics (ROUGE, BERTScore, etc.)

## Key Results

| Evaluation Dimension | Key Finding |
|---|---|
| Human judgment agreement | Substantially stronger than ROUGE, BERTScore, and other established metrics |
| Coverage gap detection | Interpretable identification of missing key information |
| Factual alignment detection | Identifies inconsistencies between summary and source document |
| Self-refinement quality | Significant improvement without retraining |
| Generalisation | Validated across 7 diverse summarisation benchmarks |

- **LongSumEval's QA-based approach shows substantially stronger agreement with human judgments than established metrics across 7 benchmarks — conventional metrics are poor proxies for summary quality**
- The framework bridges evaluation and generation: structured feedback serves directly as executable refinement instructions, enabling iterative quality improvement without retraining
- Both answerability and factual alignment are necessary — a summary can mention key topics (answerability) while still being factually wrong (alignment failure)
- The generalisation across 7 diverse benchmarks validates the approach as a robust alternative to surface-level metrics

## FoxBrain Relevance
Foxconn generates and consumes large volumes of long documents — engineering specifications, audit reports, supplier contracts, regulatory filings, and meeting transcripts — for which reliable automated summarisation is a high-value FoxBrain capability. LongSumEval's finding that conventional metrics correlate poorly with human quality judgment means FoxBrain's summary evaluation pipeline must adopt QA-based fidelity measurement rather than ROUGE/BERTScore. More importantly, the self-refinement loop — using structured feedback to iteratively improve summaries — provides a production-ready architecture for FoxBrain's document summarisation pipeline that does not require retraining and can be applied to any document domain relevant to Foxconn operations.

---
*Back to [Main Digest](../README.md)*
