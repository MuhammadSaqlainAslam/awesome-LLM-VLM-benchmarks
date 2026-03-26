## Problem
LLMs struggle with strict structural fidelity (JSON, XML, LaTeX) when tasks become deeply nested or require specific schema adherence for tool-use.

## Method
**StructEval** tests models across 18 distinct structured formats, requiring the model to generate, transform, and debug code/data while maintaining 100% syntactic correctness.

## Benchmarks / Datasets
- **Benchmark:** StructEval
- **Dataset:** 18 Formats (JSON, YAML, HTML, Mermaid, etc.)
- **Metrics:** Syntax Validity, Schema Fidelity, Field Accuracy

## Key Results
Top-tier models achieve high scores in JSON/YAML but drop to **62% fidelity** when generating complex visual structures like Mermaid diagrams or nested LaTeX tables.

## FoxBrain Relevance
Directly addresses our goal to "Adopt StructEval to verify FoxBrain's JSON-schema generation reliability." This is our primary benchmark for API-calling and data extraction features.
