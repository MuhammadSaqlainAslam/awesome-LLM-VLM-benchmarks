# Paper Overview: MMMU-Pro: A More Robust Multi-discipline Multimodal Understanding Benchmark

## Problem
What problem does this paper solve? (1–2 sentences)
Many current Vision-Language Models (VLMs) "cheat" on multimodal benchmarks by relying on text-based language priors rather than actually "seeing" the image. MMMU-Pro addresses this by introducing a vision-only input mode and harder expert-level questions that force models to integrate visual and textual information seamlessly.

## Method
What approach did they use? (1–2 sentences)
The researchers redesigned the original MMMU by converting textual options and questions into "text-rich images," effectively disabling the model's ability to use OCR as a separate pre-processing step. They also implemented a more rigorous multi-discipline evaluation across 30+ domains to eliminate "shallow" reasoning shortcuts.

## Benchmarks / Datasets
List all benchmarks and datasets used.
* **MMMU-Pro:** The new primary benchmark featuring 3,460 expert-level questions.
* **Vision-only Input Mode:** A specific test setting where all text is rendered as pixels.
* **Baselines:** Compared against GPT-4o, Gemini 1.5 Pro, and the original MMMU scores to calculate the "Perception Gap."

## Key Results
At least one concrete number.
Results show a massive drop in performance across all models when text is rendered as pixels; for example, **Gemini 3.1 Pro** leads the leaderboard but only achieves **82% on MMMU-Pro**, whereas models that scored ~70% on the original MMMU frequently drop below **30%** on the Pro version.

## FoxBrain Relevance
Is there anything we can learn or apply to FoxBrain?
Highly critical. It teaches us that "High OCR accuracy is necessary but not sufficient for multimodal intelligence." For FoxBrain, we must ensure our models aren't just reading the text on a chart but are actually understanding the spatial relationships and data trends within the image. We should use MMMU-Pro to verify if our models are truly "seeing."

---
*Back to [Main Digest](../README.md)*
