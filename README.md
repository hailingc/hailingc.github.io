# Isotonic Layer: Universal Recommendation Debiasing

[![Paper](https://img.shields.io/badge/Paper-PDF-red)](./debias.pdf)
[![Live Demo](https://img.shields.io/badge/Live-Blog_Post-blue)](https://yourusername.github.io/your-repo-name/)

[cite_start]This repository contains the implementation and conceptual overview of the **Isotonic Layer**, a differentiable framework designed to enforce global monotonicity within deep learning architectures for large-scale recommendation systems[cite: 751, 752, 761].

## 🔗 Project Page
Detailed explanations, mathematical formulations, and interactive summaries can be found here:
### [**View the Isotonic Layer Research Blog**](index.html)

---

## 🚀 Key Features
* [cite_start]**Differentiable Isotonic Calibration:** Integrates piecewise linear fitting directly into neural architectures, allowing for end-to-end gradient-based optimization[cite: 761, 829].
* [cite_start]**Global Monotonicity:** Enforces strict order properties using a non-negativity constraint (ReLU) on bucket weights, ensuring logically consistent outputs[cite: 763, 820].
* [cite_start]**Context-Aware Debiasing:** Uses learnable embeddings to capture nuanced distortions from display positions, device types, and advertiser IDs[cite: 765, 769].
* [cite_start]**Multi-Task Scalability:** Specifically designed for Multi-Task Learning (MTL) environments to handle heterogeneous bias profiles across different user behaviors[cite: 784, 833].

## 📊 Performance Summary
The Isotonic Layer has been validated through extensive production A/B tests at LinkedIn, showing:
* [cite_start]**+0.63%** lift in Weekly Active Users[cite: 656].
* [cite_start]**+1.5% to +1.9%** gains in Evaluation AUC for downstream tasks[cite: 637].
* [cite_start]Significant reduction in prediction variance and improved calibration fidelity[cite: 785, 642].

## 🛠 Implementation Detail
[cite_start]The layer discretizes the input space into fixed-width buckets (default range `[-17, 8]`) and computes a dot-product between non-negative weights and a transformed activation vector[cite: 831, 882]. [cite_start]This ensures high-throughput efficiency for production systems[cite: 832].
