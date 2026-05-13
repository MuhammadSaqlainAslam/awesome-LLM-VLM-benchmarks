# LongMemEval-V2: Evaluating Long-Term Agent Memory Toward Experienced Colleagues (2026)

## Problem
Existing agent memory benchmarks evaluate memory against user histories and short interaction traces — they test whether agents can recall what a user previously said, not whether agents can accumulate **domain expertise** about the environments they repeatedly operate in. Production agents working in the same environment over hundreds of sessions should develop the equivalent of an "experienced colleague" who knows environment-specific gotchas, workflow patterns, and dynamic state evolution. No benchmark existed to evaluate this form of environment-specific long-term memory accumulation, leaving developers without a way to measure or compare memory systems for expertise acquisition.

## Method
**LongMemEval-V2** (arXiv: 2605.12493, May 2026) introduces a benchmark of **451 manually curated questions** across **five memory ability dimensions**: static state recall, dynamic state tracking, workflow knowledge, environment gotcha recognition, and premise awareness. Each question is paired with long-horizon agent history trajectories containing **up to 500 trajectories and 115M tokens** of environment interaction history. Two novel memory architectures are proposed and evaluated: **AgentRunbook-R** (RAG-based with specialised knowledge pools for state observations, events, and strategy notes) and **AgentRunbook-C** (trajectory-as-file storage with a coding agent gathering evidence in an augmented sandbox). Both are compared against a RAG baseline and an off-the-shelf coding agent baseline.

## Benchmarks / Datasets
- 451 manually curated questions across 5 memory ability dimensions
- Up to 500 trajectories / 115M tokens per question (long-horizon history)
- 5 memory ability types: static recall / dynamic tracking / workflow / gotchas / premise awareness
- AgentRunbook-R vs. AgentRunbook-C vs. RAG baseline vs. coding agent baseline

## Key Results

| System | Average Accuracy |
|---|---|
| RAG baseline | 48.5% |
| Off-the-shelf coding agent | 69.3% |
| **AgentRunbook-C (proposed)** | **72.5%** |

- **AgentRunbook-C achieves 72.5% vs. RAG baseline 48.5% — a 24 pp improvement — by storing trajectories as files and using a coding agent to gather evidence**
- The 24 pp gap between RAG (48.5%) and AgentRunbook-C (72.5%) demonstrates that standard RAG is insufficient for environment-specific expertise accumulation
- Off-the-shelf coding agents (69.3%) approach the proposed method but fall 3.2 pp short, confirming that specialised memory architecture is required
- Substantial room for improvement remains — even the best system at 72.5% leaves 27.5% of expertise-requiring questions unanswered

## Enterprise / Industry Relevance
Foxconn's FoxBrain agents deployed repeatedly in the same operational environment — factory management systems, quality inspection workflows, supplier coordination portals — should accumulate environment-specific expertise over time. LongMemEval-V2's finding that RAG memory achieves only 48.5% on environment-expertise questions directly predicts FoxBrain performance in long-running deployments: a RAG-based FoxBrain memory system will fail on 51.5% of questions that require environment-specific knowledge built from hundreds of past interactions. For Foxconn's high-value workflows where environment gotcha recognition (edge cases in specific factory ERP systems, supplier portal quirks) is critical to agent reliability, the AgentRunbook-C architecture — trajectories as files, coding agent evidence gathering — provides the best current pathway to operationally useful long-term memory.

---
*Back to [Main Digest](../README.md)*
