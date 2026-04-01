# MATHVERSE: Does Your Multi-modal LLM Truly See the Diagrams in Visual Math Problems? (ECCV 2024)

## Problem
Existing visual math benchmarks pack excessive diagrammatic information *redundantly* into both images and text, allowing MLLMs to solve problems by reading only the text — without ever interpreting the diagram. This creates an illusion of visual math competence and masks a fundamental weakness.

## Method
MATHVERSE collects **2,612 high-quality multi-subject math problems with diagrams** spanning plane geometry, solid geometry, and functions. Human annotators transform each problem into **six versions** with varying visual-to-textual information ratios:
1. **Text Dominant** — full textual description + diagram (potentially redundant).
2. **Text Lite** — reduced text, more reliance on diagram.
3. **Text Only** — no diagram; tests pure symbolic reasoning.
4. **Vision Intensive** — diagram + minimal text cues.
5. **Vision Dominant** — diagram with almost no text.
6. **Vision Only** — diagram alone, no text at all.

This ablation design yields **15K+ total test samples**. A CoT evaluation strategy uses GPT-4(V) to adaptively extract and score each reasoning step, enabling fine-grained error analysis beyond binary correct/wrong scoring.

## Benchmarks / Datasets
- **MATHVERSE:** 2,612 source problems → 15K test samples across 6 difficulty versions.
- **Subjects:** Plane geometry, solid geometry, functions.
- **Metrics:** Step-level CoT accuracy scored by GPT-4(V).

## Key Results
Most MLLMs rely heavily on textual shortcuts — performance drops sharply as text content is reduced. **Genuine visual mathematical reasoning** (extracting values, relationships, or quantifiers directly from diagrams) remains weak across all tested frontier models, including GPT-4V. The Vision Only setting exposes a severe gap between claimed and actual visual math capability.

## FoxBrain Relevance
FoxBrain will need to read engineering schematics, circuit diagrams, and tolerance charts — all of which are Vision Intensive or Vision Only scenarios. MATHVERSE's six-version ablation is the right diagnostic to reveal whether FoxBrain is truly interpreting technical drawings or relying on caption-like metadata in the prompt.

---
*Back to [Main Digest](../README.md)*
