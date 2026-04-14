# BankerToolBench: Evaluating AI Agents on End-to-End Investment Banking Workflows (2026)

## Problem
Investment banking represents one of the highest-value, highest-stakes knowledge-work domains for AI automation — yet no benchmark evaluated whether LLM agents could complete full end-to-end banking workflows as a professional would. Tasks like navigating data rooms, interpreting SEC filings, building Excel financial models, and producing client-ready PowerPoint decks require sustained multi-step reasoning, cross-artifact consistency, and adherence to professional standards that generic agent benchmarks (web navigation, coding) do not test. Without a banking-specific evaluation, teams deploying AI in financial services had no way to assess whether outputs were actually client-ready.

## Method
**BankerToolBench** (arXiv: 2604.11304, April 13, 2026) evaluates AI agents on **end-to-end investment banking workflows** validated by **502 professional bankers**. Workflows include: navigating virtual data rooms, parsing SEC filings (10-K, 10-Q, 8-K), generating Excel financial models (DCF, LBO, comparable company analysis), producing PowerPoint pitch decks, and writing deal summary reports. The complete manual workflow requires approximately **21 hours** per engagement. Outputs are assessed against **100+ rubric criteria** by veteran investment bankers using a **cross-artifact consistency** metric — ensuring that figures cited in the PowerPoint deck match the Excel model and are correctly sourced from the SEC filings.

Authors: Elaine Lau, Markus Dücker, Ronak Chaudhary, Hui Wen Goh.

## Benchmarks / Datasets
- **End-to-end investment banking workflows** (data room → SEC filings → Excel → PowerPoint → report)
- **502 professional bankers** as validators
- **100+ rubric criteria** per workflow
- **~21 hours** of manual work per engagement
- **Metrics:** Rubric-based client-readiness rating; cross-artifact consistency score

## Key Results

| Model | Rubric Pass Rate | Client-Ready Outputs | Notes |
|---|---|---|---|
| **GPT-5.4** | ~50% of rubric criteria | **0%** | Best evaluated model |
| Other frontier LLMs | Lower | 0% | All fail client-readiness |
| Human banker | ~100% | ~95%+ | Baseline |

- **GPT-5.4, the best-performing model, fails approximately 50% of rubric criteria** — and produces **zero client-ready outputs** by professional banker standards
- Cross-artifact consistency is the primary failure mode: figures in PowerPoint decks frequently do not match the Excel models or are incorrectly sourced
- All models show strong performance on individual sub-tasks in isolation but fail when evaluated holistically end-to-end
- The 21-hour manual task duration reveals the practical value ceiling: even a 50%-accurate agent would save significant hours, but zero client-readiness means all outputs require full human rework

## FoxBrain Relevance
BankerToolBench establishes the benchmark for AI performance in high-value financial workflows — directly relevant to Foxconn's M&A analysis, supplier financial due diligence, and capital allocation reporting. The 0% client-ready finding is a critical reality check for FoxBrain's finance automation ambitions: current frontier models cannot be trusted to produce finance outputs without extensive human review, even when individual sub-tasks appear competent. The cross-artifact consistency metric is immediately applicable to FoxBrain's financial report pipeline — verify that figures in executive summaries match the underlying data models before any output reaches stakeholders. The 100+ rubric criteria framework can be adapted as FoxBrain's finance QA checklist.

---
*Back to [Main Digest](../README.md)*
