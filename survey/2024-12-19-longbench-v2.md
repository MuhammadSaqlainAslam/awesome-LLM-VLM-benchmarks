# LongBench v2: Towards Deeper Understanding and Reasoning on Realistic Long-Context Multitasks (2024)

## Problem
Existing long-context benchmarks — including LongBench v1 — can often be solved with surface-level retrieval or short-context heuristics, failing to test genuine deep reasoning over extended documents. There was no challenging, human-validated benchmark requiring true understanding and multi-step reasoning over documents up to 2 million words, with difficulty levels calibrated against real human performance under time pressure.

## Method
503 multiple-choice questions were curated by ~100 highly educated annotators from diverse professional backgrounds using combined automated and rigorous manual review. Each question has a single unambiguous correct answer from 4 options. Context lengths range from **8K to 2,000,000 words**, organised into three difficulty buckets: **short (0–32K)**, **medium (32K–128K)**, and **long (128K–2M)**. A human baseline was established under a realistic 15-minute time constraint. Tasks span 6 categories. Published at **ACL 2025 (main conference, Long Papers)** from Tsinghua University's THUDM group.

## Benchmarks / Datasets
- **503 multiple-choice questions (4-option, single correct answer)**
- **Context range:** 8,000–2,000,000 words (3 difficulty buckets: Short / Medium / Long)
- **6 task categories:**
  1. Single-document QA
  2. Multi-document QA
  3. Long in-context learning
  4. Long-dialogue history understanding
  5. Code repository understanding
  6. Long structured data understanding
- **Human baseline:** 53.7% accuracy under 15-minute time limit

## Key Results

**At paper release (December 2024):**

| Model | Accuracy |
|---|---|
| Human experts (15-min) | 53.7% |
| o1-preview | **57.7%** |
| Best direct-answering model | 50.1% |

**Current leaderboard (April 2026):**

| Model | Accuracy |
|---|---|
| **Gemini 2.5 Pro** | **63.3%** |
| Gemini 2.5 Flash | 62.1% |
| Qwen3-235B-A22B-Thinking | 60.6% |
| DeepSeek-R1 | 58.3% |

At release, frontier models could barely match human performance under time pressure (57.7% vs 53.7%). By April 2026, Gemini 2.5 Pro has pushed to **63.3%**, exceeding the human baseline — but the benchmark is deliberately harder than humans can solve perfectly in 15 minutes, leaving significant headroom.

## FoxBrain Relevance
LongBench v2's "code repository understanding" and "long structured data understanding" categories are directly applicable to FoxBrain's use case — parsing large Foxconn software codebases, multi-hundred-page technical specifications, and long structured BOM/ERP export files. The medium context tier (32K–128K) represents the most practically relevant range for FoxBrain's factory floor document library; performance in this tier should be the primary gating metric before deploying FoxBrain on multi-document reasoning tasks. The human baseline (53.7% under time pressure) provides a realistic production target.

---
*Back to [Main Digest](../README.md)*
