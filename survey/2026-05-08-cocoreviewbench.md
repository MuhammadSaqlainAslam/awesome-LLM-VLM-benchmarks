# CoCoReviewBench: A Completeness- and Correctness-Oriented Benchmark for AI Reviewers (2026)

## Problem
Evaluating AI reviewers is structurally broken: existing metrics measure overlap with human reviews rather than whether the review is correct. Human reviews are unreliable gold standards — they cover only partial issues and sometimes contain errors themselves. This means a high-scoring AI reviewer may be rewarded for mimicking flawed human behaviour rather than for producing genuinely complete and correct technical assessments. No benchmark existed that independently assessed review completeness and correctness, leaving the field unable to determine whether AI reviewers are actually reliable.

## Method
**CoCoReviewBench** (arXiv: 2605.07905, May 2026; accepted ICML 2026) introduces a benchmark of **3,900 papers from ICLR and NeurIPS** with two orthogonal evaluation strategies: (1) **Completeness strengthening** — category-specific benchmark subsets that skip evaluation when human reviews are known to be incomplete, eliminating false negatives; (2) **Correctness strengthening** — using reviewer-author-meta-review discussion threads as expert annotations to filter unreliable reviews and establish ground truth. Four diagnostic tasks evaluate AI reviewer quality along these two independent axes. Reasoning models are found to outperform standard instruction-tuned models as reviewers.

## Benchmarks / Datasets
- 3,900 papers from ICLR and NeurIPS (full benchmark)
- Category-specific completeness subsets (incomplete review exclusion)
- Reviewer-author-meta-review discussion annotations (correctness filter)
- Multiple frontier AI reviewer systems evaluated

## Key Results

| Dimension | Finding |
|---|---|
| AI reviewer correctness | Limited — prone to hallucinations on technical claims |
| Reasoning model advantage | Reasoning models outperform instruction-tuned reviewers |
| Completeness coverage | Category-specific subsets expose coverage gaps hidden in full-set scoring |
| Human review reliability | Human reviews partially incomplete — not a valid universal gold standard |

- **AI reviewers remain limited in correctness and are prone to hallucinations — high overlap with human reviews does not certify review quality**
- The CoCoReviewBench design exposes that standard AI reviewer evaluations reward mimicry of flawed human reviews rather than accuracy, inflating reported performance
- Reasoning models (chain-of-thought enabled) consistently outperform standard instruction-tuned models as peer reviewers
- Reviewer-author-meta-review discussion threads provide the first reliable correctness signal independent of potentially flawed individual human reviews

## Enterprise / Industry Relevance
Foxconn's FoxBrain is increasingly used for automated document review — quality assurance reports, supplier audits, regulatory compliance reviews, and technical specification checks. CoCoReviewBench's central finding — that high review-overlap scores do not imply correct or complete reviews — directly applies: FoxBrain's review outputs should not be validated by comparing them to existing human reviews without first auditing whether those human reviews are themselves complete and correct. For Foxconn's compliance workflows, a FoxBrain reviewer that scores well against an incomplete human reference may miss the same gaps the human missed. The CoCoReviewBench two-axis evaluation strategy (completeness + correctness independently) is a template for building Foxconn-specific FoxBrain review validation protocols that go beyond agreement-with-humans to independent correctness checking against authoritative standards.

---
*Back to [Main Digest](../README.md)*
