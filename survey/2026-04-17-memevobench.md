# MemEvoBench: Benchmarking Memory MisEvolution in LLM Agents (2026)

## Problem
LLM agents that maintain persistent memory over long horizons are increasingly deployed in production, but a new safety risk has emerged: memory misevolution, where adversarial or simply biased information accumulates in agent memory and gradually corrupts behavior. Existing safety benchmarks test resilience to single-turn adversarial inputs, not to the slow drift of safety degradation over extended memory updates. There is no benchmark specifically measuring how agents' safety properties change under sustained biased memory injection.

## Method
**MemEvoBench** (arXiv: 2604.15774, April 17, 2026) constructs two task types: QA-style tasks spanning 7 domains with 36 risk categories, and workflow-style tasks adapted from 20 safety-focused agent environments with simulated noisy tool outputs. The benchmark injects adversarial memory (biased information, corrupted tool returns, and prejudiced feedback) across multi-turn interactions and measures cumulative safety degradation. Representative LLMs were evaluated, and the inadequacy of static prompt-based defenses was demonstrated.

Authors: Weiwei Xie, Shaoxiong Guo, Fan Zhang, Tian Xia, Xue Yang, Lizhuang Ma, Junchi Yan, Qibing Ren

## Benchmarks / Datasets
- QA-style tasks: 7 domains, 36 risk categories
- Workflow-style tasks: adapted from 20 safety-focused agent environments
- Adversarial injection types: biased memory updates, corrupted tool returns, prejudiced feedback
- Multiple representative LLMs evaluated
- Key metrics: safety degradation rate over memory turns, static-defense efficacy, risk category coverage

## Key Results

| Defense Type | Effectiveness Against Memory MisEvolution | Notes |
|---|---|---|
| Static prompt-based defenses | Insufficient | Cannot address dynamic memory drift |
| No defense | Substantial safety degradation | All tested LLMs affected |

- **All evaluated LLMs exhibit substantial safety degradation under sustained biased memory updates — memory misevolution is a universal vulnerability, not a model-specific one.**
- Static prompt-based defenses (system prompts, safety instructions) are proven insufficient to counteract adversarial memory injection, as they do not adapt to evolving memory content.
- Workflow-style tasks from real safety environments show higher vulnerability than QA tasks, suggesting that action-oriented agentic deployments carry greater risk.

## Enterprise / Industry Relevance
FoxBrain's long-horizon manufacturing agents maintain persistent memory of operational history, supplier interactions, and quality-control records — exactly the accumulation surfaces that MemEvoBench targets. A corrupted memory trace in a procurement agent (e.g., biased historical pricing injected by a compromised supplier API) could silently degrade FoxBrain's safety and accuracy over weeks of operation. Foxconn should evaluate FoxBrain's memory architecture against MemEvoBench's 36-risk-category taxonomy before deploying any persistent-memory agent in production environments. The finding that static prompt defenses are insufficient means Foxconn's AI safety team needs memory-aware monitoring and auditing systems (rather than simply strong system prompts) to detect misevolution in active deployments.

---
*Back to [Main Digest](../README.md)*
