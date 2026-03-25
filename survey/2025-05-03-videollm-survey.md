# Paper Overview: VideoLLM Benchmarks and Evaluation: A Survey

## Problem
The rapid shift from Image-LLMs to Video-LLMs has created a fragmented evaluation landscape. Standard vision-language metrics (like CIDEr) fail to capture temporal reasoning and complex motion patterns.

## Method
A comprehensive meta-analysis of the VideoLLM landscape. It categorizes benchmarks into **Closed-set** (multiple choice) and **Open-set** (flexible reasoning), specifically highlighting the move toward "extremely long video" benchmarks like InfiniBench (hour-long videos).

## Benchmarks / Datasets
* **Key Benchmarks Examined:** ActivityNet-QA (temporal reasoning), TVQA (dialogue/plot), and MLVU (long-video context).
* **Finding:** Current VideoLLMs struggle significantly with maintaining context over extended durations.

## FoxBrain Relevance
This survey helps us select the right "test suite" for our video-monitoring sub-systems. We will adopt the **specialized temporal evaluations** mentioned here to improve our model's ability to track objects over hour-long feeds.

---
*Back to [Main Digest](../README.md)*
