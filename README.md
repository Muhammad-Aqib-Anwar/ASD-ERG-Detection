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
- **Statistical comparison** with Bonferroni correction

---

## 📂 Repository Structure
``` bash
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
``` 
## 📈 Results Summary

The best performance was achieved by **SVM at the subject level** using lower flash strength data (**0.114 cd·s·m⁻²**). The model outperformed state-of-the-art results reported in the literature by **15%**.

### Performance Metrics (Mean ± SD)

| Metric | Value | 95% Confidence Interval |
|--------|-------|-------------------------|
| **Accuracy** | 96% ± 0.06 | 90.5% – 97.9% |
| **AUC** | 98% ± 0.02 | 96.3% – 100% |
| **Sensitivity** | 93.33% ± 0.06 | 89.6% – 97.0% |
| **Specificity** | 98.33% ± 0.05 | 95.2% – 100% |

### Model Comparison

Statistical comparison using **Bonferroni correction** (adjusted α = 0.008) confirmed that SVM significantly outperformed all other classifiers (*p* < 0.001 for all comparisons).

| Classifier | Accuracy (%) | AUC (%) |
|------------|--------------|---------|
| **SVM** | **96.0 ± 0.06** | **98.0 ± 0.02** |
| LSTM-FCN | 85.0 ± 0.08 | 87.0 ± 0.05 |
| Transformer | 83.0 ± 0.09 | 85.0 ± 0.06 |
| Random Forest | 88.0 ± 0.07 | 90.0 ± 0.04 |
| XGBoost | 87.0 ± 0.06 | 89.0 ± 0.05 |

### Clinical Interpretability

Building on the findings of Kulyabin et al. [1], our results further demonstrate that **reduced b-wave amplitude** and **absent oscillatory potentials** at lower flash strengths suggest that low-intensity ERG protocols may serve as a sensitive, non-invasive biomarker for detecting retinal signaling deficits associated with ASD.

---

## 📊 Key Findings

- ✅ Subject-level experiments provide the most reliable evaluation (no data leakage)
- ✅ Lower flash strengths (0.114 cd·s·m⁻²) yield the best classification performance
- ✅ SVM with UMAP-transformed features significantly outperforms deep learning architectures (LSTM, Transformer)
- ✅ Statistical significance confirmed with Bonferroni correction
- ✅ Reduced b-wave amplitude and absent oscillatory potentials in ASD suggest retinal signaling deficits

## 📊 Dataset Description

We utilized a publicly available ERG dataset contributed by Flinders University, Australia [1, 36, 38], accessible at: [https://open.flinders.edu.au/](https://open.flinders.edu.au/).

### Participants

- **Total:** N = 106 participants
- **ASD:** 46 participants
- **Control:** 60 participants
- **Exclusion criteria:** Family history of ASD, psychiatric illness, retinal or chromosomal disorders, diabetes, co-occurring neurodevelopmental conditions, or brain injury.

### ERG Recording Protocol

- **Flash strengths:** Nine levels ranging from **−0.367** to **1.204 cd·s·m⁻²**
- **Flash categories:**
  - **Low:** (−0.367, 0.114) cd·s·m⁻²
  - **Medium:** (0.398, 0.799) cd·s·m⁻²
  - **High:** (0.949, 1.204) cd·s·m⁻²
- **Repeats:** Each flash repeated 2–3 times to validate retinal responses
- **Eyes:** Recorded from both eyes of each participant
- **Feature extraction:** Average signal per flash strength computed, resulting in **235 features** per instance (representing a-wave and b-wave amplitudes)
### 📚 Dataset Reference

Constable, P., Marmolejo-Ramos, F., Thompson, D., & Brabec, M. (2022). *Electroretinogram raw waveforms for control and autism* [Dataset]. Flinders University. [https://doi.org/10.25451/flinders.21546210.v1](https://doi.org/10.25451/flinders.21546210.v1)
## 📧 Contact

For questions regarding the code, data access, collaboration, or any other inquiries, please feel free to reach out:

- **Corresponding Author:** [Muhammad Aqib Anwar]
- **Email:** [muan88621@hbku.edu.qa]
- **Institution:** [HBKU, Qatar]
- **GitHub:** [https://github.com/Muhammad-Aqib-Anwar](https://github.com/yourusername)
- **Google Scholar:** [https://scholar.google.com/citations?user=xO9pQQYAAAAJ&hl=en]

For dataset access requests, please contact the dataset curators directly at: [paul.constable@flinders.edu.au](mailto:paul.constable@flinders.edu.au)

---

### 📬 Quick Contact

| Purpose | Contact |
|---------|---------|
| Code/Implementation Issues | [muan88621@hbku.edu.qa](mailto:muan88621@hbku.edu.qa) |
| Data Access Requests | [paul.constable@flinders.edu.au](mailto:paul.constable@flinders.edu.au) |
| Collaboration/General Inquiries | [muan88621@hbku.edu.qa](mailto:muan88621@hbku.edu.qa) |

---

**We welcome feedback, questions, and collaboration opportunities!**
