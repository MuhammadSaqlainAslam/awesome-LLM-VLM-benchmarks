# WildFireVQA: Large-Scale VQA Benchmark for Aerial Wildfire Monitoring (2026)

## Problem
Wildfire monitoring from aerial platforms requires multimodal reasoning over RGB and thermal imagery, yet no benchmark had evaluated how well multimodal large language models handle the unique challenges of fire detection, distribution mapping, and flight path planning. Existing remote sensing benchmarks do not incorporate radiometric thermal data or safety-critical flight planning tasks, leaving a gap for AI-assisted emergency response applications.

## Method
**WildFireVQA** (arXiv: 2604.20190, April 22, 2026) is a large-scale VQA benchmark integrating RGB and radiometric thermal aerial imagery of wildfires. The benchmark covers six task categories across 6,097 RGB-thermal image pairs, producing 207,298 multiple-choice questions. Annotation combines MLLM-based answer generation with sensor-driven deterministic labelling, manual verification, and intra-frame and inter-frame consistency checks. Models are evaluated under RGB-only, thermal-only, and retrieval-augmented settings.

Authors: (listed in paper)

## Benchmarks / Datasets
- 6,097 RGB-thermal aerial image sample pairs
- 207,298 multiple-choice questions total
- Six task categories: presence and detection, classification, distribution and segmentation, localisation and direction, cross-modal reasoning, flight planning
- Three evaluation settings: RGB, thermal, and retrieval-augmented
- Representative MLLMs evaluated across all three modality configurations

## Key Results

| Modality Setting | Performance Trend |
|---|---|
| RGB only | Strongest performance for current models |
| Thermal only | Weakest; models not adapted to thermal cues |
| Retrieval-augmented thermal | Gains for stronger MLLMs vs. thermal alone |

- **RGB remains the strongest modality for current models; thermal data is underutilised despite its unique value for detecting active fire zones invisible in RGB**
- Retrieved thermal context yields measurable gains for stronger MLLMs, suggesting RAG-based thermal integration is a viable path forward
- Cross-modal reasoning (jointly interpreting RGB and thermal) and flight planning tasks are the most challenging categories for all evaluated models

## FoxBrain Relevance
Foxconn's large industrial campuses in fire-prone regions of Taiwan, China, and India require advanced early warning and emergency response capabilities. A FoxBrain vision module benchmarked on WildFireVQA would be better positioned to integrate with thermal camera networks for factory fire detection and suppression zone planning. The benchmark's cross-modal RGB+thermal reasoning task mirrors Foxconn's industrial inspection setting, where thermal cameras are deployed alongside standard CCTV to detect overheating components and electrical fires. The flight planning task category also has relevance to Foxconn's drone-based campus inspection workflows, where autonomous path planning under hazardous conditions is an active R&D priority.

---
*Back to [Main Digest](../README.md)*
