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

## 💻 Run the Experiments
The project is divided into two major experiments. You can run them directly in the cloud using the links below.

### **1. Main Experiment: Cross-Cultural Clustering (HBLM-100)**
Disentangling language from genre using the Fusion Encoder on the custom dataset.
<br>
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1WMch9Rr9Okq06HAz6Lit-hyAlC35vQ5O?usp=sharing)

### **2. Benchmark Experiment: Genre Classification (GTZAN)**
Validating the audio encoder on standard genre classification tasks using Kaggle GPUs.
<br>
[![Open In Kaggle](https://kaggle.com/static/images/open-in-kaggle.svg)](https://www.kaggle.com/code/rummanahmedprodhan/2-gtzan-benchmark-clustering)

<br>

## 📊 Results Summary

| Dataset | Method | ARI | NMI | Silhouette | Purity | CH Index |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **HBLM-100** | **Hybrid Beta-VAE** | **1.00** | **1.00** | **0.21** | **1.00** | **238.6** |
| HBLM-100 | Baseline PCA | 0.00 | 0.00 | 0.24 | 0.51 | 303.8 |
| **GTZAN** | **Conv-VAE** | **0.19** | **0.32** | **0.08** | **0.41** | **45.6** |
| GTZAN | Baseline PCA | 0.04 | 0.06 | -0.02 | 0.18 | 28.5 |

> **Note:** While PCA achieves higher Silhouette scores on HBLM due to dense acoustic clustering, it fails to capture the semantic (language) structure, resulting in ARI ≈ 0.

<br>

## 📥 Dataset Setup
Due to GitHub storage limits, raw audio files are not included. If running locally, please download them:

1.  **HBLM-100 (Custom):** [Download from Google Drive](https://drive.google.com/file/d/1YWjhcl6BYRUfViDYS_EltGRrTz6AxdyS/view?usp=sharing) and extract to `data/HBLM-100/audio/`.
2.  **GTZAN (Benchmark):** [Download from Kaggle](https://www.kaggle.com/datasets/andradaolteanu/gtzan-dataset-music-genre-classification) and extract to `data/GTZAN/`.

<br>

## 🛠️ Installation (Local)
To run the code on your own machine:

```bash
git clone [https://github.com/rummanprodhan/Hybrid-Beta-VAE-Music-Clustering.git](https://github.com/rummanprodhan/Hybrid-Beta-VAE-Music-Clustering.git)
cd Hybrid-Beta-VAE-Music-Clustering
pip install -r requirements.txt


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
├── results/                   # Generated Plots & Visualizations
├── requirements.txt           # Dependencies
├── Disentangling_Language_and_Genre__Unsupervised_Cross_Cultural_Music_Clustering_via_Hybrid_Beta_VAE.pdf  # Final Scientific Report
└── README.md                  # This file
