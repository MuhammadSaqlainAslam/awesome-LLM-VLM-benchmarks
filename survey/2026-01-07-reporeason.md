# RepoReason: Benchmarking Agentic Code Reasoning at the Repository Level (2026)

## Problem
Existing code benchmarks focus on isolated function-level generation, failing to capture the multi-file, stateful reasoning required for real-world repository-level software engineering. Models that score well on HumanEval often cannot simulate the execution state of a complex repository after a sequence of operations.

## Method
RepoReason introduces **Abductive Assertion Verification** — given a repository's execution history, the model must infer the current system state rather than generate code. An execution-driven mutation framework eliminates memorization while preserving semantic depth. Three diagnostic metrics are defined: ESV (execution state volume, measuring reading load), MCL (maximum call length, measuring simulation depth), and DFI (data flow integration, measuring cross-file integration width).

## Benchmarks / Datasets
- **RepoReason Dataset:** 2,492 tasks drawn from real-world repositories.
- **Metrics:** ESV (reading load), MCL (simulation depth), DFI (integration width); overall assertion accuracy.
- **Models Evaluated:** Claude, DeepSeek, and other frontier LLMs.

## Key Results
Evaluations reveal a prevalent **"Aggregation Deficit"** across all frontier models: integration width (DFI) is the primary cognitive bottleneck, not raw reading volume. Claude and DeepSeek both struggle disproportionately with tasks that require synthesizing information across more than three files simultaneously.

## FoxBrain Relevance
Directly relevant for FoxBrain's agentic software engineering use cases. The DFI metric provides a practical diagnostic: before deploying FoxBrain for repository-level tasks, measure its cross-file integration capability on RepoReason tasks representative of target codebases. The abductive verification task format is also a valuable addition to FoxBrain's internal QA pipeline.

---
*Back to [Main Digest](../README.md)*
