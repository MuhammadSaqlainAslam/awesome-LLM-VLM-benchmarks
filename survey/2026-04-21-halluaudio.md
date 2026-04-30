# HalluAudio: A Comprehensive Benchmark for Hallucination Detection in Large Audio-Language Models (2026)

## Problem
Large Audio-Language Models (LALMs) are increasingly deployed in speech recognition, environmental sound understanding, and music analysis, yet their tendency to hallucinate — generating outputs not grounded in the actual audio input — has not been systematically measured. No prior benchmark covered all three audio modalities (speech, environmental sound, music) with fine-grained diagnostic analysis, leaving a critical blind spot in LALM safety evaluation.

## Method
**HalluAudio** (arXiv: 2604.19300, April 21, 2026) is the first large-scale hallucination benchmark for LALMs, comprising over 5,000 human-verified QA pairs spanning speech, environmental sound, and music across four task types: binary judgments, multi-choice reasoning, attribute verification, and open-ended QA. The benchmark enables fine-grained error-type analysis across modalities and measures hallucination rate, yes/no bias, error-type distribution, and refusal rate. Accepted to ACL 2026.

Authors: Feiyu Zhao, Yiming Chen, Wenhuan Lu, Daipeng Zhang, Xianghu Yue, Jianguo Wei

## Benchmarks / Datasets
- 5,000+ human-verified QA pairs covering speech, environmental sound, and music
- 4 task types: binary judgment, multi-choice reasoning, attribute verification, open-ended QA
- Broad range of open-source and proprietary LALMs evaluated
- Key metrics: hallucination rate, yes/no bias, error-type analysis, refusal rate

## Key Results

| Audio Modality | Hallucination Challenge Level |
|---|---|
| Speech | Moderate — best-understood modality |
| Environmental Sound | High — temporal grounding failures common |
| Music | Highest — attribute verification most error-prone |

- **Significant hallucination deficiencies identified across all tested LALMs on acoustic grounding and temporal reasoning tasks**
- Models exhibit systematic yes/no bias that inflates apparent accuracy on binary judgment tasks
- Environmental sound and music modalities show substantially worse hallucination control than speech, revealing modality-specific training gaps

## Enterprise / Industry Relevance
Foxconn's factories operate in high-noise environments where audio monitoring systems detect anomalous machine sounds, worker safety alerts, and equipment failure signatures. FoxBrain's multimodal capabilities, when extended to audio, could power predictive maintenance and safety monitoring systems on the production floor. HalluAudio's environmental sound tasks directly mirror this use case: a LALM hallucinating about ambient industrial sounds could trigger false safety alerts or miss genuine equipment failures. Running HalluAudio on any FoxBrain audio-language module before factory deployment is essential to characterize modality-specific hallucination rates and establish safe operating thresholds.

---
*Back to [Main Digest](../README.md)*
