# Paper Overview: GPQA: A Graduate-Level Google-Proof Q&A Benchmark

## Problem
What problem does this paper solve? (1–2 sentences)
Standard benchmarks (like MMLU) are increasingly prone to data contamination and are becoming too easy for frontier models. GPQA addresses this by introducing a "Google-proof" dataset of science questions that are so difficult that even non-expert humans with unrestricted internet access cannot find the answers easily.

## Method
What approach did they use? (1–2 sentences)
The authors hired PhD-level experts in biology, physics, and chemistry to write 448 high-quality multiple-choice questions. They validated these through a "scalable oversight" framework where questions were only kept if they were unambiguous to experts but consistently misled non-experts (even those using Google). The **Diamond** subset consists of the 198 hardest, most verified questions.

## Benchmarks / Datasets
List all benchmarks and datasets used.
* **GPQA Diamond:** The flagship subset of 198 highly-vetted, expert-level questions.
* **GPQA Main:** The full set of 448 questions.
* **GPQA Extended:** A larger, less-vetted set of 1,000+ questions.
* **Baselines:** Comparison against PhD experts (avg. ~65-70%) and skilled non-experts with web access (avg. ~34%).

## Key Results
At least one concrete number.
Upon release in late 2023, **GPT-4** scored only **39%**, barely above the non-expert human baseline. However, as of March 2026, frontier reasoning models like **Gemini 3.1 Pro** have reached an unprecedented **94.3% accuracy**, officially surpassing the human expert baseline on this specific scientific reasoning task.

## FoxBrain Relevance
Is there anything we can learn or apply to FoxBrain?
Extremely high relevance for technical validation. GPQA Diamond serves as a "stress test" for FoxBrain's reasoning capabilities. It teaches us that to achieve PhD-level performance, we must prioritize **Chain-of-Thought (CoT)** depth. If FoxBrain can maintain a high score here, it proves the model isn't just "chatting" but is performing valid logical deduction in high-stakes scientific contexts.

---
*Back to [Main Digest](../README.md)*
