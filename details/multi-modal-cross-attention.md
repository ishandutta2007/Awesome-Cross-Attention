# Multi-Modal Cross-Attention (Dual-Cross-Attention)

## 📋 Overview
Dual-Cross-Attention processes reciprocal Queries from multiple modalities simultaneously, creating a bidirectional flow of information that builds deeper inter-sequence dependencies.

## 🏗️ Architecture Diagram
```mermaid
graph LR
    subgraph Modality1
        Q1[Query 1]
        KV1[KV 1]
    end
    subgraph Modality2
        Q2[Query 2]
        KV2[KV 2]
    end
    Q1 --> Attn2[Attention Modality 2]
    KV2 --> Attn2
    Q2 --> Attn1[Attention Modality 1]
    KV1 --> Attn1
    Attn1 --> Fusion[Final Fusion]
    Attn2 --> Fusion
```

## 🔍 Key Details
- **First Used:** 2025
- **Primary Benefit:** Superior alignment for complex data like single-cell multi-omics or medical imaging.
- **Paper:** [scDiffusion-X](https://www.biorxiv.org/content/10.1101/2025.02.27.640020v1)

[⬅️ Back to README](../README.md)
