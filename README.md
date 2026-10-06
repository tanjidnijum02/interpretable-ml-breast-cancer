# 🧬 Interpretable Machine Learning for Breast Cancer Stage Classification

<p align="center">

### Gene Regulatory Network & Pathway Analysis Using Explainable AI

</p>

<p align="center">

[![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)](https://www.python.org/)
[![Machine Learning](https://img.shields.io/badge/Machine%20Learning-XGBoost-orange)]
[![Explainable AI](https://img.shields.io/badge/Explainable%20AI-SHAP-purple)]
[![Bioinformatics](https://img.shields.io/badge/Bioinformatics-Cancer%20Genomics-green)]
[![Data](https://img.shields.io/badge/Data-TCGA%20%7C%20UCSC%20Xena-red)]

</p>

---

## 📌 Overview

This repository contains the computational framework developed for:

> **Interpretable Machine Learning Framework for Gene Regulatory Network and Pathway Analysis in Breast Cancer**

The study investigates whether gene-expression profiles can be used to classify breast cancer into **early-stage and late-stage groups** using machine learning while maintaining biological interpretability.

The framework integrates:

- Gene-expression preprocessing
- Biologically informed feature selection
- SMOTE-based class balancing
- Machine learning classification
- SHAP-based model interpretation
- Gene correlation analysis
- Gene interaction network construction
- Hub-gene identification
- KEGG pathway enrichment analysis

The objective is to combine **predictive modelling with biological interpretation**, rather than treating machine learning as a black-box classification system.

---

## 👥 Authors

**Sriporna Biswas¹***  
**Tanjidul Huda²**  
**Hema Pal³**  
**Dr. Vinod Kumar Gupta³**

¹ Department of Computer Science & Engineering, Chandigarh University, Punjab, India  
² Department of Biomedical Science, University of Delhi, Delhi, India  
³ Rapture Biotech International (P) Ltd., Noida, Uttar Pradesh, India

\* Corresponding author

---

# 🔬 Research Question

Can interpretable machine learning models classify breast cancer stage from gene-expression profiles while identifying biologically meaningful genes, gene interactions, and cancer-associated pathways?

---

# 🧪 Methodology

The computational workflow consists of the following major stages:

```text
TCGA Gene Expression Data
          │
          ▼
   Data Preprocessing
          │
          ▼
   Feature Selection
          │
          ▼
      SMOTE
 Class Balancing
          │
          ▼
   Feature Scaling
          │
          ▼
      Train/Test Split
          │
          ▼
 ┌────────┼─────────┐
 ▼        ▼         ▼
LR       SVM        RF       XGBoost
 └────────┼─────────┘
          ▼
   Model Evaluation
          │
          ▼
      SHAP Analysis
          │
          ▼
 Gene Correlation Analysis
          │
          ▼
 Gene Interaction Networks
          │
          ▼
   Hub Gene Identification
          │
          ▼
 KEGG Pathway Enrichment


