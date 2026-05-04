# AgentFloor: How Far Up the Tool-Use Ladder Can Small Open-Weight Models Go? (2026)

## Problem
Enterprise AI deployments default to frontier models for all agentic tasks, assuming that larger models are uniformly better at tool use and multi-step reasoning. This assumption drives unnecessary infrastructure cost and latency. The practical question — at which specific capability tiers do small models match frontier models, and where does the performance gap actually emerge — had not been empirically answered at scale across a structured capability ladder. Without this answer, organisations over-deploy expensive frontier models on tasks where small open-weight models are already sufficient.

## Method
**AgentFloor** (arXiv: 2605.00334, May 2026) introduces a **30-task deterministic benchmark** structured as a **six-tier capability ladder** covering: instruction following → single tool use → multi-tool use → multi-step coordination → long-horizon planning → complex planning with adversarial conditions. Sixteen open-weight models (0.27B to 32B parameters) plus GPT-5 are evaluated, totalling **16,542 scored runs**. The deterministic design ensures reproducibility and eliminates scoring ambiguity.

## Benchmarks / Datasets
- 30 tasks across 6 capability tiers (instruction following → complex long-horizon planning)
- 16 open-weight models: 0.27B to 32B parameters
- 1 frontier model: GPT-5 (as ceiling reference)
- 16,542 total scored runs
- Deterministic benchmark design (reproducible, unambiguous scoring)

## Key Results

| Capability Tier | Small Models vs. GPT-5 |
|---|---|
| Instruction following | Matched by ≥7B models |
| Single tool use | Matched by ≥7B models |
| Multi-tool use | Matched by ≥13B models |
| Multi-step coordination | Matched by best 32B model |
| Long-horizon planning | GPT-5 leads |
| Complex planning + adversarial | GPT-5 leads significantly |

- **The strongest open-weight model matches GPT-5 performance on structured short-horizon tool use while being substantially cheaper and faster — frontier models are over-deployed on routine agentic tasks**
- A clear performance boundary exists: small/mid-sized models handle structured tool use well; frontier models maintain meaningful advantage only on complex long-horizon planning and adversarial conditions
- The performance gap between model sizes is tier-dependent: size matters little on lower tiers, matters a lot on the top two tiers
- 16,542 scored runs confirm statistical robustness — this is not an artefact of small sample evaluation

## Enterprise / Industry Relevance
AgentFloor's six-tier capability ladder provides FoxBrain architects with a direct decision framework for model selection in agentic deployments. Foxconn's agentic use cases span all six tiers: structured data retrieval from ERP (tiers 1-2, small models sufficient), multi-system query orchestration (tier 3-4, mid-size models sufficient), and autonomous supplier negotiation or complex logistics planning (tiers 5-6, frontier model required). Systematically routing tasks to the appropriate tier reduces FoxBrain infrastructure cost significantly: if 70% of Foxconn's agentic queries are tier 1-3 tasks (instruction following and straightforward tool use), those can be handled by a 13B open-weight model at a fraction of frontier model cost, with frontier models reserved for tier 5-6 planning. AgentFloor provides the benchmark to audit this routing assumption before implementing it in production.

---
*Back to [Main Digest](../README.md)*
