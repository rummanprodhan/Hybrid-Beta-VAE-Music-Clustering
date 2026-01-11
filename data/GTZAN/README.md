## 📌 Overview
The GTZAN dataset is a standard benchmark for Music Information Retrieval (MIR), consisting of 1,000 audio tracks each 30 seconds long. It is used in this project to validate the **Generalization** capability of the VAE encoder.

## 📥 Download Instructions
**The raw audio files are excluded from this repository.**
Please download the dataset from Kaggle:

* **Download Link:** [Kaggle - GTZAN Dataset](https://www.kaggle.com/datasets/andradaolteanu/gtzan-dataset-music-genre-classification)

### **Setup**
1.  Download the dataset (requires Kaggle account).
2.  Unzip the archive.
3.  Locate the folder named `genres_original` (contains subfolders like `rock`, `jazz`, etc.).
4.  Copy `genres_original` into this directory.

## 📂 Directory Structure
After setup, your folder should look like this:

```text
data/GTZAN/
└── genres_original/   <-- Downloaded separately
    ├── blues/
    ├── classical/
    ├── country/
    ├── ... (10 genres total)
    └── rock/
