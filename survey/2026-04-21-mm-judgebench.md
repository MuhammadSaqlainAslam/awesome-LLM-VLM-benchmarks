# Lost in Translation: Do LVLM Judges Generalize Across Languages? (2026)

## Problem
Automatic reward models based on large vision-language models (LVLMs) are increasingly used as judges in RLHF pipelines and evaluation frameworks, but their cross-lingual consistency has never been systematically tested. If LVLM judges exhibit different preferences and reliability across languages, then model rankings produced by these evaluators are language-biased, making multilingual AI development and fairness assessment fundamentally unreliable.

## Method
**MM-JudgeBench** (arXiv: 2604.19405, April 21, 2026) is the first large-scale multilingual and multimodal judge evaluation benchmark, comprising over 60,000 pairwise preference instances spanning 25 typologically diverse languages. The benchmark includes two complementary evaluation subsets and tests 22 LVLMs (15 open-source, 7 proprietary) as judge models. The study reveals that model size and architecture are poor predictors of multilingual judge consistency.

Authors: Md Tahmid Rahman Laskar, Mohammed Saidul Islam, Mir Tafseer Nayeem, Amran Bhuiyan, Mizanur Rahman, Shafiq Joty, Enamul Hoque, Jimmy Huang

## Benchmarks / Datasets
- 60,000+ pairwise preference instances across 25 typologically diverse languages
- Two complementary evaluation subsets
- 22 LVLMs evaluated as judge models (15 open-source, 7 proprietary)
- Key metric: cross-lingual performance variance and judge consistency

## Key Results

| Finding | Detail |
|---|---|
| Models tested | 22 LVLMs (15 OS + 7 proprietary) |
| Languages covered | 25 typologically diverse |
| Cross-lingual variance | Substantial across all models |
| Size/architecture as predictor | Poor predictor of multilingual robustness |

- **Even state-of-the-art LVLM judges exhibit substantial cross-lingual performance variance, undermining their reliability as multilingual reward models**
- Model scale and architecture do not reliably predict judge consistency across languages — a larger model is not necessarily a more language-neutral judge
- The benchmark reveals that current LVLM judges are implicitly English-biased, skewing evaluation results for non-English content

## FoxBrain Relevance
Foxconn's global operations span manufacturing facilities in China, Taiwan, India, Vietnam, Mexico, and Eastern Europe, requiring FoxBrain to handle multilingual enterprise documents, supplier communications, and quality reports in Mandarin, Hindi, Vietnamese, Spanish, and other languages. If FoxBrain uses an LVLM judge for reward modeling or automated QA evaluation, MM-JudgeBench is essential for auditing whether that judge provides consistent quality signals across all languages encountered in Foxconn's global supply chain. The finding that large model size does not guarantee cross-lingual judge reliability means FoxBrain's evaluation pipeline must be explicitly validated on each target language rather than assuming English benchmark performance generalizes.

---
*Back to [Main Digest](../README.md)*
