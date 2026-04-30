# SkillLearnBench: Benchmarking Continual Learning for Agent Skill Generation (2026)

## Problem
LLM agents increasingly rely on externally stored skills to handle complex tasks, but no benchmark had systematically evaluated whether continual skill learning methods actually improve agent performance over time on real-world tasks. The field lacked a standardised testbed that spans diverse sub-domains and measures skill quality, execution trajectories, and final task outcomes simultaneously.

## Method
**SkillLearnBench** (arXiv: 2604.20087, April 21, 2026) is the first benchmark specifically designed to evaluate continual skill learning for LLM agents on real-world tasks. It comprises 20 verified, skill-dependent tasks across 15 sub-domains derived from a real-world skill taxonomy. Continual learning methods tested include one-shot skill generation, self-feedback, teacher feedback, and skill creator paradigms, evaluated across three granularities: skill quality, execution trajectory, and task outcome.

Authors: Shanshan Zhong, Yi Lu, Jingjie Ning, Yibing Wan, Lihan Feng, Yuyi Ao, Leonardo F. R. Ribeiro, Markus Dreyer, Sean Ammirati, Chenyan Xiong

## Benchmarks / Datasets
- 20 verified skill-dependent tasks spanning 15 real-world sub-domains
- Three evaluation levels: skill quality, execution trajectory, task outcome
- Continual learning methods: one-shot, self-feedback, teacher feedback, skill creator
- Open-source code and data available on GitHub
- Multiple LLM backbones evaluated across methods

## Key Results

| Continual Learning Method | Key Finding |
|---|---|
| All methods vs. no-skill baseline | Consistent improvement over baseline |
| Self-feedback alone | Causes recursive drift on open-ended tasks |
| External feedback (teacher) | Drives genuine improvement vs. self-feedback |
| No single method | Dominates across all tasks and LLMs |

- **All continual learning methods improve over the no-skill baseline, but no single method leads consistently across all 20 tasks and LLM backends**
- Stronger LLMs do not reliably produce better skills; model capability and skill generation quality are partially decoupled
- External feedback is essential; self-feedback alone causes recursive drift that degrades performance on open-ended tasks

## Enterprise / Industry Relevance
Manufacturing automation at Foxconn increasingly relies on agentic systems that must learn and reuse skills across production workflows — from automated test routines to equipment calibration procedures. SkillLearnBench directly measures whether FoxBrain agents can accumulate reusable skills over time without catastrophic forgetting, which is critical for Foxconn's goal of deploying adaptive AI agents across changing production lines. The benchmark's 15 sub-domain structure mirrors the diversity of Foxconn's factory operations, where agents must handle tasks ranging from component inspection to logistics coordination. The finding that external teacher feedback outperforms self-feedback guides the FoxBrain team toward human-in-the-loop skill validation architectures.

---
*Back to [Main Digest](../README.md)*
