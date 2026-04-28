# CT-FineBench: A Diagnostic Fidelity Benchmark for Fine-Grained Evaluation of CT Report Generation (2026)

## Problem
Automated CT report generation systems are evaluated using conventional NLP metrics (BLEU, ROUGE, BERTScore) that measure lexical overlap rather than clinical correctness. These metrics cannot detect fine-grained factual errors in disease-oriented attributes such as lesion location, size, and morphology — the exact errors that cause harm in clinical practice. A benchmark was needed that evaluates CT report generation based on diagnostic fidelity rather than text similarity.

## Method
**CT-FineBench** (arXiv: 2604.24001, April 28, 2026) introduces a diagnostic fidelity benchmark for evaluating CT report generation using a question-answering approach that targets fine-grained, disease-oriented attributes — location, size, morphology, and clinical impression. Built from the CT-RATE and Merlin CT datasets, the benchmark measures factual consistency at the attribute level, correlating scores with expert clinical judgment and demonstrating substantially higher sensitivity to fine-grained clinical errors than conventional metrics.

## Benchmarks / Datasets
- Built from CT-RATE and Merlin CT datasets
- Fine-grained QA approach targeting disease-oriented attributes: location / size / morphology / clinical impression
- Expert clinical assessment as ground truth for correlation validation
- Sensitivity analysis against specific types of clinical errors
- First benchmark specifically targeting diagnostic fidelity in CT report generation

## Key Results

| Evaluation Dimension | Key Finding |
|---|---|
| Correlation with expert clinical judgment | Superior to all prior metrics |
| Sensitivity to fine-grained factual errors | Substantially more sensitive than lexical metrics |
| Attribute-level evaluation | Location, size, morphology errors captured independently |
| Clinical impression scoring | Clinically relevant assessment vs. text-level proxy |

- **CT-FineBench demonstrates superior correlation with expert clinical judgment compared to prior metrics — lexical overlap metrics are insufficient for evaluating clinical AI report generation**
- The QA-based approach is substantially more sensitive to fine-grained factual errors (wrong lesion location, incorrect size) that conventional metrics miss entirely
- Attribute-level evaluation provides diagnostic signal: which types of errors a model makes, not just aggregate quality
- The benchmark establishes the standard for evaluating medical report generation systems before clinical deployment

## FoxBrain Relevance
While CT report generation is a medical domain application, CT-FineBench's core methodology — using QA-based fine-grained attribute evaluation instead of lexical overlap metrics — is directly applicable to FoxBrain's structured report generation tasks. Foxconn generates quality inspection reports, engineering assessment reports, and supplier audit reports where attribute-level factual accuracy (defect location, measurement values, compliance status) matters far more than text fluency. Adopting CT-FineBench's QA-based evaluation methodology for FoxBrain's report generation pipeline would provide more reliable quality signals than BLEU/ROUGE-style metrics currently used in many NLG evaluation setups.

---
*Back to [Main Digest](../README.md)*
