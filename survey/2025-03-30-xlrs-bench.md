# XLRS-Bench: Multimodal LLMs on Extremely Large Ultra-High-Resolution Remote Sensing Imagery (2025)

## Problem
Current VLM benchmarks use standard-resolution images (224×224 to 1024×1024), but real-world remote sensing (RS) applications require understanding of **extremely large, ultra-high-resolution (UHR) satellite and aerial images** (often 8000×8000+ pixels). No benchmark existed to measure whether MLLMs can actually perceive and reason over such massive-scale RS imagery.

## Method
**XLRS-Bench** is a comprehensive benchmark for evaluating the perception and reasoning capabilities of MLLMs on **ultra-high-resolution remote sensing imagery**. All evaluation samples are manually annotated with assistance from a novel **semi-automatic captioner** designed for UHR RS images. The benchmark covers both **Chinese (XLRS-Bench-ZH)** and **English (XLRS-Bench-EN)** versions to test multilingual RS understanding.

## Benchmarks / Datasets
* **XLRS-Bench** — **45,942 annotations** across:
  * **10 perception ability indicators** (object detection, counting, attribute recognition, etc.)
  * **6 reasoning ability indicators** (spatial reasoning, change detection, scene understanding, etc.)
* **Dataset breakdown:**
  * 32,389 VQA pairs
  * 12,619 visual grounding instances
  * 934 detailed captions
* **Largest average image size:** **8,500 × 8,500 pixels** — largest RS benchmark of its kind.
* **Metrics:** VQA Accuracy, Grounding Precision (IoU), Caption Quality (BLEU/CIDEr).

## Key Results
* Current frontier MLLMs (GPT-4V, LLaVA, etc.) show significant performance drops on UHR RS images compared to standard-resolution benchmarks.
* Perception tasks (object detection, counting) degrade most severely at high resolutions, revealing a fundamental limitation of current vision encoders that downsample input.
* Reasoning tasks show moderate performance but fail on fine-grained spatial relationships across large image contexts.

## FoxBrain Relevance
If FoxBrain is applied to **satellite imagery, drone footage, or industrial inspection** (relevant for Foxconn's manufacturing and infrastructure monitoring), XLRS-Bench sets the bar for vision encoder quality at UHR inputs. Standard VLM encoders will fail here — high-res tiling or native-resolution encoders are required.

---
*Back to [Main Digest](../README.md)*
