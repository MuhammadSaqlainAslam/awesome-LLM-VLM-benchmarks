# PilotBench: Evaluating LLMs as Safety-Critical Aviation Agents (2026)

## Problem
LLMs are increasingly considered for integration into aviation decision-support systems, but no benchmark evaluated their performance on the specific challenges of safety-critical flight operations: predicting trajectory and attitude across 9 distinct flight phases, adhering to strict aviation safety protocols, and balancing semantic reasoning with physics-governed quantitative predictions. Standard agent benchmarks use forgiving web or code environments where errors are recoverable; aviation tasks require correct predictions in irreversible, high-stakes conditions.

## Method
**PilotBench** (arXiv: 2604.08987, April 10, 2026) evaluates LLMs on **708 real-world general aviation flight trajectories** with **34-channel telemetry data** spanning 9 flight phases (pre-flight, taxi, takeoff, climb, cruise, descent, approach, landing, go-around). The composite **Pilot-Score** metric weights three equally important dimensions:
- **Regression accuracy (60%):** MAE on predicted altitude, heading, airspeed, and vertical rate
- **Instruction adherence (40%):** Compliance with aviation protocol instructions
- **Safety compliance:** Binary penalty for safety protocol violations (hard constraint)

Traditional time-series forecasting methods are compared directly against frontier LLMs to reveal the accuracy-vs-protocol trade-off. Authors: Yalun Wu, Haotian Liu, Zhoujun Li, Boyang Wang.

## Benchmarks / Datasets
- **708 real-world general aviation trajectories**
- **34-channel telemetry data** (altitude, heading, airspeed, vertical rate, engine parameters, etc.)
- **9 flight phases** (pre-flight through go-around)
- **Pilot-Score:** 60% regression MAE + 40% instruction adherence + safety compliance hard constraint
- **Baseline comparison:** Traditional forecasters vs. frontier LLMs

## Key Results

| Model Type | Regression MAE | Instruction Following | Notes |
|---|---|---|---|
| **Traditional forecasters** | **7.01 MAE** (best) | Low | Strong on numerical accuracy |
| **Frontier LLMs** | 11–14 MAE | **86–89%** | Strong on protocol adherence |
| Combined approach | Balanced | Balanced | Paper's proposed direction |

- **Fundamental trade-off identified:** Traditional forecasting methods achieve lower regression MAE (7.01) but poor protocol compliance; frontier LLMs achieve strong instruction following (86–89%) but higher numerical error (11–14 MAE)
- No current system achieves both high quantitative accuracy AND high safety protocol adherence simultaneously
- The go-around phase (aborted landing) is the hardest flight phase for all evaluated models
- LLMs show consistent strength in semantic phase classification but systematic weakness in precise quantitative trajectory prediction

## FoxBrain Relevance
PilotBench defines the safety-critical agent evaluation paradigm directly applicable to FoxBrain's industrial automation deployments: autonomous robotic arm path planning, AGV trajectory control, and CNC machine parameter prediction all share PilotBench's core challenge — LLMs must simultaneously follow semantic operating protocols AND produce quantitatively precise numerical outputs. The identified trade-off (LLMs: good protocols, bad numbers; traditional models: good numbers, bad protocols) suggests FoxBrain's industrial agent architecture should use a hybrid approach: LLM for semantic planning and protocol compliance, traditional control algorithms for precise quantitative actuation. The Pilot-Score composite metric (accuracy + adherence + safety) is directly adaptable as FoxBrain's evaluation framework for manufacturing agent deployments.

---
*Back to [Main Digest](../README.md)*
