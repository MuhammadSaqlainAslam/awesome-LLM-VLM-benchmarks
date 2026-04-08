# Terminal-Bench: Benchmarking Agents on Hard, Realistic Tasks in Command Line Interfaces (2026)

## Problem
Existing agent benchmarks do not adequately test AI on the kind of hard, end-to-end tasks encountered in real terminal and CLI workflows — they are either too synthetic, too narrow, or easily saturated. There was no benchmark measuring how well AI agents handle genuine, multi-step command-line work that mirrors what a software engineer or system administrator actually does daily.

## Method
Terminal-Bench provides agents with an interactive **tmux session** running inside a sandboxed Docker container via the **Terminus 2** scaffold — the model sends keystrokes to the terminal and can use any available CLI tool. Evaluation is outcome-driven: automated tests verify the final container state, not intermediate commands. An LLM-as-judge (GPT-5, 90% agreement with human annotations) handles subjective aspects. Human reviewers contributed ~3 hours per task with three reviewers each. 32,155 total trials were run across 6 agent scaffolds and 16 frontier models (minimum 5 runs per model-agent combination). The benchmark was built by the **Laude Institute** with contributors from Anthropic, Google DeepMind, OpenAI, Meta AI, Stanford University, and 80+ additional researchers. Published January 2026 (arXiv: 2601.11868).

## Benchmarks / Datasets
- **89 tasks across 10 categories:**
  1. Software Engineering (largest category)
  2. System Configuration
  3. Machine Learning Operations (MLOps)
  4. Scientific Computing
  5. Cybersecurity
  6. Database Management
  7. Video Processing
  8. Personal Assistant Tasks
  9. Binary Reverse Engineering
  10. Research Paper Reimplementation
- **Difficulty:** 48.6% expert-level (<1 hour human); 71.6% junior-level (1–24 hours human)
- **Scale:** 32,155 trials; live leaderboard at tbench.ai

## Key Results (Terminus 2 scaffold, pass rates)

| Model | Pass Rate |
|---|---|
| **Claude Opus 4.5** | **57.8% ± 2.5%** |
| Gemini 3 Pro | 56.9% ± 2.5% |
| GPT-5.2 | 54.0% ± 2.9% |
| Claude Sonnet 4.5 | 42.8% ± 2.8% |
| Kimi K2 Thinking | 35.7% ± 2.8% |
| GPT-OSS-120B | 18.7% ± 2.7% |
| GPT-5-Nano | 7.9% ± 1.9% |

**Current SOTA:** GPT-5.2 + Codex CLI scaffold: **62.9% ± 3.0%**

No model exceeds 65%, confirming substantial headroom. Scaffold choice matters significantly — the right agent framework can add 10+ percentage points over a base model.

## FoxBrain Relevance
Terminal-Bench's Software Engineering, System Configuration, and Scientific Computing categories map directly to FoxBrain's highest-value agentic use cases: automated script writing for factory floor automation, configuration of manufacturing execution systems, and computational analysis for process optimisation. The Docker-sandboxed evaluation methodology provides a safe blueprint for FoxBrain's internal agentic testing — containering model actions before exposing them to live Foxconn infrastructure. The 10-category task taxonomy can serve as a template for Foxconn-specific terminal task assessment (e.g., PLC programming, ERP CLI interactions, sensor data pipelines).

---
*Back to [Main Digest](../README.md)*
