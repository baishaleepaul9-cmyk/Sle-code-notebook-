# Sle-code-notebook-# SLE Transcriptomic Biomarker Discovery and Diagnostic Prediction

## Overview

This repository contains the code used for the discovery of transcriptomic biomarkers and the development of a machine learning-based diagnostic model for **Systemic Lupus Erythematosus (SLE)** using publicly available gene expression datasets from the Gene Expression Omnibus (GEO).

The workflow includes data preprocessing, feature selection, biomarker identification, machine learning model development, model evaluation, calibration, external validation, and biomarker interpretation.

---

## Objectives

- Identify transcriptomic biomarkers associated with SLE.
- Develop an accurate diagnostic prediction model.
- Evaluate model performance using multiple metrics.
- Validate the model on an independent external dataset.
- Provide an interpretable and reproducible computational workflow.

---

## Datasets

Publicly available datasets were obtained from the NCBI Gene Expression Omnibus (GEO).

### Discovery Dataset
- **GSE65391**

### External Validation Dataset
- **GSE61635**

---

## Workflow

1. Download GEO datasets
2. Data preprocessing and normalization
3. Probe-to-gene annotation
4. Feature selection
5. Biomarker identification
6. Machine learning model training
7. Model evaluation
8. Calibration
9. External validation
10. Visualization and interpretation

---

## Machine Learning Models

The notebook evaluates multiple classification algorithms, including:

- Logistic Regression
- Random Forest
- Support Vector Machine (SVM)
- XGBoost

The best-performing model is selected based on diagnostic performance.

---

## Performance Metrics

Model performance is assessed using:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion Matrix
- Calibration Curve
- Brier Score

---

## Repository Structure

```
.
├── experimental_sle_project.ipynb
├── experimental_sle_project.py
├── requirements.txt
├── README.md
└── figures/
```

---

## Requirements

Python 3.10+

Major libraries:

- pandas
- numpy
- scikit-learn
- xgboost
- matplotlib
- seaborn
- scipy
- GEOparse
- shap

Install dependencies using:

```bash
pip install -r requirements.txt
```

---

## Running the Code

Clone the repository:

```bash
git clone https://github.com/your-username/your-repository.git
```

Open either:

- `experimental_sle_project.ipynb` in Jupyter Notebook or Google Colab

or

Run the Python script:

```bash
python experimental_sle_project.py
```

---

## Data Availability

All datasets used in this study are publicly available through the NCBI Gene Expression Omnibus (GEO).

---

## Citation

If you use this code in your research, please cite the corresponding publication once available.

---

## Author

**Baishalee Paul**

B.Tech Bioinformatics  
Amity University, Noida

---

## License

This project is released under the MIT License.


































