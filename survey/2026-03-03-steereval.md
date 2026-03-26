## Problem
Evaluating how well an LLM follows specific stylistic or behavioral "steering" (e.g., persona, tone, safety constraints) is often subjective and lacks granular metrics.

## Method
**SteerEval** employs a hierarchical evaluation approach, measuring steering at three levels: high-level intent, mid-level sentiment/personality, and fine-grained linguistic constraints.

## Benchmarks / Datasets
- **Benchmark:** SteerEval
- **Dataset:** 5,000+ behavioral steering prompts
- **Metrics:** Control % (Adherence to constraints), Multi-turn Consistency

## Key Results
The paper shows that while models follow high-level personas well, they fail at "Negative Constraint Steering" (e.g., "don't use the letter 'e'") in **over 40%** of complex reasoning tasks.

## FoxBrain Relevance
Essential for FoxBrain's "Brand Voice" features. If we need our agent to maintain a specific professional persona without slipping, SteerEval is the metric to track.
