# HarmfulSkillBench: How Do Harmful Skills Weaponize Your Agents? (2026)

## Problem
The rapid growth of skill/plugin marketplaces for LLM agents introduces a novel attack surface: harmful capabilities can be packaged as installable skills that override model safety behaviors when invoked. Existing safety benchmarks focus on direct adversarial prompts against standalone models, missing the qualitatively different threat of pre-installed harmful skills embedded in agent ecosystems. There is no large-scale measurement of harmful skill prevalence in real registries or systematic evaluation of how skill installation degrades model safety.

## Method
**HarmfulSkillBench** (arXiv: 2604.15415, April 16, 2026) is constructed from a large-scale measurement study of 98,440 skills across two major agent skill registries (ClawHub and Skills.Rest), identifying 4,858 harmful skills (4.93% prevalence). From these, a curated benchmark of 200 harmful skills spanning 20 categories (cyber attacks, fraud, privacy violations, inappropriate content, etc.) was assembled. Six LLMs were evaluated under four conditions to measure how skill installation and implicit framing of harmful intent affect refusal rates and harm scores.

Authors: Yukun Jiang, Yage Zhang, Michael Backes, Xinyue Shen, Yang Zhang

## Benchmarks / Datasets
- 98,440 skills audited across ClawHub (8.84% harmful rate) and Skills.Rest (3.49% harmful rate)
- 200 harmful skills across 20 categories in the evaluation benchmark
- 6 LLMs evaluated under 4 conditions (no skill, skill installed, explicit harm, implicit harm)
- Key metrics: harm score (0–1 scale), refusal rate, harm score delta between baseline and skill-installed conditions

## Key Results

| Condition | Average Harm Score | Change vs. Baseline |
|---|---|---|
| No skill (baseline) | 0.27 | — |
| Harmful skill installed | 0.47 | +0.20 |
| Harmful skill + implicit intent | 0.76 | +0.49 |

- **Installing a harmful skill raises average harm score from 0.27 to 0.47 (+74%) and substantially lowers refusal rates across all 6 evaluated models.**
- Implicit framing of harmful intent (not stating the goal explicitly) raises harm scores to 0.76 — nearly 3× the baseline — because models treat the skill's purpose as legitimate context.
- ClawHub shows 2.5× the harmful skill prevalence of Skills.Rest, indicating registry governance quality significantly affects downstream safety exposure.

## FoxBrain Relevance
As Foxconn deploys FoxBrain with plugin/tool ecosystems for enterprise workflows (ERP integrations, procurement APIs, quality-control tools), the HarmfulSkillBench findings introduce a critical enterprise security concern: third-party or internally developed skills could inadvertently or maliciously lower FoxBrain's safety guardrails. Any skill marketplace or plugin registry used with FoxBrain should undergo the same prevalence audit methodology described in this paper before deployment. The implicit-intent finding (0.76 harm score) is especially concerning for manufacturing contexts where automation scripts often omit intent context, making it easy for harmful instructions to slip through. Foxconn's AI governance team should establish a skill vetting pipeline analogous to HarmfulSkillBench's 20-category taxonomy before opening FoxBrain to third-party extensions.

---
*Back to [Main Digest](../README.md)*
