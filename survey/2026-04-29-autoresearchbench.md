# AutoResearchBench: Benchmarking AI Agents on Complex Scientific Literature Discovery (2026)

## Problem
AI agents capable of autonomous scientific literature discovery — finding specific papers through multi-step investigation and comprehensively collecting papers meeting specified criteria — are increasingly used in research workflows. Yet no benchmark existed to evaluate this capability rigorously. General agentic web-browsing benchmarks do not capture the deep comprehension of research concepts and deliberate multi-step reasoning that scientific literature search requires.

## Method
**AutoResearchBench** (arXiv: 2604.25256, April 29, 2026) introduces a benchmark for evaluating AI agents on two complementary scientific literature discovery tasks: Deep Research (finding specific target papers through multi-step investigation of research lineages) and Wide Research (comprehensively collecting all papers meeting specified criteria across a domain). The benchmark tests the most powerful frontier LLMs alongside strong baselines, measuring performance with task-specific accuracy metrics for each research mode.

## Benchmarks / Datasets
- Two task types: Deep Research (target paper discovery) + Wide Research (comprehensive collection)
- Tasks sourced from real scientific literature discovery challenges
- Frontier LLMs + strong baselines evaluated
- Deep Research metric: accuracy at finding specific target papers
- Wide Research metric: Intersection over Union (IoU) of collected vs. ground-truth paper sets

## Key Results

| Task Type | Top LLM Performance | Baseline Performance |
|---|---|---|
| Deep Research | 9.39% accuracy | Below 5% for most baselines |
| Wide Research | 9.31% IoU | Below 5% for most baselines |

- **Even the most powerful frontier LLMs — which have largely solved general agentic web-browsing benchmarks — achieve only ~9% on complex scientific literature discovery tasks**
- Deep Research and Wide Research both expose the same fundamental gap: models lack the ability to reason about research concept relationships and follow multi-step citation lineages
- Scientific literature discovery requires deep comprehension of domain concepts that goes far beyond keyword search or surface-level web browsing
- AutoResearchBench reveals that conquering general benchmarks does not transfer to the specialised reasoning required for autonomous research assistance

## Enterprise / Industry Relevance
Foxconn's R&D teams and IP strategy functions require systematic scientific literature discovery — tracking competitive research, identifying prior art for patent filings, and monitoring emerging technologies. AutoResearchBench's finding that top LLMs achieve only ~9% on rigorous literature discovery tasks means FoxBrain cannot be trusted to autonomously conduct comprehensive patent or research surveys without extensive human expert verification. The benchmark's distinction between Deep Research (finding specific papers) and Wide Research (comprehensive collection) maps directly to the two modes Foxconn's research intelligence teams use — and both are currently beyond reliable autonomous AI capability.

---
*Back to [Main Digest](../README.md)*
