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

```
---

## 📊 Dataset & Experimental Setup

The study used breast cancer gene-expression data obtained through the **UCSC Xena platform** from **TCGA**.

### Dataset characteristics

| Category | Samples |
|---|---:|
| Original dataset | 1,219 |
| Early-stage | 900 |
| Late-stage | 300 |
| After SMOTE | 1,652 |
| Balanced early-stage | 826 |
| Balanced late-stage | 826 |

A set of **70 biologically relevant genes** associated with cancer-related pathways was selected for the analysis.

SMOTE (Synthetic Minority Oversampling Technique) was applied to address class imbalance before model training.

---

## 🤖 Model Performance

Four machine learning models were evaluated:

- Logistic Regression
- Support Vector Machine (SVM)
- Random Forest
- XGBoost

### Performance Comparison

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| **XGBoost** | 0.832 | 0.832 | 1.000 | 0.908 | **0.626** |
| Logistic Regression | 0.832 | 0.835 | 0.995 | 0.908 | 0.616 |
| SVM | 0.832 | 0.832 | 1.000 | 0.908 | 0.562 |
| Random Forest | 0.832 | 0.832 | 1.000 | 0.908 | 0.543 |

### 🏆 Best Performing Model

XGBoost achieved the highest ROC-AUC (**0.626**) among the evaluated models and was therefore selected for subsequent interpretability analysis.

---

## 📈 ROC Analysis

Receiver Operating Characteristic (ROC) analysis was used to compare the
discriminative performance of the four classification models.

The reported ROC-AUC values were:

- **XGBoost:** 0.626
- **Logistic Regression:** 0.616
- **SVM:** 0.562
- **Random Forest:** 0.543

XGBoost achieved the highest ROC-AUC, indicating the strongest
discriminative performance among the evaluated models in this study.

---

## 🧠 Explainable AI — SHAP Analysis

To improve model interpretability, **SHAP (SHapley Additive exPlanations)**
was applied to the XGBoost model.

The analysis identified several genes contributing strongly to model
predictions, including:

- **RUNX1**
- **ERBB2**
- **NCOR2**
- **FOS**
- NANOG
- SOX2
- VEGFA
- KRAS
- AR

SHAP provides a quantitative interpretation of how individual gene-expression
features influence model predictions, helping transform the classification
framework from a black-box model into an interpretable machine learning system.

---

## 🧬 Gene Expression Heatmap

A gene-expression heatmap was generated to visualize expression patterns
across the breast cancer samples.

The analysis showed differences in expression patterns between early-stage
and late-stage samples, suggesting stage-specific molecular signatures.

The heatmap also provides a visual representation of expression heterogeneity
and groups of genes showing similar expression patterns.

---

## 🕸️ Gene Interaction Network Analysis

Gene interaction networks were constructed using correlation-based thresholds.

Two thresholds were investigated:

- **0.7** — stronger gene interactions
- **0.5** — more densely connected interactions

Genes were represented as nodes, while correlation-based relationships
were represented as edges.

The resulting networks were used to investigate the structure of gene
relationships and identify highly connected genes.

---

## 🎯 Hub Gene Identification

Degree centrality was used to identify highly connected genes within the
gene interaction network.

The analysis identified several prominent hub genes, including:

- **ATM**
- **PIK3CA**
- **CDK6**
- **NCOR1**

These genes showed high connectivity within the constructed interaction
network and were highlighted as candidates for further biological investigation.

---

## 🧪 KEGG Pathway Enrichment

KEGG pathway enrichment analysis was performed to investigate the biological
relevance of the selected genes.

The analysis identified enrichment across several cancer-associated and
regulatory pathways, including:

- **MicroRNAs in Cancer**
- **Breast Cancer**
- **Pathways in Cancer**
- **FOXO Signaling**
- **Thyroid Hormone Signaling**

The enrichment analysis provided an additional biological validation layer
for the genes identified through the machine learning and network analyses.

---

## 🔎 Key Findings

- Four machine learning models achieved approximately **83.2% accuracy**.
- **XGBoost** achieved the highest reported ROC-AUC (**0.626**).
- SHAP analysis highlighted genes including **RUNX1, ERBB2, NCOR2 and FOS** as important contributors to model predictions.
- Gene-expression analysis revealed distinct expression patterns across early- and late-stage samples.
- Correlation-based network analysis identified highly connected genes including **ATM, PIK3CA, CDK6 and NCOR1**.
- KEGG enrichment indicated associations with multiple cancer-related and regulatory pathways.
- Integrating machine learning with SHAP, network analysis and pathway enrichment provided a more biologically interpretable framework for breast cancer stage classification.

---

## ⚠️ Limitations

The current framework is based on computational analysis of gene-expression
data and requires further validation before any clinical application.

The study also highlights the need for independent external validation and
broader molecular data integration.

---

## 🔭 Future Directions

Future development of the framework may include:

- Multi-omics integration
- Proteomics
- Metabolomics
- Epigenomics
- Graph Neural Networks (GNNs)
- Deep learning approaches
- Independent external validation
- Expanded pathway analysis
- Drug-target interaction analysis
- Personalized medicine applications
- Clinical decision-support integration




