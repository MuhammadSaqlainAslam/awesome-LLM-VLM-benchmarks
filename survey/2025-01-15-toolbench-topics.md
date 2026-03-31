# ToolBench — Benchmark Topic Organization

> **Paper:** [ToolBench: Facilitating Large Language Models in Mastering 16000+ Real-world APIs](https://arxiv.org/abs/2307.16789)
> **Date Added:** 2025-01-15
> **Back to:** [Main Digest](../README.md) | [ToolBench Notes](./2025-01-15-toolbench.md)

---

## What Kind of Benchmark is ToolBench?

ToolBench is an **Agentic Tool-Use Benchmark** for LLMs. It evaluates a model's ability to autonomously select, invoke, sequence, and recover from failures across a massive, open-ended set of real-world APIs — not just answer questions.

---

## Benchmark Taxonomy

### 1. Primary Category: Agentic / Tool-Use Evaluation

| Dimension | What is Tested |
|---|---|
| **Tool Selection** | Can the model choose the right API from 16,459 candidates given a user instruction? |
| **Parameter Generation** | Can it correctly populate API parameters (types, formats, required fields)? |
| **Multi-step Sequencing** | Can it chain multiple API calls in the correct order to complete a complex task? |
| **Error Recovery** | Can it backtrack and retry a different API when a call fails (via DFSDT)? |
| **Zero-shot Generalization** | Can it use APIs it has never seen during training (G2: Unseen Tools, G3: Unseen Domains)? |

---

### 2. Dataset Split Structure

| Split | Description | Challenge Level |
|---|---|---|
| **G1 — Instruction Tuning** | APIs seen during training; tests instruction-following fidelity | Medium |
| **G2 — Unseen Tools** | New APIs in known domains; tests in-domain generalization | Hard |
| **G3 — Unseen Domains** | Completely new domains; tests out-of-distribution robustness | Very Hard |

---

### 3. Evaluation Dimensions (ToolEval)

| Metric | What It Measures |
|---|---|
| **Pass Rate** | Did the model complete the task successfully end-to-end? |
| **Win Rate** | Head-to-head comparison between two models judged by GPT-4 |
| **Solvable Pass Rate (SoPR)** | Pass rate restricted to tasks GPT-4 itself can solve (fairness filter) |
| **Solvable Win Rate (SoWR)** | Win rate on solvable tasks only |

---

### 4. Capability Tags (Cross-reference with Other Benchmarks)

| Tag | Covered by ToolBench? | Related Benchmarks |
|---|---|---|
| `tool-use` | **Yes — primary focus** | ToolBench |
| `multi-step reasoning` | **Yes** | LiveBench, GPQA Diamond |
| `instruction following` | **Yes** | MM-IFEngine, SteerEval |
| `agentic behavior` | **Yes** | SWE-bench, OSWorld |
| `zero-shot generalization` | **Yes (G2/G3)** | LemmaBench |
| `code generation` | Partial (API params) | SWE-bench |
| `vision/multimodal` | **No** | CoW-Bench, OmniDocBench |
| `multilingual` | **No** | SemEval-26 |
| `document parsing` | **No** | OmniDocBench, olmOCR |

---

### 5. Benchmark Positioning in the Agentic Landscape

```
Low Complexity ──────────────────────────────────► High Complexity
    │                                                    │
  QA / MCQ         Instruction          Tool Use     Full OS Agent
 (GPQA, HLE)      Following         (ToolBench)    (OSWorld, SWE-bench)
                (MM-IFEngine)
                                        ▲
                                  ToolBench sits here:
                                  Open-world API calls
                                  with multi-step planning
                                  and error recovery
```

---

### 6. Strengths & Limitations

| Aspect | Strength | Limitation |
|---|---|---|
| **Scale** | 16,459 real APIs (largest at time of publication) | Live APIs may deprecate; benchmark can go stale |
| **Realism** | Uses actual RapidAPI endpoints | No adversarial/injection testing of API responses |
| **Training Data** | DFSDT enables sophisticated exploration | DFSDT adds inference-time cost |
| **Evaluation** | GPT-4 as judge scales cheaply | Judge bias; GPT-4 performance changes over time |
| **Generalization** | G2/G3 splits test OOD robustness | Domain coverage skews toward web/consumer APIs |

---

### 7. FoxBrain Action Items

- [ ] Implement **DFSDT-style backtracking** in FoxBrain's tool orchestration layer
- [ ] Build an internal equivalent of **G2/G3** splits using Foxconn-specific enterprise APIs
- [ ] Supplement ToolEval with an **adversarial API response** test suite (prompt injection via tool output)
- [ ] Re-evaluate ToolBench scores using a **frozen API snapshot** to track real model progress over time

---

*Back to [Main Digest](../README.md)*
