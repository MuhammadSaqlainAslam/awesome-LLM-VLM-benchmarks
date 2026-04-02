# R1-Onevision: Advancing Generalized Multimodal Reasoning through Cross-Modal Formalization (2025)

## Problem
Applying DeepSeek-R1-style reinforcement learning to vision-language models is non-trivial: images are not natively amenable to formal symbolic reasoning, so the RL reward signal cannot easily verify step-by-step visual reasoning chains. R1-Onevision addresses this by first converting diverse visual inputs into structured textual formalizations, enabling rigorous RL training over verified reasoning traces.

## Method
The core contribution is a **Cross-Modal Formalization Pipeline** that converts images into domain-appropriate structured text representations using GPT-4o, Grounding DINO, and EasyOCR: circuits become SPICE netlists, flowcharts become PlantUML, tables become CSV/JSON. This pipeline constructs the **R1-Onevision dataset** of 155K samples spanning science, mathematics, charts, and general scenarios, each with verified step-by-step multimodal reasoning annotations. Training proceeds in two stages: supervised fine-tuning on the formalized dataset followed by reinforcement learning with verifiable rewards. A role-playing strategy drives iterative visual understanding refinement. The work also introduces **R1-Onevision-Bench**: 942 questions across 5 domains (Math, Physics, Chemistry, Biology, Deduction), 4 difficulty grades (Junior High through Social/Professional Test), and 38 subcategories aligned with human educational stages. Accepted at **ICCV 2025**.

## Benchmarks / Datasets
- **MathVision:** Challenging math problems requiring visual diagrams
- **MathVerse (ALL):** Mathematical diagram reasoning
- **MathVista:** Visual mathematical reasoning
- **WeMath:** Weighted math evaluation
- **R1-Onevision-Bench (new):** 942 QA, 5 domains, 4 difficulty grades, 38 subcategories

## Key Results (R1-Onevision-7B vs baselines)
| Benchmark | R1-Onevision-7B | GPT-4o | Qwen2.5-VL-7B |
|---|---|---|---|
| MathVision | 29.9% | 30.6% | 25.4% |
| MathVerse ALL | **46.4%** | 41.2% | 43.6% |
| MathVerse Vision-Only | **(+5.5% vs GPT-4o)** | — | — |
| MathVista | **40.0%** | 34.5% | 38.2% |
| R1-OV-Bench (Avg) | 36.2% | 49.6% | 32.1% |

- A 7B model outperforms GPT-4o on MathVerse ALL (+5.2%) and MathVista (+4.1%)
- Cross-modal formalization enables RL training on visual reasoning at a fraction of the cost of larger proprietary models

## FoxBrain Relevance
R1-Onevision's cross-modal formalization pipeline is directly applicable to Foxconn's engineering workflows: circuit schematics → SPICE, process flowcharts → PlantUML, BOM tables → JSON. This structured intermediate representation enables FoxBrain to apply verifiable RL training on factory-relevant visual reasoning tasks without requiring hand-labeled symbolic annotations. The difficulty-graded R1-Onevision-Bench structure can serve as a template for FoxBrain's own tiered engineering assessment suite.

---
*Back to [Main Digest](../README.md)*
