# HalluScan: A Systematic Benchmark for Detecting and Mitigating Hallucinations in Instruction-Following LLMs (2026)

## Problem
Hallucination detection methods for instruction-following LLMs proliferate without systematic head-to-head comparison — each paper proposes a new detector evaluated on different models, domains, and metrics, making it impossible to choose the right detection approach for a given deployment. No framework existed to compare detection methods, model families, and domains under controlled conditions, or to quantify the cost-accuracy tradeoff of different detection strategies.

## Method
**HalluScan** (arXiv: 2605.02443, May 2026) benchmarks **72 configurations** spanning **6 detection methods**, **4 open-weight model families**, and **3 diverse domains**. Detection methods compared include NLI verification, RAG-Aided Verification (RAV), and others. A new unified metric — **HalluScore** — is introduced, achieving Pearson correlation of r = 0.41 with human expert judgments. An **Adaptive Detection Routing** strategy is proposed that selects the cheapest detection method capable of achieving target reliability, delivering 2.0× cost reduction with only 0.1% AUROC degradation. Error cascade decomposition is applied across domains to trace hallucination propagation paths.

## Benchmarks / Datasets
- 72 configurations: 6 detection methods × 4 model families × 3 domains
- HalluScore metric (Pearson r = 0.41 with human expert judgments)
- Adaptive Detection Routing evaluation
- Error cascade decomposition across domains

## Key Results

| Detection Method | AUROC |
|---|---|
| NLI Verification | **0.88** (best) |
| RAG-Aided Verification (RAV) | 0.66 (second) |
| Other methods | Lower |

| Strategy | Cost vs. Baseline | AUROC Loss |
|---|---|---|
| Adaptive Detection Routing | 2.0× cheaper | 0.1% only |

- **NLI Verification achieves the highest AUROC of 0.88 — the most reliable hallucination detection method across all 72 tested configurations**
- Adaptive Detection Routing delivers 2.0× cost reduction with only 0.1% AUROC degradation — detection can be made production-economical without meaningfully sacrificing reliability
- HalluScore (r = 0.41 with human judgments) provides the first unified metric enabling cross-method, cross-domain hallucination detection comparison
- Error cascade analysis reveals how hallucinations in one step propagate to dependent outputs, with domain-specific patterns requiring domain-tailored detection strategies

## Enterprise / Industry Relevance
FoxBrain deployments generating factual content — supplier reports, regulatory filings, engineering assessments, customer communications — require hallucination detection as a production control. HalluScan's finding that NLI Verification achieves 0.88 AUROC makes it the evidence-backed default detection choice for FoxBrain's output verification pipeline. The Adaptive Detection Routing strategy is directly actionable: for low-stakes FoxBrain outputs (internal summaries, draft reports), route to cheaper detection methods; for high-stakes outputs (customer-facing documents, compliance filings), route to NLI verification. The 2.0× cost reduction means hallucination detection can be applied to high volumes of FoxBrain outputs without doubling inference costs. The error cascade decomposition methodology also provides a template for Foxconn to trace how hallucinations in FoxBrain's first-step extraction propagate into downstream pipeline outputs.

---
*Back to [Main Digest](../README.md)*
