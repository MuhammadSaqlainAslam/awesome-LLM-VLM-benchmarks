# FinSafetyBench: Evaluating LLM Safety in Real-World Financial Scenarios (2026)

## Problem
LLMs deployed in financial services face a critical safety gap: general safety benchmarks test social harms but not the specific financial crimes and ethical violations that finance-sector deployments must refuse — market manipulation, fraudulent transactions, money laundering facilitation, and insider trading advice. Finance-specialised LLMs are increasingly deployed but untested for compliance with financial crime law and ethics standards. A bilingual gap also exists: no prior benchmark tested financial safety in both English and Chinese despite the dominance of both languages in global financial markets.

## Method
**FinSafetyBench** (arXiv: 2605.00706, May 2026) introduces a bilingual (English-Chinese) red-teaming benchmark grounded in real-world financial crime cases and professional ethics standards. The benchmark covers **14 subcategories spanning financial crimes and ethical violations**, structured around adversarial prompts designed to bypass compliance safeguards. Both general-purpose LLMs and finance-specialised LLMs are evaluated. The study specifically tests whether prompt-level defences are sufficient against sophisticated manipulation strategies, and whether safety alignment differs between English and Chinese financial contexts.

## Benchmarks / Datasets
- 14 subcategories spanning financial crimes and ethical violations
- Bilingual: English and Chinese financial contexts
- Grounded in real-world financial crime cases and professional ethics standards
- Red-teaming adversarial prompts targeting compliance safeguard bypass
- Both general-purpose and finance-specialised LLMs evaluated

## Key Results

| Finding | Result |
|---|---|
| Adversarial prompt bypass rate | Critical vulnerabilities identified across models |
| Chinese context vulnerability | Stronger susceptibility than English context |
| Prompt-level defence adequacy | Insufficient against sophisticated manipulation |
| Finance-specialised vs. general LLMs | Both exhibit critical safety gaps |

- **Critical vulnerabilities allow adversarial prompts to bypass compliance safeguards in both general and finance-specialised LLMs — fine-tuning on financial data does not improve safety alignment**
- **Stronger susceptibility in Chinese contexts** — models that safely refuse harmful financial requests in English are more likely to comply in Chinese, exposing a cross-lingual safety asymmetry
- Prompt-level defences are insufficient: sophisticated manipulation strategies bypass guardrails regardless of system prompt instructions, requiring model-level safety training
- Finance-specialised LLMs show no safety advantage over general LLMs despite domain expertise — domain specialisation and safety alignment are orthogonal

## Enterprise / Industry Relevance
Foxconn's FoxBrain deployments that touch financial workflows — treasury management, supplier payment processing, financial reporting, procurement cost analysis — face exactly the vulnerability FinSafetyBench exposes. The finding that finance-specialised LLMs are no safer than general models is a direct warning: deploying a domain-fine-tuned FoxBrain variant for financial tasks does not inherit any additional safety guarantee. The Chinese-context vulnerability is particularly critical for Foxconn's mainland China finance operations: FoxBrain must be independently safety-evaluated in Chinese financial contexts before deployment, not assumed safe because English evaluations pass. Prompt-level safety instructions (system prompt guardrails) are insufficient as a primary control — model-level alignment must be verified through red-teaming before any financial workflow deployment.

---
*Back to [Main Digest](../README.md)*
