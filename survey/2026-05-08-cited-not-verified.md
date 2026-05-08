# Cited but Not Verified: Source Attribution Accuracy in LLM Deep Research Agents (2026)

## Problem
LLM deep research agents generate reports with inline citations that create an appearance of academic rigour — but the citations' factual accuracy is almost never verified. A cited URL that resolves and contains topically relevant content can still support a factually wrong claim. Enterprise and research users who trust AI-generated cited reports are exposed to a compound failure: the source exists, is relevant, and yet the extracted claim is wrong. No systematic evaluation framework had disentangled link validity, relevance, and factual accuracy as independent citation quality dimensions.

## Method
**Cited but Not Verified** (arXiv: 2605.06635, May 2026) introduces a three-dimensional source attribution evaluation framework with an **AST parser** that extracts inline citations from Markdown-formatted LLM reports, retrieves the actual cited content, and enables human or model evaluators to judge each citation along three independent axes: (1) **Link Works** — URL is accessible, (2) **Relevant Content** — cited source is topically related to the claim, (3) **Fact Check** — cited source actually supports the factual claim. **14 closed-source and open-source LLMs** are evaluated. Tool-call scaling effects are measured from 2 to 150 tool calls per report.

## Benchmarks / Datasets
- AST parser for Markdown citation extraction from LLM research reports
- Three evaluation dimensions: Link Works / Relevant Content / Fact Check
- 14 closed-source and open-source LLMs evaluated
- Tool-call scaling analysis: 2 → 150 calls
- Domain: deep research agents, automated report generation

## Key Results

| Metric | Frontier Models | Open-Source Models |
|---|---|---|
| Link Works | **>94%** | Variable |
| Relevant Content | **>80%** | Variable |
| Fact Check accuracy | **39–77%** | <50% success citing |
| Fact Check at 150 tool calls | −42% vs. 2 tool calls | — |

- **Factual accuracy of citations ranges only 39–77% across frontier models — even the best models have roughly one-in-four citations that do not factually support the claim they are attached to**
- Fact Check accuracy drops approximately **42%** as tool calls scale from 2 to 150 — more research depth produces less reliable citations
- Fewer than half of open-source models successfully generate cited reports in one-shot settings at all
- Link validity (>94%) and relevance (>80%) are strong, but both are weak proxies for factual accuracy — a valid, relevant source can still be misrepresented

## Enterprise / Industry Relevance
Foxconn's FoxBrain deep research workflows — generating due diligence reports, supplier analysis documents, regulatory compliance summaries, and technical literature reviews — produce cited content that enterprise users treat as verified. The 39–77% factual accuracy range means that between one-quarter and three-fifths of citations in FoxBrain-generated research reports may misrepresent their sources. For Foxconn's legal, IP, and compliance teams, a fabricated or misrepresented citation in a regulatory filing or patent prior art search has direct legal consequences. The 42% accuracy drop at 150 tool calls is a critical operational finding: FoxBrain's "deep research" mode with many tool calls produces less reliable citations than shallow mode with few calls. FoxBrain's research pipeline must implement source attribution verification — either via human review of sampled citations or automated fact-check tooling — before any cited AI-generated report is submitted for enterprise decision-making.

---
*Back to [Main Digest](../README.md)*
