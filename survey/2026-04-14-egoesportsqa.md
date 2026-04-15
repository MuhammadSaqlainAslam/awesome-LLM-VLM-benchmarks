# EgoEsportsQA: An Egocentric Video Benchmark for Perception and Reasoning in Esports (2026)

## Problem
Video language models (VLMs) are evaluated predominantly on real-world daily-activity videos (cooking, sports, surveillance), leaving a critical gap: fast-paced, rule-intensive virtual environments that require both fine-grained visual perception and deep tactical reasoning. Esports gameplay offers a uniquely challenging setting — millisecond-scale micro-operations, complex rule systems, and layered tactical decision-making — that exposes VLM limitations invisible in slower, real-world video benchmarks.

## Method
**EgoEsportsQA** (arXiv: 2604.12320, April 14, 2026) presents a **video question-answering benchmark** built from professional esports matches across **3 first-person shooter (FPS) games**, captured from egocentric (player-perspective) viewpoints. The benchmark features a **two-dimensional taxonomy**: 11 cognitive capability sub-tasks spanning the full perception-to-reasoning spectrum, and 6 esports knowledge sub-tasks requiring domain-specific game mechanics understanding. Questions are designed at multiple granularities — basic visual perception (item locations, health status) through tactical reasoning (optimal positioning, decision-making under uncertainty) to fine-grained micro-operations (precise aim timing, ability sequencing). All 1,745 QA pairs are sourced from professional-level matches to ensure evaluation reflects the highest-stakes, most complex gameplay scenarios.

Authors: Jianzhe Ma, Zhonghao Cao, Shangkui Chen, Yichen Xu, Wenxuan Wang, Qin Jin.

## Benchmarks / Datasets
- **1,745 high-quality QA pairs** from professional FPS esports matches
- **3 first-person shooter games** (titles from professional esports circuit)
- **11 cognitive capability sub-tasks** (perception → tactical reasoning)
- **6 esports knowledge sub-tasks** (game mechanics, rule knowledge)
- Egocentric (first-person) video perspective throughout
- **Metrics:** Task accuracy per sub-task; overall accuracy; perception vs. reasoning gap

## Key Results

| Metric | Score | Notes |
|---|---|---|
| Best model accuracy | **71.58%** | Performance ceiling on full benchmark |
| Perception sub-tasks | Higher (relative strength) | Models handle basic visual grounding |
| Tactical reasoning | Substantially lower | Primary failure mode |
| Fine-grained micro-ops | Lowest | Most challenging category |

- **Best-performing model achieves only 71.58% overall accuracy**, with substantial room for improvement
- Models excel at basic visual perception (locating objects, reading health/ammo values) but **fail sharply on deep tactical reasoning and fine-grained micro-operations**
- The two-dimensional taxonomy successfully isolates perception failures from reasoning failures, revealing that current VLMs have a genuine tactical reasoning gap, not merely a perception problem
- Results expose architectural limitations in temporal modeling: fast-paced FPS sequences with millisecond-critical events exceed current VLM video understanding capabilities

## FoxBrain Relevance
While esports is not a direct Foxconn domain, EgoEsportsQA's core contribution is a rigorous test of VLM capabilities in fast-paced, rule-intensive environments with fine-grained temporal reasoning — directly analogous to Foxconn's manufacturing quality control (detecting assembly defects in real-time video), robotic process monitoring, and production line anomaly detection. The benchmark's taxonomy (perception vs. tactical reasoning vs. micro-operations) provides a reusable diagnostic framework for evaluating FoxBrain VLMs on factory-floor video understanding tasks before deployment.

---
*Back to [Main Digest](../README.md)*
