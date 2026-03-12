/
├── README.md               <-- Main Directory (The "Map")
├── surveys/                <-- Summaries of major LLM/VLM surveys
├── sota-digests/           <-- Folder for your deep-dive papers
│   ├── current-sota.md     <-- Always updated with the #1 models/metrics
│   ├── archive/            <-- Older digests moved here
├── roadmap/                <-- FoxBrain Roadmap & Action Items
└── scripts/                <-- (Optional) Python tools to fetch arXiv links

# awesome-LLM-VLM-benchmarks
A comprehensive repository tracking SOTA LLM/VLM benchmarks, datasets, and evaluation metrics. Features a running digest of research papers and system roadmaps.
# 🏛️ The SOTA LLM/VLM Benchmark Library

A comprehensive, system-first repository tracking the evolution of evaluation for Large Language Models (LLM) and Vision-Language Models (VLM).

## 🚀 Living SOTA Leaderboard (March 2026)
| Domain | SOTA Model | Key Benchmark | Score | Metric |
| :--- | :--- | :--- | :--- | :--- |
| **General Reasoning** | GPT-5.2 / Kimi K2.5 | MMLU-Pro | 90.0+ | Accuracy |
| **Visual Math** | Claude 4.1 Opus | MathVista | 76.1% | Accuracy |
| **Software Eng** | MiniMax M2.5 | SWE-bench | 80.2 | Resolved % |
| **Video Reasoning** | Gemini 2.5 Pro | Video-MME | 75.6% | Accuracy |

---

## 📂 Research Categories

### 1. Vision-Language Foundations (VLM)
Focused on image-text alignment, OCR, and spatial reasoning.
* [MMMU](https://github.com/MMMU-Benchmark/MMMU) - Expert-level multimodal reasoning.
* [MathVista](https://mathvista.github.io/) - Mathematical reasoning in visual contexts.
* [MMBench](https://opencompass.org.cn/mmbench) - Robustness and perception suite.

### 2. Frontier Language Reasoning (LLM)
Focusing on hard-science, coding, and long-context logic.
* [GPQA Diamond](https://arxiv.org/abs/2311.12022) - Graduate-level science (PhD difficulty).
* [LiveCodeBench](https://livecodebench.github.io/) - Real-time competitive coding evaluation.
* [IFEval](https://github.com/google-research/google-research/tree/master/ifeval) - Strict instruction following.

### 3. Agentic & Tool-Use Benchmarks
Evaluating how models interact with the real world.
* [SWE-bench Verified](https://www.swebench.com/) - Real-world GitHub issue resolution.
* [ToolBench](https://github.com/OpenBMB/ToolBench) - Complex API calling and orchestration.

---

## 📝 Running Digest (The Work)
* [Latest SOTA Summary](./sota-digests/current-sota.md) - Our most recent survey of benchmark papers.
* [Historical Archive](./sota-digests/archive/) - Tracking how metrics have evolved since 2024.

## 🦊 FoxBrain Roadmap
*Active integration items for our benchmarking suite.*
- [ ] Implement **RAGAS** for context-retrieval scoring.
- [ ] Adopt **LLM-as-a-Judge** (G-Eval) for open-ended response quality.
