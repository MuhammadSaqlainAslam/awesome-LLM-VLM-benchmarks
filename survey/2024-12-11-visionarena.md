# VisionArena: 230K Real World User-VLM Conversations with Preference Labels (2024)

## Problem
The field lacked a large-scale, real-world dataset capturing genuine user preferences when interacting with VLMs. Existing VLM preference benchmarks were small, narrow in scope, or synthetically constructed — failing to reflect the diversity of tasks, languages, and interaction patterns that characterize actual deployment. Additionally, automated VLM leaderboards were biased by confounders such as response verbosity and markdown formatting, inflating scores for models that "look good" rather than perform well.

## Method
VisionArena collects 230K conversations from Chatbot Arena, an open platform where users interact with two anonymized VLMs side-by-side and vote on their preferences. The dataset is organized into three subsets: **VisionArena-Chat** (200K single- and multi-turn conversations), **VisionArena-Battle** (30K paired comparisons with explicit preference votes), and **VisionArena-Bench** (500 diverse prompts for automated evaluation). A style-aware Bradley-Terry model is introduced to debias preference scores by accounting for response length and markdown formatting. The dataset covers 73K unique users, 45 VLMs, and 138 languages across 8 task categories: captioning, OCR, coding, entity recognition, homework, humor, diagram understanding, and creative writing.

## Benchmarks / Datasets
- **VisionArena-Chat:** 200K single/multi-turn conversations
- **VisionArena-Battle:** 30K paired comparisons with preference votes
- **VisionArena-Bench:** 500 diverse prompts for automated VLM ranking
- **Comparison benchmarks:** MMMU, WildVision, LMSYS-Chat-1M, VQA 2.0, DocVQA, ChartQA, TextVQA, WikiArt
- **Scale:** 73K users, 45 VLMs, 138 languages, 8 task categories

## Key Results
- Fine-tuning on VisionArena-Chat yields **+17 points on MMMU** and **+46 points on WildVision** vs LLaVA-Instruct-158K
- **Expert label correlation:** Pearson 0.88, Spearman 0.87
- **User-expert agreement:** 0.72 (excluding ties)
- VisionArena-Bench achieves better alignment with the Chatbot Arena leaderboard (100K+ human votes) than WildVision-Bench
- Key finding: open-ended tasks (captioning, humor) are highly style-dependent; VLMs consistently struggle with spatial reasoning and visual planning
- Accepted at **CVPR 2025**

## FoxBrain Relevance
VisionArena-Chat is a high-quality fine-tuning resource that FoxBrain can leverage for multimodal instruction tuning, particularly for open-ended visual QA tasks relevant to manufacturing (e.g., visual diagram explanation, OCR of engineering documents). The style-aware Bradley-Terry methodology for debiasing leaderboard scores is directly applicable to FoxBrain's internal VLM evaluation infrastructure, preventing verbose or markdown-heavy responses from gaming preference-based quality assessments.

---
*Back to [Main Digest](../README.md)*
