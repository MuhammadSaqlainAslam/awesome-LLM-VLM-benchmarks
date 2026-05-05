# AcademiClaw: When Students Set Challenges for AI Agents (2026)

## Problem
AI agent benchmarks are predominantly authored by researchers who select tasks solvable by current systems — creating a systematic ceiling where benchmarks are obsolete by the time they are published. Real-world expert-level tasks that students encounter in university coursework, research, and competitions represent a more genuine and adversarially diverse challenge: they are not pre-filtered for AI solvability, they span long-horizon multi-step workflows, and they require domain-specific expertise across a wide range of disciplines. No benchmark had used student-generated real academic tasks to evaluate frontier AI agents.

## Method
**AcademiClaw** (arXiv: 2605.02661, May 2026) is a bilingual benchmark curated from **230 student submissions**, yielding **80 complex long-horizon tasks** across **25+ professional domains** — ranging from olympiad-level mathematics to GPU-intensive machine learning workflows. Notably, **16 tasks require CUDA GPU execution inside Docker sandboxes**, testing agent capability for resource-intensive computational tasks in isolated environments. Six frontier language models are evaluated. The benchmark is bilingual (English and Chinese) and emphasises genuine academic difficulty rather than AI-friendly task design.

## Benchmarks / Datasets
- 80 complex long-horizon tasks from 230 student submissions
- 25+ professional domains (mathematics, ML, science, engineering, etc.)
- 16 tasks requiring CUDA GPU execution in Docker sandboxes
- Bilingual: English and Chinese
- 6 frontier models evaluated
- Ground truth: verified student solutions

## Key Results

| Metric | Result |
|---|---|
| Best frontier model pass rate | **55%** |
| Task domains | 25+ professional domains |
| GPU-execution tasks | 16 (Docker sandboxes) |
| Capability boundary type | Sharp — domain-dependent cliffs |

- **Best frontier model achieves only 55% pass rate on student-generated academic tasks — nearly half of genuine university-level challenges remain unsolved by frontier AI agents**
- Sharp capability boundaries identified across task domains: agents perform well in some domains and collapse entirely in others rather than showing gradual degradation
- Divergent behavioural patterns across models: different frontier models fail on different task subsets, suggesting complementary rather than uniform capability gaps
- GPU-execution tasks (CUDA in Docker) expose a rarely tested capability: agents must not just generate code but correctly orchestrate resource-intensive computational environments

## Enterprise / Industry Relevance
Foxconn's most demanding FoxBrain use cases — computational materials simulation, advanced process optimisation, research literature synthesis, and engineering design analysis — are analogous to the academic tasks where frontier models achieve only 55%. This benchmark directly challenges FoxBrain teams who may assume that frontier model capabilities demonstrated on clean benchmarks transfer to complex, long-horizon professional tasks. The sharp domain-specific capability boundaries are particularly important: FoxBrain's capability must be evaluated domain by domain (manufacturing engineering vs. supply chain finance vs. regulatory compliance), not assumed uniform across Foxconn's enterprise breadth. The Docker/CUDA task design is also a template for FoxBrain's engineering computation workflows: agents must be tested in sandboxed execution environments with realistic resource constraints, not just evaluated on code generation quality.

---
*Back to [Main Digest](../README.md)*
