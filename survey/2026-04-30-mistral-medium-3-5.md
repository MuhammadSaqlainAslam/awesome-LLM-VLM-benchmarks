# Mistral Medium 3.5 (128B): Unified Flagship — Instruction, Reasoning, and Coding in One Model (2026)

## Problem
Enterprise deployments of frontier models have historically required maintaining multiple specialised models for different task types: a coding model, a reasoning model, and an instruction-following model. Switching between models in a workflow pipeline adds latency, complexity, and cost. Mistral Medium 3.5 targets this operational fragmentation by merging best-in-class coding, reasoning, and instruction-following capabilities into a single 128B dense model with configurable reasoning effort per request.

## Method
**Mistral Medium 3.5 (128B)** (Mistral AI, April 30, 2026) is a 128B dense transformer model replacing Mistral Medium 3.1, Magistral (reasoning), and Devstral 2 (coding) — three previously separate models unified into one. Key features include:
- **Architecture:** Mistral3 dense transformer, 128B parameters, BF16 and FP8 precision
- **Context window:** 256K tokens
- **Multimodal input:** Text + image (variable size/aspect ratio)
- **Configurable reasoning effort:** `reasoning_effort="none"` (fast) or `reasoning_effort="high"` (deliberate, complex tasks/agents) — adjustable per request without model switching
- **Native function calling:** JSON-structured tool use
- **24+ languages** including English, Chinese, Japanese, Korean, Arabic, and major European languages
- **Modified MIT licence** — open for commercial deployment
- **EAGLE speculative decoding model** available for 2× inference speedup

## Benchmarks / Datasets

| Benchmark | Mistral Medium 3.5 | Category |
|---|---|---|
| τ³-Telecom | **91.4%** | Industry/Agentic |
| SWE-Bench Verified | **77.6%** | Software Engineering |
| Instruction following | Best-in-class (reported) | General |
| Reasoning (math) | Top tier (reported) | Reasoning |

## Key Results

- **91.4% on τ³-Telecom — highest reported score on this industry-specific agentic benchmark**, reflecting strong performance in structured multi-step enterprise workflows
- **77.6% SWE-Bench Verified** — competitive coding performance; Mistral reports this surpasses all prior Devstral coding models
- **Single model replaces three** (Medium 3.1 + Magistral + Devstral 2): operational simplification without capability compromise
- Per-request `reasoning_effort` switching eliminates the need to route between reasoning and non-reasoning models — fast replies for simple tasks, deliberate reasoning for complex ones in the same deployment
- EAGLE speculative decoding reduces inference latency significantly for high-throughput deployments
- Vision capability with variable-size image handling enables multimodal agent tasks in a single model

## Enterprise / Industry Relevance
Mistral Medium 3.5's consolidation of reasoning, coding, and instruction-following into a single 128B model is highly relevant for Foxconn's FoxBrain infrastructure planning. Currently deploying multiple specialised models for different task types creates routing complexity and inconsistent context. Medium 3.5's per-request `reasoning_effort` parameter allows FoxBrain to use the same model for both high-volume routine queries (`reasoning_effort="none"`, fast and cheap) and complex agentic tasks (`reasoning_effort="high"`, deliberate) — reducing infrastructure complexity while maintaining capability coverage. The 91.4% τ³-Telecom score is particularly relevant for Foxconn's telecom manufacturing (iPhone/network infrastructure assembly) where structured multi-step workflow automation is a core use case. The 256K context window supports full engineering documentation ingestion. Modified MIT licence enables direct commercial deployment without licensing friction.

---
*Back to [Main Digest](../README.md)*
