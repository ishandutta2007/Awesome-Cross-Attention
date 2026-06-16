<!-- 
SEO Keywords: Cross-Attention, Transformer Architecture, Deep Learning, AI, Large Language Models, LLM Optimization, KV Cache, Multi-Modal AI, Flamingo, LV-XAttn, CLA, GCA
-->

<div align="center">
  <img src="assets/banner.svg" alt="Awesome Cross-Attention Banner" width="100%" />

  <p align="center">
    <a href="https://github.com/ishandutta2007/Awesome-Cross-Attention/stargazers"><img src="https://img.shields.io/github/stars/ishandutta2007/Awesome-Cross-Attention?style=for-the-badge&color=yellow" alt="stars" /></a>
    <a href="https://github.com/ishandutta2007/Awesome-Cross-Attention/network/members"><img src="https://img.shields.io/github/forks/ishandutta2007/Awesome-Cross-Attention?style=for-the-badge&color=blue" alt="forks" /></a>
    <a href="https://github.com/ishandutta2007/Awesome-Cross-Attention/blob/main/LICENSE"><img src="https://img.shields.io/github/license/ishandutta2007/Awesome-Cross-Attention?style=for-the-badge&color=green" alt="license" /></a>
    <a href="https://github.com/ishandutta2007"><img alt="GitHub followers" src="https://img.shields.io/github/followers/ishandutta2007?label=Follow&style=for-the-badge&color=orange" /></a>
  </p>
</div>

# 🌟 Awesome-Cross-Attention

## 🚀 Cross-Attention Mechanisms & Key Variants

Cross-attention enables one data sequence (e.g., text) to query information from another separate sequence (e.g., an image or a different language). While the core mechanism relies on scaled dot-product attention, several specialized variants optimize how different data domains interact. 🧠✨

---

## 🛠️ Top Variants of Cross-Attention

| Variant | Description | Year | Paper Link |
| :--- | :--- | :--- | :--- |
| [**Cross-Layer Attention (CLA)**](details/cross-layer-attention.md) | Shares the same Keys (K) and Values (V) across multiple sequential decoder layers rather than recalculating them. This drastically reduces the KV cache size, memory footprint, and overall compute requirements in large models. 📉 | 2024 | [Reducing Transformer Key-Value Cache Size with Cross-Layer Attention](https://arxiv.org/abs/2405.12981) |
| [**Gated Cross-Attention (GCA)**](details/gated-cross-attention.md) | Fuses heterogeneous modalities (like audio and text) by applying learnable gating functions (e.g., sigmoid activations) to the attended features. This dynamically filters and controls what information passes through, resulting in cleaner, context-aware outputs. 🚪 | 2022 | [Flamingo: a Visual Language Model for Few-Shot Learning](https://arxiv.org/abs/2204.14198) |
| [**Distributed Cross-Attention (e.g., LV-XAttn)**](details/distributed-cross-attention.md) | Tailored for extreme sequence lengths, such as high-resolution video inputs in Vision-Language Models (VLMs). It offloads massive KV blocks into distributed network fragments, accelerating inference times without hitting communication bottlenecks. 🌐 | 2025 | [LV-XAttn: Distributed Cross-Attention for Long Visual Inputs in Multimodal Large Language Models](https://arxiv.org/abs/2502.02406) |
| [**Multi-Modal Cross-Attention**](details/multi-modal-cross-attention.md) | A category of variants (like Dual-Cross-Attention) built for single-cell multi-omics or visual question answering. It simultaneously processes reciprocal Queries from multiple modalities to build deeper inter-sequence dependencies. 🧬 | 2025 | [scDiffusion-X](https://www.biorxiv.org/content/10.1101/2025.02.27.640020v1) |

---

## 📊 Architectural Differences

In standard cross-attention, your **Queries (Q)** originate from one source, while **Keys (K)** and **Values (V)** originate from another. The specialized variants improve upon this baseline in two distinct ways:

| Focus Area | Description | Year | Paper Link |
| :--- | :--- | :--- | :--- |
| [**Memory Optimization**](details/memory-optimization.md) | Reducing hardware overhead for long sequences (e.g., CLA, LV-XAttn). 💾 | 2024 | [Reducing Transformer Key-Value Cache Size with Cross-Layer Attention](https://arxiv.org/abs/2405.12981) |
| [**Feature Fusion Quality**](details/feature-fusion-quality.md) | Enhancing how well completely different data types blend together (e.g., GCA). 🤝 | 2022 | [Flamingo: a Visual Language Model for Few-Shot Learning](https://arxiv.org/abs/2204.14198) |

---

## 📖 Recommended Resources

* [Visual Guide to Attention Variants](https://sebastianraschka.com) — A deep dive into the visual and mathematical nuances.
* [GeeksforGeeks: Types of Attention Mechanism](https://geeksforgeeks.org) — Practical implementation details for NLP.

<p align="right">(<a href="#top">back to top</a>)</p>

