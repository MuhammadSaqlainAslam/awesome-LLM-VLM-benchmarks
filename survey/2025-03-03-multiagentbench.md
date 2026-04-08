# MultiAgentBench: Evaluating the Collaboration and Competition of LLM Agents (2025)

## Problem
Existing benchmarks either focus on single-agent tasks or are confined to narrow domains, failing to capture the dynamics of multi-agent coordination and competition. There was no unified benchmark that measures both task completion quality and the quality of inter-agent collaboration and competition across diverse, interactive multi-agent scenarios — leaving a gap in understanding how LLMs behave as members of collaborative or adversarial teams.

## Method
MultiAgentBench (implemented as the **MARBLE** framework) provides 6 diverse scenarios spanning both collaborative and competitive multi-agent settings. Each scenario uses **milestone-based Key Performance Indicators (KPIs)** to measure both a **Task Score (TS)** and a **Coordination Score (CS)**. Four coordination topologies are evaluated: **star, chain, tree, and graph**. Three planning strategies are compared: vanilla prompting, chain-of-thought (CoT), group discussion, and cognitive self-evolving planning. Agent count and iteration round ablations are included, and a human evaluation validates the Werewolf competitive scenario. Published at **ACL 2025 (Long Papers)** by the University of Illinois Urbana-Champaign (arXiv: 2503.01935).

## Benchmarks / Datasets
- **6 scenarios, 2 types:**
  - **Collaborative (4):** Research Collaboration (100 test cases), Minecraft Building (100), Database Error Analysis (100), Coding Challenges (100)
  - **Competitive (2):** Werewolf (game simulation), Bargaining (negotiation)
- **4 coordination topologies:** star, chain, tree, graph
- **4 planning strategies:** vanilla, CoT, group discussion, cognitive self-evolving
- **Metrics:** Task Score (TS) + Coordination Score (CS) per scenario via milestone-based KPIs

## Key Results (Task Score / Coordination Score, selected models)

| Model | Research TS/CS | Minecraft TS/CS | Database TS/CS | Coding TS/CS | Bargaining TS/CS | Werewolf TS/CS |
|---|---|---|---|---|---|---|
| Llama-3.1-8B | 80.87% / 52.40% | 6.12% / 54.40% | 34.00% / 40.00% | 59.90% / 67.24% | 72.81% / 73.36% | 12.64% / 60.00% |
| Llama-3.3-70B | 80.00% / 72.00% | 9.15% / 69.00% | 28.50% / 40.00% | 56.60% / 74.40% | 73.15% / 69.56% | 36.33% / 76.30% |
| GPT-3.5-turbo | 70.20% / 55.90% | 5.05% / 63.60% | 45.00% / 60.89% | 55.50% / 76.20% | 71.67% / 72.00% | 15.69% / 75.90% |
| **GPT-4o-mini** | **84.13% / 52.00%** | **33.60% / 61.50%** | **45.00% / 43.22%** | **65.10% / 66.30%** | **74.47% / 74.20%** | 14.06% / 60.10% |

**Coordination topology findings (Research scenario):**
- **Graph** topology: best overall task performance and planning efficiency
- **Star**: comparable task scores to graph
- **Chain**: moderate performance
- **Tree**: worst task performance, highest token consumption

**Planning strategy findings:**
- **Cognitive self-evolving planning**: best coordination scores; improves milestone achievement ~3% vs. baseline
- **Group discussion**: lowest performance across all metrics
- Increasing agents beyond 3 decreases overall KPI in Research scenario — more agents ≠ better

## FoxBrain Relevance
MultiAgentBench's collaborative scenarios — Research Collaboration, Database Error Analysis, and Coding Challenges — directly mirror Foxconn's planned FoxBrain multi-agent deployments: concurrent R&D literature analysis, cross-system database interrogation, and parallel code generation pipelines. The finding that **graph topology outperforms star/chain/tree** provides a concrete architecture recommendation for FoxBrain's multi-agent orchestration design. The KPI split (Task Score vs. Coordination Score) provides a two-dimensional evaluation framework for FoxBrain's agent teams — separating output quality from communication efficiency, which is critical for optimising token cost in production multi-agent workflows.

---
*Back to [Main Digest](../README.md)*
