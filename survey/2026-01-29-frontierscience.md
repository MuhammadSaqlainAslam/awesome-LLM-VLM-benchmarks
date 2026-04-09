# FrontierScience: Evaluating AI's Ability to Perform Expert-Level Scientific Tasks (2026)

## Problem
Existing science benchmarks (GPQA, MMLU, SciBench) have been nearly saturated by frontier models, making them ineffective at differentiating between top-tier systems or tracking genuine progress in scientific reasoning. There was no benchmark specifically designed for the two hardest tiers of science problem-solving: international olympiad-level competition problems and open-ended, PhD-level research sub-problems — the two regimes most relevant to whether AI can function as a genuine scientific collaborator.

## Method
**FrontierScience** (OpenAI, arXiv: 2601.21165, January 29, 2026) constructs a 160-question expert-level science benchmark across two distinct tracks, authored by international olympiad medalists and PhD-level scientists to ensure genuine novelty and contamination resistance.

**Olympiad Track (100 questions):**
- Problems at IPhO, IChO, and IBO (International Physics/Chemistry/Biology Olympiad) standard
- Created by 42 international olympiad medalists and coaches (108 total medals: 45 gold, 37 silver, 26 bronze)
- Structured problems requiring precise numeric or algebraic answers
- Evaluation: expression/numeric equivalency matching, averaged over 20 independent trials

**Research Track (60 questions):**
- PhD-level sub-problems drawn from active scientific research
- Equally split: 20 physics, 20 chemistry, 20 biology
- Created by 45 PhD-level scientists (postdocs, professors, doctoral candidates)
- Evaluation: 10-point rubric; ≥7/10 required to count as success, averaged over 30 independent trials
- Grading performed by GPT-5 at high reasoning effort

Authors: Miles Wang, Robi Lin, Kat Hu, Joy Jiao, Neil Chowdhury, Ethan Chang, Tejal Patwardhan (OpenAI).

## Benchmarks / Datasets
- **160 questions total:** 100 Olympiad + 60 Research
- **Disciplines:** Physics, Chemistry, Biology (both tracks)
- **Tracks:** Olympiad (structured, competition) vs. Research (open-ended, PhD-level)
- **Metrics:** Exact/fuzzy expression matching (Olympiad); 10-point rubric ≥7/10 (Research)
- All problems novel and unpublished — contamination-resistant by design

## Key Results

| Model | Olympiad | Research |
|---|---|---|
| **GPT-5.2** (xhigh reasoning effort) | **77.1%** | **25.2%** |
| Gemini 3 Pro (high reasoning effort) | 76.1% | 12.4% |
| Claude Opus 4.5 | — | 17.5% |
| Grok 4 | — | 15.9% |

- **~52-point gap** between Olympiad and Research tracks for the best model (77.1% vs. 25.2%) — structured competition problems remain far more tractable than open-ended research reasoning
- **Test-time compute scaling** substantially helps: GPT-5.2 improved from 67.5% → 77.1% (Olympiad) and 18% → 25% (Research) with more reasoning tokens
- **Chemistry** is the easiest subject across both tracks; **Biology** is the hardest on the Research track
- Recent models have nearly saturated GPQA Diamond (>90%), confirming FrontierScience fills a critical difficulty gap above existing benchmarks

## FoxBrain Relevance
FrontierScience defines the frontier of scientific reasoning capability — directly relevant to FoxBrain's R&D applications in materials science, process chemistry, and engineering physics at Foxconn. The 52-point Olympiad–Research gap highlights a critical weakness: FoxBrain may perform competently on structured formula derivations but fail on ill-defined, multi-step research problems resembling real R&D tasks. The Research track's 10-point rubric methodology (≥7/10 for success) provides a template for evaluating FoxBrain on internal engineering problem-solving tasks where partial credit and reasoning quality matter more than exact-match correctness. Priority: run FoxBrain on the Olympiad track to establish a baseline before targeting the more demanding Research track problems.

---
*Back to [Main Digest](../README.md)*
