# SpatialEpiBench: Benchmarking Spatial Information and Epidemic Priors in Forecasting (2026)

## Problem
Epidemic forecasting models that incorporate spatial information and domain epidemiological priors are assumed to outperform naive baselines — this assumption underpins substantial public health investment in spatiotemporal AI systems. No standardised benchmark existed to rigorously test this assumption across diverse epidemic datasets, leaving the field without reproducible evidence that increasingly complex spatial models actually improve over simple alternatives. When AI forecasting systems are deployed for public health response without this evidence, flawed models may mislead resource allocation during outbreaks.

## Method
**SpatialEpiBench** (arXiv: 2605.06530, May 2026) introduces a benchmark of **11 epidemic datasets** with **standardised rolling evaluations** and **outbreak-specific metrics** designed to reflect real-time forecasting scenarios rather than retrospective chronological splits. The benchmark tests adjacency-informed forecasting models incorporating widely used epidemic priors against a simple last-value baseline across forecasting horizons from 1 day to 1 month ahead. Three failure modes are systematically characterised across the tested models.

## Benchmarks / Datasets
- 11 epidemic datasets
- Standardised rolling evaluation protocol (real-time forecasting realism)
- Outbreak-specific evaluation metrics
- Forecasting horizons: 1 day to 1 month ahead
- Adjacency-informed spatiotemporal models + epidemic priors tested
- Simple last-value baseline as comparator

## Key Results

| Condition | Finding |
|---|---|
| Spatiotemporal models vs. last-value baseline | **Most underperform** baseline at all horizons |
| During outbreak periods | **Underperformance sustained** |
| With epidemic priors applied | **Limited improvement** |
| Failure mode 1 | Poor outbreak anticipation |
| Failure mode 2 | Difficulty managing sparsity and noise |
| Failure mode 3 | Geographic adjacency provides limited signal |

- **Most evaluated spatiotemporal epidemic models underperform a simple last-value baseline from 1 day to 1 month ahead — complex spatial modelling does not improve outbreak forecasting**
- Epidemic priors applied to general spatiotemporal models provide limited improvement, challenging the assumption that domain knowledge integration improves AI forecasting reliability
- Geographic adjacency contributes limited useful spatial signal for epidemiological prediction — proximity-based spread assumptions are weaker than expected
- Three systematic failure modes characterise all models: poor outbreak anticipation, data sparsity/noise sensitivity, and weak geographic adjacency utility

## Enterprise / Industry Relevance
Foxconn operates across 200+ global locations and is directly affected by epidemic outbreaks (COVID-19 severely impacted Foxconn's production lines). Any FoxBrain deployment for workforce health monitoring, factory operational risk assessment, or supply chain disruption prediction that incorporates epidemic forecasting must grapple with SpatialEpiBench's finding: complex spatiotemporal AI models are less reliable than simple trend extrapolation for epidemic prediction. For Foxconn's supply chain resilience planning, this means AI-generated epidemic risk forecasts for regional supplier clusters or factory locations should be validated against simple last-observation baselines before being treated as more reliable than naive extrapolation. The finding that geographic adjacency provides limited signal is also relevant for Foxconn's COVID-style operational planning: proximity-based risk propagation assumptions in AI models are empirically weak and should not be trusted without specific validation on historical Foxconn operational data.

---
*Back to [Main Digest](../README.md)*
