# Policy Invariance: A Reliability Test for LLM Safety Judges Beyond Accuracy (2026)

## Problem
LLM safety judges are used to evaluate whether agent systems behave safely — but existing safety benchmarks measure only verdict accuracy, not verdict consistency. A judge that produces correct verdicts on average can still flip its decision when the evaluation instructions are rephrased without changing their meaning. This conflates what the agent actually did with how the evaluator was prompted, producing safety scores that reflect evaluator prompt sensitivity rather than agent behaviour. No principled test existed to audit whether safety judges produce policy-invariant verdicts.

## Method
**Policy Invariance** (arXiv: 2605.06161, May 2026) introduces the concept of **policy invariance** for safety judge reliability — the requirement that semantically equivalent evaluation framings produce the same verdict. Three testable principles are formalised: (1) rubric semantics consistency, (2) threshold consistency, and (3) ambiguity calibration. These are operationalised through content-preserving policy rewrites applied to the ASSEBench and R-Judge benchmark evaluation protocols. **Four agent-class safety judges** are evaluated, and the **Policy Invariance Score** and **Judge Card** reporting protocol are introduced as standardised reliability audit tools.

## Benchmarks / Datasets
- ASSEBench and R-Judge (existing safety benchmarks re-evaluated for invariance)
- Four agent-class safety judges
- Content-preserving policy rewrite methodology
- Three invariance principles: rubric semantics / threshold / ambiguity calibration
- Policy Invariance Score + Judge Card reporting protocol

## Key Results

| Metric | Result |
|---|---|
| Verdict flip rate from content-preserving rewrites | Up to **9.1%** above baseline variation |
| Verdict changes on unambiguous cases after rewrites | **18–43%** |
| Reliability spread across judges | **Order-of-magnitude difference** |
| Verdict flips captured by accuracy metrics | **Not detected** |

- **Content-preserving policy rewrites flip up to 9.1% of verdicts above baseline — simply rephrasing evaluation instructions changes safety verdicts without changing what the agent did**
- **18–43% of verdict changes occur on unambiguous cases** — judges are inconsistent not just on borderline scenarios but on clear-cut ones
- An order-of-magnitude spread in reliability exists across safety judges that accuracy metrics completely miss
- Policy Invariance Score and Judge Card provide the first standardised framework for auditing and reporting LLM safety judge reliability

## Enterprise / Industry Relevance
FoxBrain's quality assurance and compliance workflows use LLM-as-judge to evaluate whether generated outputs meet safety and policy standards. Policy Invariance's finding that verdict flip rates of 18–43% occur on unambiguous cases after content-preserving evaluation prompt rewrites means FoxBrain's safety judges are producing verdicts that depend substantially on how evaluation instructions are worded, not just on what the evaluated output contains. For Foxconn's compliance-critical use cases — evaluating FoxBrain outputs for regulatory compliance, supplier code-of-conduct adherence, or worker safety policy conformance — an unreliable safety judge that flips decisions based on prompt phrasing is a systemic governance risk. FoxBrain's safety evaluation pipeline must be audited using Policy Invariance Score before any safety judge is used in a compliance-critical workflow, and Judge Cards should be required for any externally sourced safety judge integrated into FoxBrain's infrastructure.

---
*Back to [Main Digest](../README.md)*
