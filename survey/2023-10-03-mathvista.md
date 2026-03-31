# MathVista: Evaluating Mathematical Reasoning of Foundation Models in Visual Contexts (2023)

## Problem
Math reasoning benchmarks and visual understanding benchmarks had evolved independently, leaving untested the compositional challenge of mathematical reasoning in visual contexts. Models that excel at text-based math and at image captioning still fail when required to jointly parse a figure and perform multi-step mathematical reasoning on its content.

## Method
MathVista combines challenges from 28 existing multimodal math datasets with 3 newly created datasets (IQTest for abstract pattern reasoning, FunctionQA for mathematical function graphs, and PaperQA for scientific figure QA), yielding 6,141 examples spanning geometry, algebra, statistics, IQ-style puzzles, and paper figure analysis. It evaluates fine-grained visual understanding jointly with compositional mathematical reasoning. Published at ICLR 2024.

## Benchmarks / Datasets
- **MathVista:** 6,141 examples from 28 existing + 3 new datasets.
- **New Datasets:** IQTest (abstract/IQ reasoning), FunctionQA (function graphs), PaperQA (scientific figures).
- **Task Types:** Figure QA, geometry, algebra, statistics, abstract reasoning, scientific paper figures.
- **Metrics:** Overall accuracy; fine-grained accuracy by task type and visual context type.
- **GitHub:** https://github.com/lupantech/MathVista | **Project:** https://mathvista.github.io/

## Key Results
At release, **GPT-4V achieved 49.9% accuracy** — the best model result — still **10.4 percentage points below human performance** (60.3%). Models with strong text-math ability do not automatically transfer that ability to visual math contexts, confirming that visual-math compositional reasoning is a distinct and underexplored capability. Current SOTA as of early 2026 has risen significantly with models like Gemini and GPT-4o series.

## FoxBrain Relevance
Essential benchmark for any FoxBrain visual analytics application — engineering diagrams, production charts, quality control graphs, or scientific figures in R&D workflows. The IQTest and FunctionQA subsets are particularly relevant for manufacturing process optimization tasks that require interpreting numerical trends from visual displays. FoxBrain should target above human-level (>60.3%) on MathVista for visual analytics deployments.

---
*Back to [Main Digest](../README.md)*
