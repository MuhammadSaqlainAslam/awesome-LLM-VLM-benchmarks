# QuanBench+: A Unified Multi-Framework Benchmark for LLM Quantum Code Generation (2026)

## Problem
Quantum computing is transitioning from research to production deployment, with major frameworks (Qiskit, PennyLane, Cirq) developing divergent APIs and paradigms. LLMs are increasingly used to assist quantum software development, but no benchmark evaluated quantum code generation across all three major frameworks simultaneously with consistent evaluation methodology. Prior benchmarks were single-framework, used deterministic exact-match evaluation inappropriate for probabilistic quantum outputs, and did not test feedback-based repair — the iterative debugging workflow that characterises real quantum software development.

## Method
**QuanBench+** (arXiv: 2604.08570, March 25, 2026) constructs **42 aligned tasks** designed to be equivalent in difficulty across **Qiskit, PennyLane, and Cirq**, covering quantum algorithms, gate decomposition, state preparation, and circuit optimisation. Key methodological innovation: **KL-divergence-based acceptance criterion** for evaluating probabilistic quantum circuit outputs — rather than exact output matching, solutions are accepted if the output probability distribution is within a defined KL-divergence threshold of the target distribution. A **feedback-based repair** protocol tests iterative self-correction: models receive execution error messages and attempt to fix their code, simulating real-world quantum development workflows. Authors: Ali Slim, Haydar Hamieh, Jawad Kotaich, Yehya Ghosn, Mahdi Chehimi, Ammar Mohanna, Hasan Abed Al Kader Hammoud, Bernard Ghanem.

## Benchmarks / Datasets
- **42 aligned tasks** across Qiskit, PennyLane, and Cirq (126 total evaluation instances)
- **Task types:** Quantum algorithms, gate decomposition, state preparation, circuit optimisation
- **Evaluation:** KL-divergence-based acceptance for probabilistic outputs (not exact match)
- **Feedback repair protocol:** Models given error messages for iterative self-correction
- **Metrics:** Pass@1, Pass@5, Pass@1-after-repair

## Key Results

| Framework | Best Pass@1 (1-shot) | Best Pass@1 (after repair) | Gap |
|---|---|---|---|
| **Qiskit** | **59.5%** | **83.3%** | +23.8 pp |
| **Cirq** | **54.8%** | **76.2%** | +21.4 pp |
| **PennyLane** | **42.9%** | **66.7%** | +23.8 pp |

- **Feedback-based repair provides +21–24 percentage points** across all frameworks — iterative self-correction is the single largest improvement factor in quantum code generation
- **PennyLane is consistently the hardest framework** for all models (lowest 1-shot and post-repair scores), reflecting its more abstract, functional programming paradigm
- **Qiskit benefits most from model familiarity** (most training data), confirming framework popularity in training corpora influences quantum code quality
- All models show framework-specific strengths — no single LLM dominates all three frameworks simultaneously

## FoxBrain Relevance
QuanBench+ is forward-looking for Foxconn's quantum computing roadmap: as quantum hardware matures for optimisation problems in supply chain, manufacturing scheduling, and materials simulation, FoxBrain will need to generate and debug quantum circuits across multiple frameworks. The 83.3% post-repair Qiskit performance establishes a realistic near-term ceiling — FoxBrain can be a useful quantum code assistant with iterative feedback, but not yet an autonomous quantum programmer. The KL-divergence evaluation methodology is immediately applicable to FoxBrain's quantum testing pipeline: replace binary pass/fail with distribution-similarity acceptance for probabilistic quantum outputs. Prioritise Qiskit integration first (highest performance) before PennyLane (hardest).

---
*Back to [Main Digest](../README.md)*
