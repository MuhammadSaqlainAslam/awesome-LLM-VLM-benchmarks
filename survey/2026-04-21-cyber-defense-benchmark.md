# Cyber Defense Benchmark: Agentic Threat Hunting Evaluation for LLMs in SecOps (2026)

## Problem
Security Operations Center (SOC) analysts must perform threat hunting — proactively searching through system logs to identify malicious activity — a task that requires sophisticated multi-step SQL reasoning over large event databases. Existing cybersecurity benchmarks focus on capture-the-flag puzzles or static QA and do not reflect the operational reality of hunting real attacker campaigns across structured telemetry. No prior benchmark evaluated LLM agents on this critical SecOps workflow.

## Method
**Cyber Defense Benchmark** (arXiv: 2604.19533, April 21, 2026) presents a reinforcement-learning environment in which agents receive Windows event log databases without any guidance and must identify exact timestamps of malicious events by issuing SQL queries, scored against ground-truth labels derived from Sigma detection rules. The benchmark covers 26 campaigns comprising 105 of 106 real attack procedures from the OTRF Security-Datasets corpus, spanning 86 MITRE ATT&CK sub-techniques across 12 tactics.

Authors: Alankrit Chona, Igor Kozlov, Ambuj Kumar

## Benchmarks / Datasets
- 26 real attack campaigns drawn from the OTRF Security-Datasets corpus
- 105 attack procedures covering 86 MITRE ATT&CK sub-techniques across 12 tactics
- Windows event log databases as the primary evaluation artifact
- Models evaluated: Claude Opus 4.6, GPT-5, Gemini 3.1 Pro, Kimi K2.5, Gemini 3 Flash

## Key Results

| Model | Avg Malicious Event Recall | Tactics Cleared (≥50% Recall) |
|---|---|---|
| Claude Opus 4.6 (best) | 3.8% | 5 / 13 |
| GPT-5 | < 3.8% | 0 / 13 |
| Gemini 3.1 Pro | < 3.8% | 0 / 13 |
| Kimi K2.5 | < 3.8% | 0 / 13 |
| Gemini 3 Flash | < 3.8% | 0 / 13 |

- **Best model (Claude Opus 4.6) achieved only 3.8% recall of malicious events on average — far below any operational threshold**
- No model reached the ≥50% recall passing threshold across all 13 evaluated tactics
- Only Claude Opus 4.6 cleared the bar on 5 of 13 tactics; all other four frontier models succeeded on zero tactics

## Enterprise / Industry Relevance
Foxconn operates large manufacturing campuses with extensive IT/OT infrastructure and Windows-based production control systems that generate vast event logs requiring continuous threat monitoring. FoxBrain could be deployed as a SecOps assistant to perform automated threat hunting over factory-floor telemetry; this benchmark directly measures readiness for that task. The near-zero recall rates across all frontier models confirm that specialized fine-tuning on Foxconn-relevant MITRE ATT&CK procedures — particularly for OT environments — is required before any production deployment. The SQL-querying paradigm also aligns with FoxBrain's enterprise data-warehouse integration workflows, making this benchmark a direct proxy for agentic database-reasoning capability.

---
*Back to [Main Digest](../README.md)*
