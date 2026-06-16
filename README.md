# Awesome-Cross-Attention
## 🚀 Cross-Attention Mechanisms & Key Variants

Cross-attention enables one data sequence (e.g., text) to query information from another separate sequence (e.g., an image or a different language). While the core mechanism relies on scaled dot-product attention, several specialized variants optimize how different data domains interact.

---

## 🛠️ Top Variants of Cross-Attention

* **Cross-Layer Attention (CLA):** Shares the same Keys (K) and Values (V) across multiple sequential decoder layers rather than recalculating them. This drastically reduces the KV cache size, memory footprint, and overall compute requirements in large models.
* **Gated Cross-Attention (GCA):** Fuses heterogeneous modalities (like audio and text) by applying learnable gating functions (e.g., sigmoid activations) to the attended features. This dynamically filters and controls what information passes through, resulting in cleaner, context-aware outputs.
* **Distributed Cross-Attention (e.g., LV-XAttn):** Tailored for extreme sequence lengths, such as high-resolution video inputs in Vision-Language Models (VLMs). It offloads massive KV blocks into distributed network fragments, accelerating inference times without hitting communication bottlenecks.
* **Multi-Modal Cross-Attention:** A category of variants (like Dual-Cross-Attention) built for single-cell multi-omics or visual question answering. It simultaneously processes reciprocal Queries from multiple modalities to build deeper inter-sequence dependencies.

---

## 📊 Architectural Differences

In standard cross-attention, your **Queries (Q)** originate from one source, while **Keys (K)** and **Values (V)** originate from another. The specialized variants improve upon this baseline in two distinct ways:
1. **Memory Optimization:** Reducing hardware overhead for long sequences (e.g., CLA, LV-XAttn).
2. **Feature Fusion Quality:** Enhancing how well completely different data types blend together (e.g., GCA).

---

## 📖 Recommended Resources

* [Visual Guide to Attention Variants](https://sebastianraschka.com) — A deep dive into the visual and mathematical nuances.
* [GeeksforGeeks: Types of Attention Mechanism](https://geeksforgeeks.org) — Practical implementation details for NLP.

<p align="right">(<a href="#top">back to top</a>)</p>

