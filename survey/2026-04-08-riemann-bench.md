# Riemann-Bench: Research-Level Mathematics Beyond Olympiad Problems (2026)

## Problem
Existing mathematical benchmarks — AIME, IMO, OlympiadBench, OMNI-MATH — have been increasingly saturated by frontier models, with some achieving >90% on problems that were once considered expert-level. This performance creates a false impression of near-human mathematical capability. In reality, the problems that professional mathematicians actually struggle with — open-ended research-level questions requiring weeks of focused effort — remain completely untested. There was no benchmark targeting the hardest tier of mathematical reasoning: problems authored by Ivy League professors and IMO medalists that routinely took their own authors weeks to solve.

## Method
**Riemann-Bench** (arXiv: 2604.06802, April 8, 2026) curates **25 research-level mathematical problems** authored exclusively by Ivy League mathematics professors and PhD-holding IMO medalists. Each problem was chosen because it "routinely took its authors weeks to solve independently." Models are given unrestricted access to coding tools, search engines, and open-ended reasoning — matching the conditions under which human mathematicians work on hard problems.

Evaluation design:
- **100 independent runs per problem** to estimate true pass rate with statistical reliability
- **Programmatic verifiers** for closed-form solutions (no LLM-as-judge for mathematical correctness)
- **Private benchmark** — problems are not publicly released to prevent contamination
- Problems span advanced algebra, analysis, number theory, combinatorics, and topology at research frontier level

Authors: Suhaas Garre, Erik Knutsen, Sushant Mehta, Edwin Chen.

## Benchmarks / Datasets
- **25 expert-curated problems** (private; contamination-resistant)
- **Authors:** Ivy League professors + PhD-holding IMO medalists
- **Tools allowed:** Coding, search, open-ended reasoning (no constraints)
- **Evaluation:** 100 runs/problem; programmatic verifiers for closed-form solutions
- **Metric:** Pass rate per problem; aggregate pass rate across 25 problems

## Key Results

| Model | Pass Rate | Notes |
|---|---|---|
| All frontier models | **< 10%** | No exceptions |
| Best model | < 10% | Not disclosed |
| Human expert (author) | ~100% (given weeks) | Baseline |

- **Every tested frontier model scores below 10%** on research-level mathematics — the hardest capability gap in the mathematical reasoning landscape
- Stark contrast to olympiad benchmarks where frontier models now exceed 70-90%
- The gap between olympiad-level (~77% on FrontierScience Olympiad track) and research-level (<10%) performance is the defining result: current AI cannot do the mathematics that professional mathematicians do
- Tool access (coding + search) does not close the gap — models fail even with unrestricted resources

## FoxBrain Relevance
Riemann-Bench establishes the hard ceiling of mathematical reasoning capability for any LLM system — including FoxBrain. For Foxconn R&D applications involving advanced optimisation theory, materials science modelling, or process simulation mathematics, the <10% pass rate confirms that FoxBrain cannot be trusted as an autonomous mathematical reasoner on novel research problems. However, the benchmark's tool-access design (coding + search permitted) mirrors FoxBrain's own agentic deployment context. Recommended: use Riemann-Bench's programmatic-verifier methodology as a template for FoxBrain engineering math evaluations, and set realistic expectations: FoxBrain can accelerate structured derivations and formula lookups, but cannot generate novel mathematical proofs on hard problems.

---
*Back to [Main Digest](../README.md)*
