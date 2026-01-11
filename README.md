# Hybrid-Beta-VAE-Music-Clustering



<<<<<<< HEAD
\# Disentangled Multi-Modal Music Clustering using Hybrid Beta-VAE



\[!\[Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1WMch9Rr9Okq06HAz6Lit-hyAlC35vQ5O?usp=sharing)

\[!\[Open In Kaggle](https://kaggle.com/static/images/open-in-kaggle.svg)](https://www.kaggle.com/code/rummanahmedprodhan/2-gtzan-benchmark-clustering)

\[!\[Project Report](https://img.shields.io/badge/PDF-Read%20Report-red)](https://drive.google.com/file/d/1xP4n4tslrkjtkb3aqOaloO0rq93gpKdO/view?usp=sharing)

\[!\[License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)



\## 📌 Project Overview

This repository contains the implementation of a \*\*Hybrid Beta-Variational Autoencoder (Beta-VAE)\*\* for unsupervised music clustering. The project addresses the challenge of cross-cultural music analysis by fusing \*\*Convolutional Spectral Features (Audio)\*\* with \*\*Semantic Lyric Embeddings (Text)\*\*.



By imposing a heavy KL-divergence penalty ($\\beta=4.0$), the model successfully disentangles "Language" (from lyrics) and "Genre" (from audio) into orthogonal axes in the latent space.



\* \*\*Course:\*\* Neural Networks

\* \*\*Track:\*\* Hard Task (Conditional/Beta-VAE \& Multi-modal Clustering)

\* \*\*Author:\*\* Rumman Ahmed Prodhan



\## 🚀 Key Features

\* \*\*Multi-Modal Fusion:\*\* Integrates Log-Mel Spectrograms (via CNN) and Sentence-BERT embeddings.

\* \*\*Beta-VAE Architecture:\*\* Uses $\\beta=4.0$ to enforce statistical independence in the latent space.

\* \*\*Custom Dataset (HBLM-100):\*\* A curated dataset of 100 Bangla and English tracks for cross-cultural evaluation.

\* \*\*State-of-the-Art Metrics:\*\* Achieved \*\*ARI=1.0\*\* and \*\*NMI=1.0\*\* on language separation tasks.

\* \*\*Benchmarked:\*\* Validated audio encoders against the standard GTZAN genre dataset.



\## 📂 Repository Structure



```text

Hybrid-Beta-VAE-Music-Clustering/

│

├── data/                      # Dataset documentation

│   ├── HBLM-100/              # Custom Dataset (Metadata included, Audio linked)

│   └── GTZAN/                 # Benchmark Dataset (Readme included)

│

├── notebooks/                 # Experiment Notebooks

│   ├── 1\_Hybrid\_Beta\_VAE\_HBLM.ipynb      # Main Experiment (Bangla vs English)

│   └── 2\_GTZAN\_Benchmark\_Clustering.ipynb # Generalization Benchmark

│

├── results/                   # Generated Plots \& Visualizations

├── requirements.txt           # Dependencies

├── Disentangling\_Language\_and\_Genre\_\_Unsupervised\_Cross\_Cultural\_Music\_Clustering\_via\_Hybrid\_Beta\_VAE.pdf  # Final Scientific Report

└── README.md                  # This file



💻 Run the ExperimentsThe project is divided into two major experiments. You can run them directly in the cloud using the links below.1. Main Experiment: Cross-Cultural Clustering (HBLM-100)Disentangling language from genre using the Fusion Encoder on the custom dataset.2. Benchmark Experiment: Genre Classification (GTZAN)Validating the audio encoder on standard genre classification tasks using Kaggle GPUs.📊 Results SummaryDatasetMethodARINMISilhouettePurityCH IndexHBLM-100Hybrid Beta-VAE1.001.000.211.00238.6HBLM-100Baseline PCA0.000.000.240.51303.8GTZANConv-VAE0.190.320.080.4145.6GTZANBaseline PCA0.040.06-0.020.1828.5Note: While PCA achieves higher Silhouette scores on HBLM due to dense acoustic clustering, it fails to capture the semantic (language) structure, resulting in ARI ≈ 0.📥 Dataset SetupDue to GitHub storage limits, raw audio files are not included. If running locally, please download them:HBLM-100 (Custom): Download from Google Drive and extract to data/HBLM-100/audio/.GTZAN (Benchmark): Download from Kaggle and extract to data/GTZAN/.🛠️ Installation (Local)To run the code on your own machine:Bashgit clone \[https://github.com/rummanprodhan/Hybrid-Beta-VAE-Music-Clustering.git](https://github.com/rummanprodhan/Hybrid-Beta-VAE-Music-Clustering.git)

cd Hybrid-Beta-VAE-Music-Clustering

pip install -r requirements.txt

📜 ReferencesHiggins, I., et al. (2017). beta-VAE: Learning Basic Visual Concepts with a Constrained Variational Framework. ICLR.Reimers, N., \& Gurevych, I. (2019). Sentence-BERT: Sentence Embeddings using Siamese BERT-Networks. EMNLP.Tzanetakis, G., \& Cook, P. (2002). Musical genre classification of audio signals. IEEE Transactions on Speech and Audio Processing.License: MIT

=======
>>>>>>> 642e804f7d577b4dc32b116f1ae575a599e7899b
