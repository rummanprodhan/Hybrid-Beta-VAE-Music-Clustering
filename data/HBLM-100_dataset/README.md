# HBLM-100 Dataset (Hybrid Bangla Language Music)

## 📌 Overview
This is a custom-curated dataset created for the **Hybrid Beta-VAE Music Clustering** project. It consists of 100 audio tracks balanced between Bangla and English languages, designed to test cross-cultural disentanglement.

## 📥 Download Instructions
**The raw audio files are too large for GitHub (883 MB).**
Please download the dataset from the link below and extract it into this folder:

* **Download Link:** [Google Drive - HBLM Dataset](https://drive.google.com/file/d/1YWjhcl6BYRUfViDYS_EltGRrTz6AxdyS/view?usp=sharing)

### **Setup**
1.  Download the zip file.
2.  Extract the contents so that the `audio` folder is inside `data/HBLM-100/`.
3.  Ensure the structure matches the "Directory Structure" below.

## 📂 Directory Structure
```text
data/HBLM-100/
├── metadata.csv       <-- Included in Repo (Labels & Lyrics)
├── README.md          <-- This file
└── audio/             <-- Downloaded separately
    ├── bangla/        <-- Contains 50 Bangla tracks
    └── english/       <-- Contains 50 English tracks