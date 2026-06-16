# Distributed Cross-Attention (LV-XAttn)

## 📋 Overview
LV-XAttn is designed for processing massive visual contexts by distributing KV blocks across multiple GPUs while minimizing communication overhead by only exchanging small Query blocks.

## 🏗️ Architecture Diagram
```mermaid
graph TD
    subgraph GPU1
        K1[KV Block 1]
        Q1[Queries]
    end
    subgraph GPU2
        K2[KV Block 2]
        Q2[Queries]
    end
    Q1 -- Exchange --> K2
    Q2 -- Exchange --> K1
    K1 -- Local --> Attn1[Attention 1]
    K2 -- Local --> Attn2[Attention 2]
```

## 🔍 Key Details
- **First Used:** 2025
- **Primary Benefit:** Enables processing of high-resolution video and long sequences in MLLMs with 10x speedup.
- **Paper:** [LV-XAttn: Distributed Cross-Attention for Long Visual Inputs in Multimodal Large Language Models](https://arxiv.org/abs/2502.02406)

[⬅️ Back to README](../README.md)
