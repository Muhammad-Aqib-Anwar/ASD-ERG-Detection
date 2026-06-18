# Machine Learning Model for the Detection of Autism Spectrum Disorder Using Electroretinogram Signals

## 📌 Overview

This repository contains the complete implementation code for the paper:

> **"Machine Learning Model for the Detection of Autism Spectrum
Disorder Using Electroretinogram Signals"**

The project presents an application-driven integration framework that combines **UMAP dimensionality reduction**, **SMOTE-based oversampling**, and **machine/deep learning classifiers** to detect Autism Spectrum Disorder (ASD) using electroretinogram (ERG) signals. The framework is evaluated across multiple flash strengths at both sample-level and subject-level, with subject-level experiments serving as the primary evaluation to prevent data leakage.

---

## 🧠 Key Features

- **Application-driven integration** of UMAP, SMOTE, and ML/DL classifiers
- **Subject-level cross-validation** to prevent data leakage
- **Multi-flash-strength analysis** (−0.367 to 1.204 cd·s·m⁻²)
- **Comprehensive model comparison**:
  - Machine Learning: SVM, Random Forest, MLP, XGBoost
  - Deep Learning: LSTM-FCN, Transformer
- **Explainability analysis** using SHAP for feature interpretation
- **Statistical comparison** with Bonferroni correction

---

## 📂 Repository Structure
UMAP-ERG/
├── Daataset/
│ ├── raw/ # Raw ERG signal data (access restricted)
│ └── processed/ # Preprocessed ERG signals
├── notebooks/
│ ├── 01_asd Vs control.ipynb
│ ├── 02_asd Vs control final.ipynb
│ └── 03_All flash ERG baseline.ipynb
│ └── 04_Correlation_Eye_Analysis.ipynb
│ └── 05_without_Smote_baseline_All_records.ipynb
│ └── 06_ERG_plots_Experiments.ipynb
├── models/
│ ├── blstm_model.pth
│ ├── blstm_weights.pth
│ ├── transformer_model.pth 
├── Results/
│ ├── ASD Experiments Final.xlsx/ # All results used in the manuscript
│ ├── Experiments_ASD.xlsx/ # Initial Results
├── images/
│ └── correlation_values_eyewise.png 
├── requirements.txt # Python dependencies
├── environment.yml # Conda environment file
├── LICENSE
└── README.md
