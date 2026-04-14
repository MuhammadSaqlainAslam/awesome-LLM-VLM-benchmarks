# OccuBench: Evaluating LLM Agents on Professional Occupational Tasks with Fault Injection (2026)

## Problem
Most agent benchmarks test generic web navigation or coding tasks that don't reflect the specialised judgment, domain knowledge, and error recovery required by real professional occupations. A medical billing agent, legal document drafter, and financial analyst face fundamentally different challenges — yet no benchmark evaluated LLM agents across a representative breadth of professional domains under realistic fault conditions. Equally important, no benchmark tested whether increased reasoning effort (more compute at inference time) actually improves professional task performance, leaving practitioners without data to guide compute allocation decisions.

## Method
**OccuBench** (arXiv: 2604.10866, April 13, 2026) constructs **100 professional task scenarios** across **10 industries** and **65 specialised domains** using **Language World Models (LWMs)** — LLM-simulated professional environments — as the execution substrate. Three **fault injection types** make tasks realistic:

1. **Explicit faults** — clearly stated errors or inconsistencies in the task materials
2. **Implicit faults** — unstated errors requiring expert domain knowledge to detect
3. **Mixed faults** — combinations of explicit and implicit errors across multiple task documents

Evaluation measures both task completion rate and fault detection/recovery. The benchmark also systematically measures the **reasoning effort scaling effect**: GPT-5.2 is evaluated at minimal, moderate, and maximum reasoning effort levels, revealing the compute-performance trade-off for professional tasks.

Authors: Xiaomeng Hu, Yinger Zhang, Fei Huang, Jianhong Tu.

## Benchmarks / Datasets
- **100 professional task scenarios** across 10 industries / 65 specialised domains
- **3 fault injection types:** Explicit, Implicit, Mixed
- **Language World Models (LWMs)** as simulated professional environments
- **Reasoning effort scaling:** Minimal → Moderate → Maximum (GPT-5.2 evaluated at all levels)
- **Metrics:** Task completion rate; fault detection/recovery rate per fault type

## Key Results

| Model / Condition | Task Completion | Notes |
|---|---|---|
| GPT-5.2 (max reasoning effort) | Baseline + **+27.5 pts** vs. minimal | Largest gain from any agent benchmark |
| GPT-5.2 (minimal reasoning effort) | Baseline | Reference |
| Other frontier LLMs | Varied by domain | Healthcare and legal hardest |

- **GPT-5.2 improves by 27.5 percentage points** when moving from minimal to maximum reasoning effort — the largest single-factor performance gain reported on any professional agent benchmark
- **Implicit fault detection** is consistently the hardest task across all models and domains — agents that perform well at task completion frequently miss unstated errors
- Healthcare and legal scenarios show the lowest task completion rates; financial and administrative tasks are most tractable
- LWM-based simulation provides reproducible evaluation without requiring real professional tool access

## FoxBrain Relevance
OccuBench directly benchmarks FoxBrain's professional domain capabilities across Foxconn's core occupational functions: procurement (finance/contracts), quality engineering (manufacturing/technical), HR (administrative/legal), and regulatory compliance (legal/government). The +27.5pp reasoning effort scaling result is immediately actionable for FoxBrain's deployment strategy — high-stakes professional tasks (compliance review, contract analysis, financial due diligence) should always use maximum reasoning effort, while routine administrative tasks can use lower compute. The implicit fault detection failure mode maps directly onto FoxBrain's most critical risk: missing unstated errors in supplier contracts, quality specifications, or regulatory filings — the category where professional judgment is most irreplaceable.

---
*Back to [Main Digest](../README.md)*
