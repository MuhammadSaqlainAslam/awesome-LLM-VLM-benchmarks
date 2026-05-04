# VLM Visual Jailbreak: Attacking Vision-Language Models Through the Visual Modality (2026)

## Problem
Safety alignment for vision-language models is predominantly trained on text — harmful text inputs are refused, but the same harmful content presented through visual encoding can bypass safety guardrails. This cross-modality safety gap means that VLMs deployed in enterprise and public-facing contexts can be manipulated by adversaries who encode harmful instructions visually rather than textually. The gap is poorly characterised and no systematic taxonomy of visual attack vectors existed.

## Method
**VLM Visual Jailbreak** (arXiv: 2605.00583, May 2026; accepted ICML 2026) introduces four novel visual attack methods targeting the visual component of frontier VLMs:
1. **Visual symbol sequences with decoding instructions** — harmful content encoded as visual symbol systems with instructions for the model to decode
2. **Benign object substitution** — replacing harmful objects in requests with visually similar benign ones
3. **In-image text replacement** — replacing text within images while maintaining surrounding context that carries harmful intent
4. **Visual analogy puzzles** — presenting harmful requests as visual pattern-completion tasks

Six frontier VLMs are evaluated across all four attack vectors, with specific quantitative results reported for Claude-Haiku-4.5.

## Benchmarks / Datasets
- Four novel visual attack methods
- Six frontier vision-language models evaluated
- Visual cipher attack vs. equivalent textual cipher attack (controlled comparison)
- Domain: cross-modality safety alignment evaluation
- Publication venue: ICML 2026

## Key Results

| Attack Type | Claude-Haiku-4.5 ASR | Text Equivalent ASR |
|---|---|---|
| Visual cipher attack | **40.9%** | 10.7% |
| Cross-modality safety gap | 3.8× higher via visual | — |

- **Visual cipher attack achieves 40.9% attack success rate (ASR) on Claude-Haiku-4.5 versus only 10.7% for an equivalent textual cipher — the visual modality bypasses safety alignment 3.8× more effectively than the equivalent text attack**
- Safety mechanisms trained on text do not automatically extend to visually-encoded harmful content — visual and textual safety alignment are independent and must be trained separately
- All four attack methods successfully bypass safety measures across multiple tested frontier VLMs
- The attack is zero-shot: no model fine-tuning or adversarial training required — standard image inputs suffice

## Enterprise / Industry Relevance
Foxconn's FoxBrain deployments that accept image inputs — OCR processing of scanned documents, visual inspection queries, engineering diagram analysis — are exposed to the vulnerability this paper documents. Any external party submitting images to FoxBrain could embed visually-encoded harmful instructions in otherwise-legitimate-looking documents (an invoice scan with encoded instructions, a component diagram with hidden text). The 40.9% success rate against a frontier proprietary model (Claude-Haiku-4.5) means this is not a theoretical risk — it is an active attack vector with high success probability. FoxBrain's multimodal deployment security posture must include: (1) sandboxed image processing that limits model actions after visual input, (2) cross-modal consistency checking (does the visual content match the text request?), and (3) human review gates for any high-stakes action triggered by an image-containing request.

---
*Back to [Main Digest](../README.md)*
