# Paper Overview: Humanity's Last Exam (HLE)

## Problem
What problem does this paper solve? (1–2 sentences)
Traditional benchmarks like MMLU and GSM8K have become saturated, with top models achieving near-perfect scores due to data contamination and inherent simplicity. HLE is designed to be a "Google-proof" exam that tests the absolute frontier of human knowledge across specialized fields where current AI still fails.

## Method
What approach did they use? (1–2 sentences)
The researchers crowdsourced 3,000 extremely difficult, multi-disciplinary questions from PhD-level experts and practitioners, ensuring the answers were not easily searchable online. They implemented a rigorous "can-it-be-googled" filtration process and a multimodal component requiring complex visual-reasoning integration.

## Benchmarks / Datasets
List all benchmarks and datasets used.
* **HLE (Humanity's Last Exam):** The primary new benchmark consisting of 2,500 text questions and 500 multimodal (vision-based) questions.
* **Baseline Comparisons:** MMLU-Pro, GPQA (Diamond), and MathVista were used to calibrate the difficulty level against existing frontier benchmarks.

## Key Results
At least one concrete number.
While models achieve ~90% on MMLU, the best-performing model at release (GPT-4o) achieved only **34.8% accuracy on HLE**, and Claude 3.5 Sonnet scored **32.1%**, illustrating a massive gap between "general knowledge" and "expert-level reasoning."

## FoxBrain Relevance
Is there anything we can learn or apply to FoxBrain?
Extremely relevant for "frontier-checking." As FoxBrain moves toward specialized domain applications (Medicine, Engineering, Law), we should use HLE to determine if our fine-tuned models actually possess deep subject-matter expertise or are simply reciting memorized training data.

---
*Back to [Main Digest](../README.md)*
