# AgentBench: Evaluating LLMs as Agents (2023)

## Problem
The rapid deployment of LLMs as autonomous agents — capable of taking actions, browsing the web, writing and executing code, and interacting with databases — had outpaced rigorous multi-environment evaluation. No benchmark had systematically measured agent performance across diverse real-world task categories, making it impossible to compare models or identify capability gaps.

## Method
AgentBench defines 8 distinct environments spanning three grounding categories: code-grounded (OS, database, knowledge graph), game-grounded (digital card game, lateral thinking puzzles, household tasks), and web-grounded (web shopping, web browsing). Five of the 8 environments were newly created. 29 LLMs are evaluated, with GPT-4 as the top performer. Published at ICLR 2024.

## Benchmarks / Datasets
- **AgentBench:** 8 environments: OS, DB, KG, Digital Card Game, Lateral Thinking Puzzles, ALFWorld (Household), WebShop, WebArena.
- **Categories:** Code-grounded, Game-grounded, Web-grounded.
- **Models Evaluated:** 29 LLMs (commercial and open-source).
- **Metrics:** Task success rate per environment; overall agent score.
- **GitHub:** https://github.com/THUDM/AgentBench

## Key Results
A large gap exists between top commercial models and open-source alternatives — GPT-4 leads significantly, while most open-source models of the time score near zero on web-grounded tasks. **Long-term reasoning** and **instruction-following across multi-step tasks** are identified as the two primary bottlenecks for all evaluated models.

## FoxBrain Relevance
The foundational reference for FoxBrain's agentic evaluation. The 8-environment structure maps directly onto FoxBrain use cases: OS-level automation, database querying, web-based procurement, and knowledge graph traversal. The long-term reasoning bottleneck identified in AgentBench is precisely the capability FoxBrain's RL-based training should target. This benchmark should serve as a baseline before and after every major FoxBrain agent upgrade.

---
*Back to [Main Digest](../README.md)*
