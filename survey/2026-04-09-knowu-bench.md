# KnowU-Bench: Evaluating Personalized Mobile GUI Agents with Proactive Preference Inference (2026)

## Problem
Mobile GUI agents are increasingly expected to act on behalf of specific users — adapting to individual preferences, workflows, and habits rather than executing generic instructions. Current agent benchmarks evaluate task completion without accounting for personalisation: an agent that completes a task in a way the user dislikes is counted as successful even though it has failed in practice. No benchmark tested three essential capabilities of truly personalised agents: (1) inferring unstated user preferences from context, (2) deciding when to proactively seek user consent before acting, and (3) knowing when to silently proceed without interrupting the user unnecessarily.

## Method
**KnowU-Bench** (arXiv: 2604.08455, April 9, 2026) evaluates mobile GUI agents across **three capability tracks** with **192 total tasks**:

1. **General GUI Execution (42 tasks)** — standard GUI task completion baseline (scrolling, tapping, form filling)
2. **Personalized Tasks (86 tasks)** — tasks where user preference must be inferred from context and history; no explicit preference is stated
3. **Proactive Intervention (64 tasks)** — tasks where the agent must judge whether to: (a) silently proceed, (b) ask for clarification, or (c) refuse and explain — based on ambiguity and risk level

Evaluation uses **rule-based verification** for deterministic GUI actions combined with **LLM-as-Judge composite scoring** for preference alignment and intervention quality. Tested on Claude Sonnet 4.6, GPT-5, Gemini-3.1-Pro, and several other frontier models.

Authors: Tongbo Chen, Zhengxi Lu, Zhan Xu, Guocheng Shao, Shaohan Zhao, Fei Tang, Yong Du, Kaitao Song et al.

## Benchmarks / Datasets
- **192 tasks total:** 42 General GUI + 86 Personalised + 64 Proactive Intervention
- **Evaluation:** Rule-based verification (deterministic) + LLM-as-Judge (preference/intervention quality)
- **Models tested:** Claude Sonnet 4.6, GPT-5, Gemini-3.1-Pro, and others
- **Metrics:** Track-level success rate; preference alignment score; intervention appropriateness score

## Key Results

| Track | Best Model Score | Notes |
|---|---|---|
| General GUI | ~70%+ | Models perform reasonably on standard tasks |
| **Personalized Tasks** | **< 50%** | All frontier models fall below 50% |
| **Proactive Intervention** | **< 50%** | No model clears 50% on vague/risk tasks |

- **Every frontier model — including Claude Sonnet 4.6 and GPT-5 — scores below 50% on preference-inference tasks**, revealing that personalisation is an unsolved problem for mobile GUI agents
- Agents systematically over-interrupt on low-ambiguity tasks (asking unnecessarily) while under-interrupting on high-risk vague tasks (acting without consent when they should pause)
- General GUI execution scores are misleadingly high — removing personalisation context inflates apparent agent capability
- No model shows a consistent strategy for balancing proactive consent-seeking vs. silent execution

## FoxBrain Relevance
KnowU-Bench defines the gap between generic GUI automation and genuinely personalised enterprise agents — directly relevant to FoxBrain deployments where operators have individual workflows, preferences, and risk tolerances on factory floors and in office environments. The <50% personalisation score across all frontier models means FoxBrain cannot be deployed as a "personalised assistant" without explicit preference-learning infrastructure. The proactive intervention failure mode (wrong consent decisions) is particularly critical for manufacturing contexts where over-interruption degrades operator efficiency and under-interruption on high-risk tasks (production parameter changes, lot release decisions) causes quality incidents. Recommended: add explicit user-preference modelling and consent-policy configuration to FoxBrain's GUI agent architecture before any personalised enterprise deployment.

---
*Back to [Main Digest](../README.md)*
