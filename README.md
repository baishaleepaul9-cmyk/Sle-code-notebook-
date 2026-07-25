# SLE Transcriptomic Biomarker Discovery, Diagnostic Prediction, and Disease Severity Prediction

## Overview

This repository contains the complete computational workflow for identifying transcriptomic biomarkers, developing a diagnostic machine learning model for Systemic Lupus Erythematosus (SLE), and predicting disease severity using publicly available gene expression datasets from the NCBI Gene Expression Omnibus (GEO).

The pipeline includes:

- Gene expression data acquisition
- Data preprocessing and normalization
- Probe-to-gene annotation
- Feature selection
- Biomarker discovery
- Diagnostic model development
- Disease severity prediction
- Model evaluation
- Probability calibration
- External validation
- Visualization and interpretation

---

## Datasets

### Diagnostic Prediction

| Dataset | Purpose |
|---------|---------|
| **GSE65391** | Discovery and model training |
| **GSE61635** | Independent external validation |

### Disease Severity Prediction

| Dataset | Purpose |
|---------|---------|
| **GSE88884** | Prediction of disease severity using SLEDAI scores |

All datasets were downloaded directly from the NCBI Gene Expression Omnibus (GEO).

---

## Repository Contents

This repository consists of two independent machine learning workflows.

### 1. Diagnostic Prediction

The diagnostic pipeline develops a transcriptomic classifier capable of distinguishing SLE patients from healthy controls.

Major steps include:

- Downloading GEO datasets
- Probe annotation (GPL10558)
- Data preprocessing
- Gene-level expression matrix generation
- Feature selection
- Biomarker identification
- Model training
- Performance evaluation
- Calibration
- External validation using GSE61635

---

### 2. Disease Severity Prediction

The severity pipeline predicts disease severity using transcriptomic profiles and clinical SLEDAI scores.

Major steps include:

- Loading GSE88884
- Data preprocessing
- Spearman correlation-based gene selection
- Severity-associated biomarker discovery
- Machine learning model development
- Model evaluation
- Visualization of severity-associated genes

---

## Workflow

```
GEO Download
      │
      ▼
Data Preprocessing
      │
      ▼
Probe Annotation
      │
      ▼
Gene Expression Matrix
      │
      ▼
Feature Selection
      │
      ├──────────────┐
      ▼              ▼
Diagnostic Model   Severity Model
      │              │
      ▼              ▼
Evaluation      Severity Prediction
      │
      ▼
Calibration
      │
      ▼
External Validation
```

---

## Machine Learning Models

The notebook evaluates multiple supervised learning algorithms, including:

- Logistic Regression
- Random Forest
- Support Vector Machine (SVM)
- XGBoost

The best-performing models are selected based on evaluation metrics.

---

## Evaluation Metrics

Model performance is assessed using:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion Matrix
- Calibration Curve
- Brier Score

For severity prediction, correlation-based feature selection and predictive performance are also evaluated.

---

## Repository Structure

```
.
├── experimental_sle_project.ipynb
├── experimental_sle_project.py
├── README.md
├── requirements.txt
├── LICENSE
└── figures/
```

---

## Requirements

Python 3.10 or later

Required packages include:

- numpy
- pandas
- scipy
- scikit-learn
- xgboost
- matplotlib
- seaborn
- GEOparse
- shap
- joblib

Install dependencies using:

```bash
pip install -r requirements.txt
```

---

## Running the Project

Clone the repository:

```bash
git clone https://github.com/<username>/<repository>.git
```

Run the notebook using:

```text
experimental_sle_project.ipynb
```

or execute the Python script:

```bash
python experimental_sle_project.py
```

---

## Data Availability

The datasets used in this study are publicly available through the NCBI Gene Expression Omnibus (GEO):

- GSE65391
- GSE61635
- GSE88884

---

## Reproducibility

The repository contains all code required to reproduce the analyses presented in the accompanying manuscript. Users only need to download the GEO datasets (performed automatically within the notebook or script) and install the required Python dependencies.

---

## Author

**Baishalee Paul**

Department of Bioinformatics  
Amity University, Noida, India

---

## License

This project is distributed under the MIT License.
