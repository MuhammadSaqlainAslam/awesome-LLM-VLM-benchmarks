# MedSkillAudit: A Domain-Specific Audit Framework for Medical Research Agent Skills (2026)

## Problem
Managed Agent platforms enable deployment of specialised AI skills for medical research, but there is no standardised methodology for auditing those skills before release — assessing scientific integrity, methodological validity, reproducibility, and boundary safety. Without rigorous pre-deployment audit, medical research agents risk propagating flawed methodologies at scale, with patient safety and scientific credibility implications.

## Method
**MedSkillAudit** (arXiv: 2604.20441, April 23, 2026) introduces skill-auditor@1.0, a layered audit framework for evaluating medical research agent skills across five critical dimensions: scientific integrity, methodological validity, reproducibility, boundary safety, and general quality. The system evaluates 75 skills distributed across five medical research categories (15 skills per category), using an LLM-as-auditor approach with rubric-based scoring. Intraclass Correlation Coefficient (ICC) is used to compare system agreement against human inter-rater baselines.

Authors: Hou et al.

## Benchmarks / Datasets
- 75 medical research agent skills across five categories (15 per category)
- Categories include Protocol Design, Academic Writing, and other medical research domains
- Rubric-based scoring across five audit dimensions: scientific integrity, methodological validity, reproducibility, boundary safety, quality
- ICC measurement against human inter-rater baseline (ICC = 0.300)
- Limited Release threshold defined for deployment gating

## Key Results

| Metric | Value |
|---|---|
| Mean consensus quality score | 72.4 (SD = 13.0) |
| Skills below Limited Release threshold | 57.3% |
| System ICC(2,1) | 0.449 (vs. human baseline 0.300) |
| Best category agreement (Protocol Design) | ICC = 0.551 |
| System divergence from consensus (SD) | 9.5 (vs. between-expert SD of 12.4) |

- **57.3% of evaluated skills fall below the Limited Release threshold, demonstrating that a majority of current medical research agent skills are not deployment-ready without further validation**
- MedSkillAudit achieves ICC(2,1) = 0.449, exceeding the human inter-rater baseline of 0.300, making it a more consistent evaluator than individual human experts
- System disagreement (SD = 9.5) is smaller than between-expert human disagreement (SD = 12.4), confirming the framework's reliability advantage
- Academic Writing category reveals rubric-expert misalignment, indicating that audit rubrics must be domain-calibrated rather than universal

## FoxBrain Relevance
Foxconn's managed AI skill deployments for manufacturing process design, equipment maintenance protocols, and supply chain analytics face analogous pre-deployment auditing challenges to medical research skills. MedSkillAudit's skill-auditor@1.0 framework provides a directly adaptable template: replacing medical research dimensions (scientific integrity, reproducibility) with Foxconn-specific dimensions (manufacturing compliance, safety regulation adherence, process reproducibility). The finding that 57.3% of skills are deployment-unready provides a realistic baseline expectation for FoxBrain skill pipelines — motivating systematic pre-release auditing rather than ad-hoc testing. The ICC-based consistency measurement also gives the FoxBrain team a principled methodology for comparing automated audits against Foxconn domain-expert reviews.

---
*Back to [Main Digest](../README.md)*
