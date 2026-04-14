# MMRareBench: Evaluating MLLMs on Rare Disease Clinical Workflows (2026)

## Problem
Rare diseases — defined as conditions affecting fewer than 1 in 2,000 people — collectively affect 300 million patients worldwide yet receive disproportionately little AI research attention due to scarce training data. Clinical AI for rare diseases must handle extreme class imbalance, highly specialised diagnostic reasoning, multi-image evidence synthesis across imaging modalities, and treatment planning under profound uncertainty. No multimodal benchmark evaluated MLLMs on the complete rare disease clinical workflow: from initial diagnosis suspicion through multi-image evidence alignment to treatment recommendation and follow-up examination suggestion.

## Method
**MMRareBench** (arXiv: 2604.10755, April 12, 2026) curates **1,756 QA pairs** with **7,958 medical images** from PMC case reports spanning confirmed rare disease cases. The benchmark covers **4 clinical workflow tracks**:

1. **Diagnosis Track** — Identify the most likely rare disease from clinical presentation + imaging
2. **Treatment Planning Track** — Recommend appropriate management given confirmed diagnosis + imaging
3. **Cross-Image Evidence Alignment** — Synthesise findings across multiple imaging modalities (CT, MRI, histology, dermoscopy) for the same patient
4. **Examination Suggestion Track** — Recommend the next appropriate diagnostic test given current evidence

A **two-level evaluation protocol** assesses both factual accuracy and clinical reasoning quality. **23 MLLMs** are evaluated including GPT-5, Gemini-3.1-Pro, Claude Opus 4.5, and leading open-source models.

Authors: Junzhi Ning, Jiashi Lin, Yingying Fang, Wei Li.

## Benchmarks / Datasets
- **1,756 QA pairs** with **7,958 medical images** from PMC rare disease case reports
- **4 clinical tracks:** Diagnosis, Treatment Planning, Cross-Image Evidence Alignment, Examination Suggestion
- **23 MLLMs evaluated**
- **Two-level evaluation:** Factual accuracy + clinical reasoning quality
- **Source:** PMC confirmed rare disease case reports (real clinical data)

## Key Results

| Track | Performance | Key Finding |
|---|---|---|
| **Diagnosis** | Best track | Models show reasonable rare disease identification |
| **Cross-Image Evidence Alignment** | Moderate | Multi-modal synthesis is challenging |
| **Examination Suggestion** | Variable | Depends heavily on disease domain |
| **Treatment Planning** | **Universally lowest** | All 23 models show critically low performance |

- **All 23 evaluated MLLMs show universally low treatment planning performance** — the most clinically critical track is the worst-performing across every tested model
- **No single model dominates** — different models show domain-specific strengths (some better at imaging, others at clinical text reasoning)
- Cross-image evidence alignment (combining CT + MRI + histology for one patient) is significantly harder than single-modality QA, revealing that clinical multi-image synthesis remains unsolved
- The two-level protocol reveals that models often produce factually correct statements while demonstrating poor clinical reasoning quality — a dangerous pattern for medical AI deployment

## FoxBrain Relevance
MMRareBench establishes the benchmark for AI in specialised clinical domains where data scarcity and high stakes intersect — directly relevant to Foxconn's healthcare technology vertical and occupational health programs. The universal treatment planning failure is a clear boundary condition for any FoxBrain health application: the model can assist with clinical information retrieval and preliminary diagnosis support but must never be used for autonomous treatment recommendations without specialist review. The cross-image evidence alignment challenge also applies to FoxBrain's multi-sensor manufacturing inspection pipelines — synthesising evidence across multiple camera types (RGB, thermal, hyperspectral) for the same inspection target faces the same fundamental multi-modal integration challenge.

---
*Back to [Main Digest](../README.md)*
