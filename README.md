# Disentangled Multi-Modal Music Clustering using Hybrid Beta-VAE

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1WMch9Rr9Okq06HAz6Lit-hyAlC35vQ5O?usp=sharing)
[![Open In Kaggle](https://kaggle.com/static/images/open-in-kaggle.svg)](https://www.kaggle.com/code/rummanahmedprodhan/2-gtzan-benchmark-clustering)
[![Project Report](https://img.shields.io/badge/PDF-Read%20Report-red)](https://drive.google.com/file/d/1xP4n4tslrkjtkb3aqOaloO0rq93gpKdO/view?usp=sharing)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 📌 Project Overview
This repository contains the implementation of a **Hybrid Beta-Variational Autoencoder (Beta-VAE)** for unsupervised music clustering. The project addresses the challenge of cross-cultural music analysis by fusing **Convolutional Spectral Features (Audio)** with **Semantic Lyric Embeddings (Text)**.

By imposing a heavy KL-divergence penalty ($\beta=4.0$), the model successfully disentangles "Language" (from lyrics) and "Genre" (from audio) into orthogonal axes in the latent space.

* **Course:** Neural Networks
* **Track:** Hard Task (Conditional/Beta-VAE & Multi-modal Clustering)
* **Author:** Rumman Ahmed Prodhan

## 🚀 Key Features
* **Multi-Modal Fusion:** Integrates Log-Mel Spectrograms (via CNN) and Sentence-BERT embeddings.
* **Beta-VAE Architecture:** Uses $\beta=4.0$ to enforce statistical independence in the latent space.
* **Custom Dataset (HBLM-100):** A curated dataset of 100 Bangla and English tracks for cross-cultural evaluation.
* **State-of-the-Art Metrics:** Achieved **ARI=1.0** and **NMI=1.0** on language separation tasks.
* **Benchmarked:** Validated audio encoders against the standard GTZAN genre dataset.

## 📂 Repository Structure

```text
Hybrid-Beta-VAE-Music-Clustering/
│
├── data/                      # Dataset documentation
│   ├── HBLM-100/              # Custom Dataset (Metadata included, Audio linked)
│   └── GTZAN/                 # Benchmark Dataset (Readme included)
│
├── notebooks/                 # Experiment Notebooks
│   ├── 1_Hybrid_Beta_VAE_HBLM.ipynb      # Main Experiment (Bangla vs English)
│   └── 2_GTZAN_Benchmark_Clustering.ipynb # Generalization Benchmark
│
├── src/                       # Modular Implementation
│   ├── vae.py                 # HybridBetaVAE Class Definition
│   ├── dataset.py             # Audio/Text Preprocessing logic
│   ├── clustering.py          # K-Means & Visualization utilities
│   └── evaluation.py          # Metrics (ARI, NMI, Silhouette)
│
├── results/                   # Generated Plots & Visualizations
├── requirements.txt           # Dependencies
├── Neural_Network_Report.pdf  # Final Scientific Report
└── README.md                  # This file
