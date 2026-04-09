# Reasoning Gym: Reasoning Environments for Reinforcement Learning with Verifiable Rewards (2025)

## Problem
Reinforcement Learning with Verifiable Rewards (RLVR) has shown promise for improving LLM reasoning, but existing training environments are too narrow — dominated by mathematics and coding — and lack the breadth, programmatic difficulty control, and verifiability guarantees needed for systematic curriculum learning. There was no unified, open framework providing diverse, scalable, automatically verifiable reasoning tasks for training and evaluating LLMs on general reasoning.

## Method
Reasoning Gym provides **100+ programmatic task generators and verifiers** across 11 reasoning domains. Every task is **algorithmically verifiable** without human judgment — a core design requirement enabling scalable RLVR training. Tasks are parameterised for configurable difficulty, supporting dynamic curricula. The framework uses the **GRPO algorithm** for RL training. Key design principles: large solution spaces (to reward generalisation over memorisation), parametric difficulty control, and automatic verification. Experiments train Qwen2.5-3B-Instruct (~1,500 GPU hours on A6000). The benchmark reveals dramatic performance gaps between easy and hard task configurations for all frontier models. Accepted as **NeurIPS 2025 Spotlight** by Open-Thought, Scale AI, and University College London (arXiv: 2505.24760).

## Benchmarks / Datasets
- **100+ task generators and verifiers** across 11 domains:

| Category | Tasks | Focus |
|---|---|---|
| Algorithms | 32 | Procedural reasoning, computational thinking |
| Games | 18 | Constraint satisfaction, puzzle-solving |
| Cognition + ARC | 14 | Pattern recognition, rule application |
| Logic | 7 | Formal deduction |
| Arithmetic | 11 | Mathematical calculation |
| Algebra | 6 | Symbolic manipulation |
| Graphs | 6 | Discrete structures |
| Geometry | 4 | Spatial reasoning |
| Code | 2 | Programming comprehension |
| Induction | 2 | Sequence inference |

- All tasks: programmatically generated, automatically verifiable, parametric difficulty

## Key Results

**Zero-shot performance (hard configurations):**

| Model | Score |
|---|---|
| **o3-mini** | **63.5%** |
| DeepSeek-R1 | 59.5% |
| Grok 3 Mini | 55.1% |
| Llama 4 Maverick | 41.5% |
| Claude 3.5 Sonnet | 40.3% |

**Difficulty scaling reveals steep drops:** o3-mini's code performance drops 71.9%, graphs 33.8%, geometry 33.1% from easy → hard configurations.

**RLVR training benefits (Qwen2.5-3B trained on Reasoning Gym):**
- Intra-domain: Algebra +11.7pp, Algorithms +7.4pp, Games +3.3pp
- Cross-domain: Training on algorithms → Algebra +29.1pp, Geometry +22.3pp
- Transfer to external benchmarks: MATH +9.7pp, Big-Bench Hard +7.7pp, MMLU-Pro +2.9–6.0pp
- Curriculum learning outperforms fixed-difficulty training by +2.0% to +40.67%

## FoxBrain Relevance
Reasoning Gym's 32 Algorithms and 6 Graphs task generators are directly applicable to FoxBrain's training for supply chain optimisation, scheduling, and BOM dependency reasoning — all structurally equivalent to graph/algorithmic problems. The framework's RLVR approach offers a practical, low-cost (~1,500 GPU hours) training recipe for improving FoxBrain's general reasoning without task-specific human annotation. The cross-domain transfer finding (+29.1pp algebra from algorithm training) suggests that training FoxBrain on manufacturing-specific procedural tasks (assembly sequences, process graphs) would generalise to engineering calculation and optimisation tasks, providing broad capability uplift from a focused training dataset.

---
*Back to [Main Digest](../README.md)*
