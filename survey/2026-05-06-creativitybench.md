# CreativityBench: Evaluating Agent Creative Reasoning via Affordance-Based Tool Repurposing (2026)

## Problem
LLM agent benchmarks evaluate tool use in canonical scenarios — using a calculator to calculate, a search engine to search, a file editor to edit. Real creative problem-solving requires affordance-based reasoning: understanding what a tool *can* do beyond its intended use and repurposing it inventively to solve novel problems (using a ruler as a lever, a microwave as a timer for a non-food task). This capability — reasoning about physical and functional affordances rather than memorised usage patterns — is untested in any existing benchmark despite being essential for agents operating in physical or creative domains.

## Method
**CreativityBench** (arXiv: 2605.02910, May 2026) introduces a knowledge base containing **4,000 entities** and **150,000+ affordance annotations** linking objects, parts, attributes, and actionable uses beyond canonical purposes. From this knowledge base, **14,000 grounded tasks** are generated requiring non-obvious yet physically plausible solutions achieved by repurposing available tools. **10 state-of-the-art LLMs** (closed and open-source) are evaluated. Chain-of-thought (CoT) strategies and scaling are also tested as potential improvements.

## Benchmarks / Datasets
- 4,000 entities with 150,000+ affordance annotations
- 14,000 grounded tasks requiring non-canonical tool repurposing
- 10 state-of-the-art LLMs (closed + open-source)
- CoT strategy evaluation
- Scaling effect analysis (performance vs. model size)

## Key Results

| Finding | Result |
|---|---|
| Object selection (plausible tools) | Models perform adequately |
| Component identification | Models struggle significantly |
| Affordance identification | Models struggle significantly |
| Physical mechanism understanding | Models struggle significantly |
| Scaling effect | **Performance saturates quickly** |
| CoT benefit | **Limited** |

- **Models can select plausible objects but systematically fail at identifying correct components, their affordances, and underlying physical mechanisms — creative tool repurposing requires a depth of physical understanding that current LLMs lack**
- Performance improvements from model scaling saturate quickly — larger models do not solve the affordance reasoning gap
- Chain-of-thought prompting provides limited benefit — the failure is not in reasoning strategy but in knowledge of physical affordances
- General reasoning ability does not reliably transfer to creative affordance discovery, confirming that creative problem-solving is a distinct, underserved capability

## Enterprise / Industry Relevance
Foxconn's manufacturing environment requires constant creative improvisation: when a specific tool is unavailable, engineers must identify what available tools can serve the same function (which is the core of affordance-based reasoning). FoxBrain agents deployed for manufacturing assistance, maintenance planning, or emergency process adaptation need exactly the capability CreativityBench measures. The finding that performance saturates with scaling means Foxconn cannot solve this by deploying a larger FoxBrain model — the gap requires targeted affordance knowledge training, not scale. For FoxBrain's tool-use agent in manufacturing contexts (recommending alternative tools when a specified one is unavailable, identifying repurposing options for surplus equipment), affordance-specific fine-tuning on Foxconn's manufacturing tool catalogue — with explicit part-function-affordance annotations — is more impactful than general capability scaling.

---
*Back to [Main Digest](../README.md)*
