# UMAP-ERG: An Application-Driven Integration Framework for ASD Detection Using Electroretinogram Signals

## 📌 Overview

This repository contains the complete implementation code for the paper:

> **"UMAP-ERG: An Application-Driven Integration Framework for ASD Detection Using Electroretinogram Signals"**

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
