# OfficeBench: Benchmarking Language Agents across Multiple Applications for Office Automation (2024)

## Problem
Existing agent benchmarks evaluate LLMs within a single isolated application (e.g., only a browser, only a code editor), failing to capture the defining challenge of real-world office work: seamlessly switching between multiple applications while maintaining long-horizon goals across the full workflow. No benchmark assessed whether agents could plan and execute realistic multi-application office tasks — the type of work that constitutes the majority of knowledge worker productivity.

## Method
**OfficeBench** (UC San Diego / UCLA / AI2, arXiv: 2407.19056, July 26, 2024) constructs 300 realistic multi-step office tasks requiring agents to orchestrate up to 9 distinct applications inside a Docker environment pre-installed with real office software. Tasks are categorised by cross-application complexity:

- **Single-application (93 tasks):** Actions confined to one app
- **Two-application (95 tasks):** Workflow spans exactly two apps
- **Three-application (112 tasks):** Full cross-app planning across three apps

**9 Applications:** Microsoft Word, Excel, PDF viewer, Calendar, Email, OCR tool, ChatGPT interface, Shell, System utilities

**23 distinct operations** span all nine applications. Evaluation uses three methods matched to task type:
1. **Exact matching** — precise comparison to annotated ground truth
2. **Fuzzy matching** — flexible criteria for tasks with valid alternative outputs
3. **Execution-based evaluation** — custom code snippets validating contextual correctness

Authors: Zilong Wang, Yuedong Cui, Li Zhong, Zimin Zhang, Da Yin, Bill Yuchen Lin, Jingbo Shang (UC San Diego, UCLA, Allen Institute for AI).

## Benchmarks / Datasets
- **300 tasks:** 93 single-app / 95 two-app / 112 three-app
- **9 applications:** Word, Excel, PDF, Calendar, Email, OCR, ChatGPT, Shell, System
- **23 operations** across all apps
- Docker-containerised environment with real office application stack
- **Metrics:** Exact Match / Fuzzy Match / Execution-based Evaluation

## Key Results

| Model | Single-App | Two-App | Three-App | Overall |
|---|---|---|---|---|
| **GPT-4 Omni** | 64.52% | 60.00% | 21.43% | **47.00%** |
| GPT-4 Turbo | 56.99% | 50.63% | 11.61% | 38.00% |
| Llama 3 (70B) | 39.79% | 41.05% | 5.36% | 27.33% |
| Gemini 1.5 Pro | 41.94% | 32.63% | 7.14% | 26.00% |
| Qwen 2 (72B) | 30.23% | 28.42% | 8.04% | 21.16% |
| **Human** | 96.00% | 96.00% | 88.00% | **93.33%** |

- **Best model (GPT-4 Omni, 47.00%) is less than half of human performance (93.33%)** — a massive capability gap for real-world office automation
- Performance degrades sharply with cross-app complexity: GPT-4 Omni drops from 64.52% (1-app) → 60.00% (2-app) → 21.43% (3-app), revealing cross-application planning as the dominant bottleneck
- Primary failure modes: **operation redundancy** (agents loop on the same action) and **hallucinations** (agents invoke actions outside the defined action space)
- Enforcing explicit application-switching (constraining actions to the current app's operation set) improves performance and reduces wasted tokens

## FoxBrain Relevance
OfficeBench directly benchmarks the enterprise automation capabilities most critical to Foxconn's internal productivity goals: multi-application workflows spanning ERP data extraction (Excel), report generation (Word/PDF), email-based approvals, and system-level operations. The 21.43% three-app success rate for the best frontier model reveals that cross-application agentic tasks remain the hardest challenge for FoxBrain deployments. Priority: use OfficeBench's 9-application taxonomy to audit FoxBrain's coverage of Foxconn's internal tool stack (SAP, SharePoint, email, PDF generation) before any enterprise agent deployment. The three-tier complexity structure (1/2/3 apps) provides a progressive qualification framework for FoxBrain agent releases.

---
*Back to [Main Digest](../README.md)*
