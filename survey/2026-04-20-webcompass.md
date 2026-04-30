# WebCompass: Towards Multimodal Web Coding Evaluation for Code Language Models (2026)

## Problem
Existing code generation benchmarks evaluate LLMs on isolated functions or algorithmic problems, missing the complex multimodal web development context where developers work with visual designs, video tutorials, and textual specifications simultaneously. No prior benchmark evaluates code models on generation, editing, and repair tasks across text, image, and video input modalities in a unified framework.

## Method
**WebCompass** (arXiv: 2604.18224, April 20, 2026) constructs a comprehensive benchmark with three task types (generation, editing, repair) across three input modalities (text, image, video). The benchmark uses human-in-the-loop curation covering 15 generation domains, 16 editing operation types, and 11 repair defect types at Easy/Medium/Hard difficulty levels. It proposes an Agent-as-a-Judge evaluation paradigm using real browser execution and automated test synthesis.

Authors: Xinping Lei, Xinyu Che, Junqi Xiong, Chenchen Zhang, Yukai Huang, Chenyu Zhou, Haoyang Huang, Minghao Liu, Letian Zhu, Hongyi Ye, Jinhua Hao, Ken Deng, Zizheng Zhan, Han Li, Dailin Li, Yifan Yao, Ming Sun, Zhaoxiang Zhang, Jiaheng Liu

## Benchmarks / Datasets
- 15 generation domains, 16 editing operation types, 11 repair defect types
- Three difficulty levels: Easy / Medium / Hard
- Representative closed-source and open-source code models evaluated
- Key metrics: Browser Execution Pass Rate, Aesthetic Score, Framework-Specific Success Rate

## Key Results

| Model Class | Generation | Editing | Repair |
|---|---|---|---|
| Closed-source | Higher | Higher | Better interactivity |
| Open-source | Lower | Lower | Weaker |
| Vue framework | Hardest | Hardest | Most failures |

- **Closed-source models consistently outperform open-source models across all task types and modalities**
- Repair tasks better preserve UI interactivity compared to generation tasks
- Aesthetics represents the primary bottleneck for all evaluated models; Vue framework is the most challenging
- Framework choice significantly impacts overall performance beyond model capability alone

## Enterprise / Industry Relevance
Foxconn develops internal web-based dashboards and enterprise portal tools for supply chain monitoring, quality inspection reporting, and factory-floor management. WebCompass directly measures whether code-generation models can handle the full web development lifecycle — from visual design to bug repair — which is exactly what FoxBrain needs to support Foxconn's internal tooling teams. The benchmark's video-input modality is particularly relevant for FoxBrain's scenario where developers record screen walkthroughs of legacy systems to guide automated code modernization. Evaluating FoxBrain against WebCompass's repair track would reveal its ability to maintain interactivity in retrofitted enterprise UI components.

---
*Back to [Main Digest](../README.md)*
