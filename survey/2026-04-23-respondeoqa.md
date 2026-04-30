# RespondeoQA: A Benchmark for Bilingual Latin-English Question Answering (2026)

## Problem
Classical Latin is a high-value low-resource language underpinning legal, scientific, and historical scholarship, yet no benchmark had rigorously assessed how well contemporary LLMs handle bilingual Latin-English reasoning — particularly for skill-oriented tasks such as poetic scansion, literary device identification, and grammar parsing. This gap leaves Latin educators and digital humanities researchers without evidence-based model selection guidance.

## Method
**RespondeoQA** (arXiv: 2604.20738, April 23, 2026) is the first comprehensive bilingual Latin-English QA benchmark, comprising approximately 7,800 question-answer pairs drawn from Latin pedagogical materials spanning the 1800s to the present — including exams, trivia competitions, and textbooks. The benchmark distinguishes between knowledge-retrieval QA and skill-oriented QA (scansion, literary device identification, grammar analysis), and evaluates three models — LLaMa 3, Qwen QwQ, and OpenAI's o3-mini — comparing performance when questions are presented in Latin versus in English.

Authors: (authors listed in paper)

## Benchmarks / Datasets
- ~7,800 QA pairs from Latin pedagogical sources (1800s–2026)
- Sources: exams, trivia competitions, and textbooks
- Two question types: knowledge-retrieval and skill-oriented (scansion, literary devices, grammar)
- Bilingual evaluation: questions presented in both Latin and English
- Three models evaluated: LLaMa 3, Qwen QwQ, OpenAI o3-mini

## Key Results

| Model / Condition | Key Finding |
|---|---|
| All models — knowledge retrieval | Relatively stronger performance vs. skill tasks |
| All models — skill-oriented tasks | Consistent performance degradation |
| QwQ — Latin-presented questions | Marginally better than English-presented questions |
| LLaMa 3 & o3-mini — language presentation | Greater task-dependent variation |
| Reasoning models (QwQ, o3-mini) | Modest gains on scansion and literary device identification |

- **All three models perform consistently worse on skill-oriented questions (scansion, literary devices) than on knowledge-retrieval — demonstrating that Latin procedural skill tasks remain a significant frontier challenge for LLMs**
- Qwen QwQ shows a marginal advantage when questions are posed in Latin, suggesting Latin training data coverage meaningfully differs across model families
- Reasoning models (QwQ, o3-mini) produce modest improvements on specific skill tasks over LLaMa 3, but gains are inconsistent across task subtypes
- The 7,800-pair scale and temporal diversity of source materials (spanning 200 years of pedagogy) make RespondeoQA robust against recency bias

## Enterprise / Industry Relevance
While Latin QA is not a core Foxconn use case, RespondeoQA's significance for FoxBrain lies in what it reveals about LLM skill-oriented reasoning in specialised low-resource domains. Foxconn's operations involve numerous specialised technical notations — circuit schematic notation, PCB layout conventions, industrial process control syntax — that share with Latin the property of being skill-oriented rather than purely knowledge-retrieval tasks. The benchmark's finding that reasoning models improve skill tasks inconsistently guides the FoxBrain team toward targeted fine-tuning rather than assuming frontier model capability on procedural technical tasks. The bilingual Latin/English evaluation paradigm also provides a methodology template for evaluating FoxBrain's cross-lingual technical reasoning in Chinese/English industrial contexts.

---
*Back to [Main Digest](../README.md)*
