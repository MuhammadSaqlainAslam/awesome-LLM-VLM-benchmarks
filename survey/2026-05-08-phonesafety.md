# PhoneSafety: Safe, or Simply Incapable? Rethinking Safety Evaluation for Phone-Use Agents (2026)

## Problem
Current safety evaluations for phone-use agents cannot distinguish between two fundamentally different causes of harmless outcomes: genuine safety (the agent recognised the risk and chose the safe action) and incapability (the agent failed to understand the screen or execute any relevant action at all). A phone-use agent that refuses to send a phishing text because it cannot navigate the messaging app produces the same surface-level "safe" outcome as one that understood the risk and deliberately chose not to act. Treating these as equivalent leads to inflated safety scores for agents that are merely less capable — and provides no guarantee of safety when those agents improve their capability in future versions.

## Method
**PhoneSafety** (arXiv: 2605.07630, May 2026) introduces a benchmark isolating **700 safety-critical decision moments** drawn from over **130 apps** in real phone interactions. Each instance presents three possible model behaviours: (1) taking the safe action, (2) taking the unsafe action, or (3) failing to act usefully (incapability). This tripartite labelling scheme enables explicit separation of genuine safety from capability failure. **Eight representative phone-use agents** are evaluated, and failure patterns are clustered by visual complexity and operational demand.

## Benchmarks / Datasets
- 700 safety-critical moments from real phone interactions
- 130+ apps (broad coverage of mobile app ecosystem)
- 8 phone-use agents evaluated
- Tripartite outcome labelling: safe action / unsafe action / incapable
- Failure clustering by visual and operational complexity

## Key Results

| Evaluation Dimension | Finding |
|---|---|
| Harmless outcome as safety evidence | Insufficient — confounds genuine safety with incapability |
| General phone-use ability vs. safety | No reliable positive correlation |
| Failure pattern 1 | Wrong choices when the agent is capable of acting |
| Failure pattern 2 | Inaction in visually or operationally complex settings |

- **A harmless phone-agent outcome alone is not sufficient evidence of safety — the PhoneSafety tripartite design reveals that safety and incapability are systematically conflated in existing evaluations**
- Stronger general phone-use capability does not correlate reliably with safer choices at risky moments — capability and safety are independent dimensions that must be evaluated separately
- Two recurring failure patterns emerge: unsafe judgement when the agent can act, and inaction in complex visual settings — each requires different mitigation
- Current safety benchmarks for phone-use agents produce inflated scores by crediting capability failures as safety successes

## Enterprise / Industry Relevance
Foxconn increasingly deploys mobile agents for manufacturing floor operations, quality inspection reporting, and supply chain coordination via mobile interfaces. PhoneSafety's finding that safety scores are inflated by incapability failures is directly relevant to FoxBrain-powered phone agents in factory settings: a FoxBrain agent that "safely" avoids sending incorrect supplier confirmations because it cannot parse the screen is not actually safe — it will pose a risk as screen-parsing capability improves. Foxconn should adopt PhoneSafety's tripartite evaluation framework (safe / unsafe / incapable) in its FoxBrain mobile agent testing protocols to distinguish genuine safety alignment from capability limitations. The finding that visual complexity drives incapability failures is particularly relevant for factory-floor mobile agents operating in visually complex or poorly standardised screen environments.

---
*Back to [Main Digest](../README.md)*
