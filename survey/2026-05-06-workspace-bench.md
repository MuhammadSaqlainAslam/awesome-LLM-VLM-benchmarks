# Workspace-Bench 1.0: Benchmarking AI Agents on Workspace Tasks with Large-Scale File Dependencies (2026)

## Problem
AI agent benchmarks evaluate tasks in isolation — single files, clean synthetic environments, or limited collections of documents. Real enterprise workspaces involve thousands of interdependent files across diverse types: code repositories linked to documentation, spreadsheets referencing configuration files, presentations depending on data exports, and project plans cross-referencing contracts. No benchmark had evaluated whether agents can navigate and reason across the full, messy, interdependent file ecosystem of a real worker's workspace.

## Method
**Workspace-Bench 1.0** (arXiv: 2605.03596, May 2026) constructs realistic workspaces with **5 worker profiles**, **74 file types**, and **20,476 files (up to 20GB)** with **388 curated tasks** requiring agents to understand and leverage cross-file dependencies. A lighter variant — **Workspace-Bench-Lite** — provides 100 tasks at ~70% lower evaluation cost. **4 agent harnesses** and **7 foundation models** are evaluated, with human performance established as a baseline at 80.7% task success.

## Benchmarks / Datasets
- 5 worker profiles (realistic persona diversity)
- 74 file types across 20,476 files (up to 20GB)
- 388 curated tasks (cross-file dependency awareness required)
- Workspace-Bench-Lite: 100 tasks, ~70% cost reduction
- 4 agent harnesses × 7 foundation models evaluated
- Human baseline: 80.7% task success

## Key Results

| System | Task Success Rate |
|---|---|
| Human workers | **80.7%** |
| Best AI agent | 68.7% |
| Average across all agents | 47.4% |
| Human-AI gap (best agent) | −12 percentage points |
| Human-AI gap (average agent) | −33.3 percentage points |

- **Best AI agent achieves 68.7% vs. human baseline of 80.7% — a 12-point gap that widens to 33 points for average agents on realistic multi-file workspace tasks**
- 74 file type diversity and 20GB workspace scale expose agent failures that small synthetic benchmarks cannot surface
- Average agent performance of 47.4% means typical deployed agents fail on more than half of real workspace tasks
- Workspace-Bench-Lite at 70% cost reduction enables practical iterative agent evaluation without full benchmark overhead

## Enterprise / Industry Relevance
Foxconn's enterprise workspace is exactly the environment Workspace-Bench targets: project engineers maintain repositories of CAD files, specifications, test reports, and procurement records that must be navigated together. A FoxBrain agent tasked with "summarise the compliance status of this project" must traverse linked engineering specs, test reports, regulatory filings, and supplier certificates — all dependent on each other. Workspace-Bench's finding that the best agents achieve only 68.7% on realistic multi-file workspaces means FoxBrain's enterprise workspace agents cannot be trusted to complete multi-file tasks reliably without human verification. The 47.4% average agent success rate also implies that off-the-shelf agent frameworks — without Foxconn-specific workspace context training — will fail on more than half of Foxconn's real cross-file tasks. Workspace-Bench's 5-profile / 74-file-type design is directly adaptable as a Foxconn-specific agent evaluation framework before any workspace automation deployment.

---
*Back to [Main Digest](../README.md)*
