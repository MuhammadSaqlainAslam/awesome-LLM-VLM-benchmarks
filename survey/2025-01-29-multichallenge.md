# MultiChallenge: A Realistic Multi-Turn Conversation Evaluation Benchmark (2025)

## Problem
Existing multi-turn conversation benchmarks are too easy — frontier models score near-perfect on them, masking real-world failure modes. No benchmark had previously tested the full set of practical challenges that arise in extended human-AI dialogue: instruction retention, user inference, document editing, and self-consistency under sycophantic pressure.

## Method
MultiChallenge evaluates LLMs across four challenge categories in realistic multi-turn conversations: (1) instruction retention across turns, (2) inference memory of user-provided information, (3) reliable versioned document editing, and (4) self-coherence/avoiding sycophancy. The 273 test conversations (avg. 5 turns, avg. 1,231.7 words each) were synthetically generated and then expert-reviewed. Published in ACL 2025 Findings.

## Benchmarks / Datasets
- **MultiChallenge:** 273 multi-turn conversations across 4 challenge categories.
- **Avg. Conversation:** 5 turns, 1,231.7 words.
- **Metrics:** Category-level accuracy; overall pass rate; sycophancy resistance score.
- **GitHub:** https://github.com/ekwinox117/multi-challenge
- **Leaderboard:** https://scale.com/leaderboard/multichallenge

## Key Results
Despite near-perfect scores on prior multi-turn benchmarks, **all frontier models score below 50%** on MultiChallenge. The best performer, Claude 3.5 Sonnet, achieved only **41.4%**. Versioned document editing and sycophancy resistance are the hardest categories across all models.

## FoxBrain Relevance
Directly relevant for any FoxBrain deployment in extended user sessions — customer support, iterative document drafting, or multi-step project coordination. The 41.4% ceiling on frontier models is a sobering baseline; FoxBrain must be explicitly evaluated on all four MultiChallenge categories before production deployment in conversational workflows.

---
*Back to [Main Digest](../README.md)*
