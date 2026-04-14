# BareBones: Probing Geometric Shape Comprehension in VLMs via Texture-Deprived Silhouettes (2026)

## Problem
Modern VLMs are trained predominantly on richly textured, colourful natural images, creating a systematic dependency on texture and colour as the primary recognition cues. This "texture bias" means models may appear capable of visual reasoning while actually relying on surface statistics rather than genuine geometric understanding — a critical weakness for any application requiring shape-based reasoning (engineering drawings, medical imaging, manufacturing inspection, CAD analysis). No benchmark systematically evaluated whether VLMs could maintain performance when stripped of all texture and colour information, leaving only pure geometric shape (silhouettes).

## Method
**BareBones** (arXiv: 2604.10528, April 12, 2026) evaluates **26 VLMs** on **zero-shot geometric shape comprehension** using **pixel-level binary silhouettes** — images from which all colour, texture, lighting, and background information has been removed, leaving only the 2D geometric boundary of the object. Six established datasets are converted to silhouette format, and a new dataset **WTP-Bench (What's The Part?)** is created for fine-grained geometric sub-part classification — testing whether models can identify not just the object category but its specific structural components from shape alone.

The benchmark introduces the **"Texture Bias Cliff"** metric — the performance drop between standard RGB input and silhouette-only input — as a quantitative measure of over-reliance on surface statistics. Authors: Aaditya Baranwal, Vishal Yadav, Abhishek Rajora.

## Benchmarks / Datasets
- **26 VLMs evaluated** (GPT-4.1, Gemini-3.1, Claude Sonnet 4.5, LLaVA family + 22 others)
- **6 established datasets** converted to silhouette format + **WTP-Bench** (new fine-grained geometric classification)
- **Input:** Pixel-level binary silhouettes (zero colour, texture, lighting, background)
- **Task:** Zero-shot object and part classification from shape alone
- **Metrics:** Silhouette accuracy; Texture Bias Cliff (RGB accuracy − silhouette accuracy)

## Key Results

| Model | Silhouette Performance | Texture Bias Cliff | Notes |
|---|---|---|---|
| GPT-4.1 | Severe collapse | High | Despite strong RGB performance |
| Gemini-3.1 | Severe collapse | High | |
| Claude Sonnet 4.5 | Severe collapse | High | |
| LLaVA variants | Severe collapse | High | |
| **All 26 VLMs** | **Severe collapse** | **Universal** | No model exception |

- **All 26 tested VLMs — including GPT-4.1, Gemini-3.1-Pro, and Claude Sonnet 4.5 — show severe performance collapse on silhouette inputs**; the "Texture Bias Cliff" is universal across architectures
- **WTP-Bench (fine-grained geometric parts)** further amplifies the failure — no model can reliably classify structural sub-parts from silhouette alone
- Performance collapse is not gradual — removing texture causes a sharp, cliff-like degradation (not a smooth reduction), confirming texture is a primary cue, not a supplementary one
- The finding holds across model families, scales, and training approaches — no architecture is immune to texture bias

## FoxBrain Relevance
BareBones reveals a critical capability gap for FoxBrain's manufacturing inspection deployments: any task requiring geometric shape analysis from technical drawings, CAD diagrams, schematic symbols, or line-art manufacturing specifications will expose the Texture Bias Cliff. PCB silkscreen inspection, component outline verification, and engineering drawing analysis are all silhouette-like tasks where texture information is absent by design. FoxBrain cannot be trusted for these tasks without domain-specific geometric fine-tuning on texture-deprived training data. Recommended: run BareBones on FoxBrain before any deployment involving technical drawings, CAD schematics, or component outlines — quantify the Texture Bias Cliff and fine-tune on Foxconn's internal silhouette-style engineering imagery if the gap exceeds an acceptable threshold.

---
*Back to [Main Digest](../README.md)*
