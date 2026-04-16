# AISafetyBenchExplorer: A Metric-Aware Catalogue of AI Safety Benchmarks Reveals Fragmented Measurement and Weak Benchmark Governance (2026)

## Problem
The AI safety evaluation landscape has undergone massive proliferation — over 195 benchmarks from 2018 to 2026 — but without corresponding standardization of measurement practices, leading to a situation where familiar metric labels (accuracy, F1, safety score) conceal materially different judges, aggregation rules, and threat models. Researchers and practitioners lack principled criteria for benchmark selection, and the majority of safety benchmarks are poorly maintained, rendering comparative evaluation of AI safety progress unreliable.

## Method
**AISafetyBenchExplorer** (arXiv: 2604.12875, April 14, 2026) constructs a structured catalogue of 195 AI safety benchmarks published between 2018 and 2026, annotating each with a rich metadata schema covering task type, metric definitions, dataset complexity tier, language coverage, and maintenance status. The paper performs systematic meta-analysis to identify fragmentation patterns, metric inconsistencies, and governance failures across the safety benchmark ecosystem.

Authors: Abiodun A. Solanke

## Benchmarks / Datasets
- 195 AI safety benchmarks catalogued (2018–2026)
- 94/195 classified as medium-complexity tier
- 7 benchmarks categorized as "Popular" tier (high adoption)
- 165/195 English-only (monolingual coverage gap)
- 170/195 evaluation-only resources (no training data)
- 137/195 stale GitHub repositories (no recent commits)
- 96/195 stale Hugging Face datasets (outdated or inactive)

## Key Results

| Metric | Count | Key Finding |
|---|---|---|
| Total benchmarks catalogued | 195 | Benchmark proliferation without standardization |
| English-only coverage | 165/195 (85%) | Severe language gap |
| Stale repositories | 137/195 (70%) | Governance and maintenance failure |
| Popular benchmarks | 7/195 (3.6%) | Highly concentrated adoption |

- Familiar metric labels such as accuracy, F1, and "safety score" conceal materially different judges, aggregation rules, and threat models — making cross-benchmark comparison unreliable.
- 70% of catalogued safety benchmarks have stale GitHub repositories, and 49% have inactive Hugging Face datasets, indicating a critical maintenance crisis in the safety evaluation ecosystem.
- Benchmark adoption is highly concentrated: only 7 of 195 benchmarks achieve "Popular" status, while the majority are published once and never revisited, creating a misleading illusion of comprehensive coverage.

## FoxBrain Relevance
AISafetyBenchExplorer provides FoxBrain's AI safety team with a curated starting point for selecting trustworthy, actively maintained safety evaluation benchmarks rather than defaulting to whatever is most cited. The 85% English-only coverage gap directly flags a risk for Foxconn's multilingual deployments across Asia: safety certifications based on English-only benchmarks may not transfer to Mandarin, Japanese, or Indic language contexts. The catalogue's medium-complexity classification system helps FoxBrain teams calibrate testing difficulty against the operational complexity of target deployment scenarios (e.g., factory control vs. customer-facing chat). The stale-repository finding mandates that Foxconn's AI governance policy require benchmark maintenance status verification before any safety benchmark is incorporated into FoxBrain's certification pipeline.

---
*Back to [Main Digest](../README.md)*
