# GeoAgentBench: A Dynamic Execution Benchmark for Tool-Augmented Agents in Spatial Analysis (2026)

## Problem
Existing benchmarks for GIS-based AI agents rely on static, offline evaluation methods that fail to capture the interactive, multi-step execution dynamics of real spatial analysis workflows. No prior benchmark combined a live sandbox environment with the breadth of atomic GIS tools needed to reflect professional geographic information science practice, leaving a critical gap in assessing tool-augmented LLM agents on real-world spatial tasks.

## Method
**GeoAgentBench** (arXiv: 2604.13888, April 15, 2026) constructs a dynamic, interactive evaluation sandbox containing 117 atomic GIS tools spanning 6 core GIS domains, and evaluates 7 representative LLMs on 53 typical spatial analysis tasks. The benchmark introduces the Parameter Execution Accuracy (PEA) metric using a "Last-Attempt Alignment" strategy, and employs Vision-Language Model verification to assess spatial accuracy and cartographic style of outputs.

Authors: Bo Yu, Cheng Yang, Dongyang Hou, Chengfu Liu, Jiayao Liu, Chi Wang, Zhiming Zhang, Haifeng Li, Wentao Yang

## Benchmarks / Datasets
- 117 atomic GIS tools available in the sandbox environment
- 53 typical spatial analysis tasks across 6 core GIS domains
- 7 representative LLMs evaluated
- Novel PEA (Parameter Execution Accuracy) metric with Last-Attempt Alignment strategy
- VLM-based visual verification of spatial outputs and cartographic quality
- 20-page paper with 3 figures and 6 evaluation tables

## Key Results

| Agent Architecture | Spatial Task Success | Parameter Accuracy (PEA) |
|---|---|---|
| Plan-and-React | Best overall | Highest balance |
| Traditional Frameworks | Lower | Weaker recovery |
| Base LLM (no agent) | Lowest | Poor multi-step |

- The "Plan-and-React" agent architecture significantly outperforms traditional frameworks, achieving the optimal balance between logical rigor and execution robustness.
- PEA metric reveals substantial differences between agent architectures that pass/fail metrics alone would miss, particularly in multi-step parameter chaining.
- VLM-based cartographic verification exposes quality gaps invisible to functional pass/fail scoring, especially for map style and spatial accuracy.

## FoxBrain Relevance
GeoAgentBench directly applies to Foxconn's geospatial facility planning and logistics optimization tasks, where LLM agents must orchestrate GIS tools to analyze factory locations, supply chain routing, and regional distribution networks. The PEA metric is especially valuable for FoxBrain's tool-calling pipelines, measuring not just whether an agentic step completes but whether parameters are correctly specified — a critical quality bar for high-stakes enterprise workflows. The benchmark's "Plan-and-React" architecture finding recommends a specific agent design pattern for FoxBrain's spatial intelligence components. The 117-tool sandbox methodology can be adapted to build a Foxconn-specific manufacturing operations tool-bench spanning ERP, MES, and logistics APIs.

---
*Back to [Main Digest](../README.md)*
