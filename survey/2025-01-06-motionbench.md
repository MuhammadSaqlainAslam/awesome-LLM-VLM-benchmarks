# MotionBench: Benchmarking Fine-grained Video Motion Understanding for VLMs (2025)

## Problem
Existing video understanding benchmarks focus on scene-level semantics (what objects are in a video) but ignore **fine-grained motion comprehension** — the precise type, direction, speed, and sequence of movements. Current VLMs trained on static image-text pairs fail to capture the temporal dynamics that define motion.

## Method
**MotionBench** is a comprehensive evaluation benchmark assessing fine-grained motion understanding via **6 primary motion-oriented question categories**:
1. Motion Type Recognition
2. Motion Direction
3. Motion Speed/Magnitude
4. Object-Motion Binding (which object performs which motion)
5. Temporal Order of Motions
6. Motion Causality

Data is collected from diverse real-world video sources with **manual annotation** ensuring high quality. To address identified VLM weaknesses, the authors also propose a **Through-Encoder (TE) Fusion** method that injects temporal features directly into the LLM encoder pathway, enabling fine-grained motion signals within standard LLM token budgets.

## Benchmarks / Datasets
* **MotionBench** — **5,000 videos** with manually annotated fine-grained motion questions.
* **Annotation Density:** 68.4 — **2× denser** than prior video benchmarks.
* 6 motion question types covering perception and causal reasoning.
* **Metrics:** Motion Question Answering Accuracy (per category + overall).
* Accepted at **CVPR 2025**.

## Key Results
* Existing frontier VLMs (GPT-4V, LLaVA, VideoLLaMA) perform **significantly below human level** on fine-grained motion tasks.
* **Temporal Order** and **Motion Causality** categories are hardest; all tested models fail near chance.
* **TE Fusion** method improves fine-grained motion accuracy by ~12% over vanilla video-LLM architectures with no extra inference cost.

## FoxBrain Relevance
Directly relevant for Foxconn's **manufacturing quality control** and **assembly line monitoring** — e.g., detecting if a robotic arm performed the correct motion sequence or if a worker assembled parts in the right order. MotionBench defines the bar FoxBrain's vision module must clear for reliable motion-aware inspection.

---
*Back to [Main Digest](../README.md)*
