# Cross-Layer Attention (CLA)

## 📋 Overview
Cross-Layer Attention (CLA) is an architectural optimization for Transformers that reduces the KV cache size by sharing Key and Value representations across multiple decoder layers.

## 🏗️ Architecture Diagram
```mermaid
graph TD
    subgraph "Layer N"
        QN[Query N]
        KN[Key]
        VN[Value]
    end
    subgraph "Layer N+1"
        QN1[Query N+1]
        KN1[Shared Key]
        VN1[Shared Value]
    end
    KN --- KN1
    VN --- VN1
    QN --> AttentionN[Attention]
    KN --> AttentionN
    VN --> AttentionN
    QN1 --> AttentionN1[Attention]
    KN1 --> AttentionN1
    VN1 --> AttentionN1
```

## 🔍 Key Details
- **First Used:** 2024
- **Primary Benefit:** Reduces KV cache size by 2x or more with minimal accuracy loss.
- **Paper:** [Reducing Transformer Key-Value Cache Size with Cross-Layer Attention](https://arxiv.org/abs/2405.12981)

[⬅️ Back to README](../README.md)
