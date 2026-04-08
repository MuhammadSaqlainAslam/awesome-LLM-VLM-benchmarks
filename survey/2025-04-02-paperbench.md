# PaperBench: Evaluating AI's Ability to Replicate AI Research (2025)

## Problem
Existing AI capability evaluations lack tasks that measure the complete pipeline of AI research — understanding a novel contribution, writing code from scratch to implement it, and executing experiments to reproduce results. PaperBench asks whether AI agents can independently replicate state-of-the-art AI research papers end-to-end, from reading a PDF to producing matching experimental results.

## Method
Agents are given the full paper PDF for each of **20 ICML 2024 Spotlight/Oral papers** and must independently build a codebase and execute experiments without access to the original code. Each paper has a **hierarchical rubric co-developed with the original paper's authors**, decomposing replication into leaf-node requirements across three types: Code Development, Execution, and Results Match. Two agent scaffolds are evaluated: **BasicAgent** (single-pass, 12-hour cap) and **IterativeAgent** (iterative refinement, 12- or 36-hour cap). Grading uses **JudgeEval** — an LLM-based automatic rubric grader (o3-mini-high, F1=0.83, ~$66/paper). A lighter variant, **PaperBench Code-Dev**, strips execution requirements for faster, cheaper evaluation. A human baseline was established with 8 ML PhD students from Berkeley, CMU, Cambridge, Cornell, Columbia, Purdue, TU Wien, and UMass Amherst. Accepted at **ICML 2025** by **OpenAI** (arXiv: 2504.01848).

## Benchmarks / Datasets
- **20 ICML 2024 Spotlight/Oral papers** across 12 ML research topic areas
- **8,316 total gradable rubric leaf nodes** (avg. 415.8/paper; range: 69–2,551)
- **3 requirement types:** Code Development, Execution, Results Match
- **2 agent scaffolds:** BasicAgent (12h) and IterativeAgent (12h/36h)
- **646 total agent runs** conducted
- **Human baseline:** 8 ML PhD participants, 48-hour window, 3-paper subset

## Key Results

**BasicAgent (12-hour limit):**

| Model | Avg. Score |
|---|---|
| **Claude 3.5 Sonnet (new)** | **21.0% ± 0.8** |
| o1-high | 13.2% ± 0.3 |
| DeepSeek-R1 | 6.0% ± 0.3 |
| GPT-4o | 4.1% ± 0.1 |
| Gemini 2.0 Flash | 3.2% ± 0.2 |
| o3-mini-high | 2.6% ± 0.2 |

**IterativeAgent:**

| Model | Avg. Score | Time Limit |
|---|---|---|
| **o1-high** | **26.0% ± 0.3** | 36 hours |
| o1-high | 24.4% ± 0.7 | 12 hours |
| Claude 3.5 Sonnet | 16.1% ± 0.1 | 12 hours |
| o3-mini-high | 8.5% ± 0.8 | 12 hours |

**Human baseline (3-paper subset, 48h window): 41.4%** — AI does not yet match human PhD-level replication ability.

**Performance by requirement type (best models):**
- Code Development: o1 Iterative reaches 43.3% — partial code replication is achievable
- Execution: o1 Iterative 7.4% — running code to completion remains very difficult
- Results Match: ~0–1.4% across all models — matching actual numerical results is nearly unsolved

## FoxBrain Relevance
PaperBench directly probes FoxBrain's R&D acceleration potential: can it read a technical paper, write the implementation code, and reproduce the results autonomously? The 21% Code Development ceiling (Claude 3.5 Sonnet) with near-0% Results Match confirms that FoxBrain can draft code scaffolding from papers but cannot yet be trusted to reproduce validated experimental results without human oversight. For Foxconn's R&D teams, FoxBrain is best deployed as a first-pass code drafting assistant — not as an autonomous research replication agent. The 3-type rubric (Code Dev → Execution → Results Match) maps directly to a staged FoxBrain deployment gate: code review → runtime validation → numerical verification.

---
*Back to [Main Digest](../README.md)*
