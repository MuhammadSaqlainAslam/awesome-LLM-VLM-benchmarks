## Problem
Standard OCR benchmarks use "clean" digital PDFs, which do not represent the messy, warped, or poorly-lit documents found in real-world office and industrial settings.

## Method
**OmniDocBench** (via the Real5-OmniDoc dataset) introduces 5 types of physical distortions: warping, skewing, screen-photography, low light, and digital noise.

## Benchmarks / Datasets
- **Benchmark:** Real5-OmniDoc (OmniDocBench)
- **Dataset:** 1,355 high-res images of physical documents
- **Metrics:** Word Error Rate (WER), Layout Parsing Accuracy

## Key Results
Frontier VLMs show a **35% performance degradation** on warped or skewed text compared to their performance on standard digital-born PDF benchmarks.

## FoxBrain Relevance
Extremely high. FoxBrain’s document parsing capability must be robust against "camera-captured" documents. We should use this to test our VLM's OCR limits.

---
*Back to [Main Digest](../README.md)*
