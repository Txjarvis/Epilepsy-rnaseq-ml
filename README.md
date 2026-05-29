# Epilepsy RNA-seq Machine Learning Analysis

## Overview

This project explores transcriptomic differences between epilepsy and control brain tissue samples using bulk RNA-seq data from GEO (GSE256068).

The workflow combines exploratory transcriptomics, dimensionality reduction and machine learning to investigate whether gene expression profiles can distinguish epilepsy samples from controls.

---

## Dataset

Source: GEO accession GSE256068

Samples included:

- TLE-HS (Temporal Lobe Epilepsy with Hippocampal Sclerosis)
- FCD2a (Focal Cortical Dysplasia Type IIa)
- FCD2b (Focal Cortical Dysplasia Type IIb)
- TSC (Tuberous Sclerosis Complex)
- Control cortex
- Control hippocampus

---

## Workflow

1. Data preprocessing and metadata extraction
2. Log2 transformation of expression data
3. Variance filtering
4. Principal Component Analysis (PCA)
5. UMAP visualization
6. Logistic Regression classification
7. Random Forest classification
8. Feature importance analysis

---

## Repository Structure

```text
epilepsy-rnaseq-ml/
├── notebooks/
│   ├── 01_preprocess.ipynb
│   ├── 02_PCA_and_UMAP.ipynb
│   └── 03_Machine_learning.ipynb
├── figures/
├── results/
├── data/
└── README.md
```

---

## Key Results

### UMAP Visualization

UMAP revealed clear separation of TLE-HS samples from other epilepsy pathologies, suggesting distinct transcriptional profiles.

### Classification Performance

| Model | Mean 5-Fold ROC-AUC |
|---------|---------|
| Logistic Regression | 0.993 ± 0.013 |
| Random Forest | 0.992 ± 0.013 |

Both models demonstrated strong performance in distinguishing epilepsy from control samples.

### Top Predictive Genes

Feature importance analysis identified genes associated with neuroinflammatory and microglial pathways, including:

- CX3CR1
- P2RY12
- P2RY13
- IL1A
- CCL3
- CH25H

These findings are consistent with known roles of neuroinflammation in epilepsy.

---

## Packages used

- Python
- Pandas
- NumPy
- Scikit-learn
- UMAP-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## Author

Tegan Jarvis

MSc Bioinformatics
