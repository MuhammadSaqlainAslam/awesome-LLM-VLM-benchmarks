# Benchmarking Vision Foundation Models for Domain-Generalizable Face Anti-Spoofing (2026)

## Problem
Face Anti-Spoofing (FAS) systems must generalize across unseen environments, attack types, and camera conditions — yet existing benchmarks favor costly Vision-Language Model (VLM) approaches that demand prohibitive compute and exhibit high inference latency. No systematic study had compared the full landscape of vision-only foundation models under severe cross-domain protocols, leaving practitioners without a principled baseline for efficient deployment. This benchmark fills that gap by rigorously evaluating 15 pre-trained architectures under standardized cross-domain stress tests.

## Method
**FAS-VFM Bench** (arXiv: 2604.19196, April 21, 2026) conducts a systematic evaluation of 15 pre-trained vision models — spanning supervised CNNs, supervised ViTs, and self-supervised ViTs — under two challenging cross-domain protocols: MICO (leave-one-dataset-out across four datasets: MSU-MFSD, IDIAP Replay-Attack, CASIA-FASD, OULU-NPU) and Limited Source Domains (LSD). The study pairs the best-performing backbone (DINOv2 with Registers) with Face Anti-Spoofing Data Augmentation (FAS-Aug), Patch-wise Data Augmentation (PDA), and Attention-weighted Patch Loss (APL) to establish a vision-only state-of-the-art baseline at only 87M parameters.

Authors: Mika Feng, Pierre Gallin-Martel, Koichi Ito, Takafumi Aoki

## Benchmarks / Datasets
- **Scale:** 15 pre-trained models; 4 public FAS datasets (MICO protocol: M, I, C, O); LSD protocol subset
- **Tasks/Tracks:** Cross-domain face anti-spoofing generalization (MICO leave-one-out, LSD data-constrained)
- **Models evaluated:** ConvNeXt, ViT-B, EfficientFormer, MobileViT, DeiT-tiny, DeiT-base, Swin Transformer, Data2vec, BEiT, MAE, CLIP, DINO, DINOv2, DINOv2+Registers, DINOv3
- **Metrics:** Half Total Error Rate (HTER %), Area Under Curve (AUC %)

## Key Results

| Protocol | HTER (%) | AUC (%) |
|---|---|---|
| CIO→M | 8.86 | 96.95 |
| OMI→C | 4.49 | 98.92 |
| OCM→I | 9.81 | 96.70 |
| ICM→O | 7.35 | 98.07 |
| **MICO Average** | **7.63** | **97.66** |

- **DINOv2 with Registers consistently outperformed all other backbone architectures, achieving state-of-the-art MICO average HTER of 7.63% at only 87M parameters — versus VLM competitors with 3,100M+ parameters.**
- Self-supervised ViTs (particularly DINOv2+Registers) suppressed attention artifacts and captured fine-grained spoofing cues that supervised models missed.
- Under the data-constrained LSD protocol, the vision-only baseline outperformed existing VLM methods (MI→C: HTER 8.29%, AUC 97.10%; MI→O: HTER 12.11%, AUC 95.36%), demonstrating that heavy multimodal supervision is not necessary for robust generalization.

## Enterprise / Industry Relevance
Physical access control and workforce identity verification are core operational concerns across Foxconn's global manufacturing campuses, where badge-based and biometric systems must resist spoofing attacks (printed photos, 3D masks, replay videos) under diverse lighting and camera conditions. The benchmark's finding that a compact 87M-parameter DINOv2+Registers model matches or exceeds billion-parameter VLM baselines on cross-domain FAS is directly actionable for edge deployment on factory floor terminals and smart-lock hardware where latency and compute budgets are constrained. FoxBrain's computer vision pipeline can adopt the FAS-Aug + PDA + APL training recipe as a lightweight, auditable baseline for on-premise anti-spoofing, avoiding the data-privacy risks of cloud-hosted VLMs processing employee facial data. The systematic 15-model comparison also provides a reusable evaluation protocol for future Foxconn security AI procurement decisions.

---
*Back to [Main Digest](../README.md)*
