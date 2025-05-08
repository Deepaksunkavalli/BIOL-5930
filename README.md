
# METABRIC Breast Cancer Survival Analysis

This project performs an integrative analysis of clinical, gene expression, and mutation data from the METABRIC dataset to predict breast cancer-specific mortality. Using PCA for dimensionality reduction and a combination of machine learning models (logistic regression, random forest, XGBoost), we assess key predictors of patient survival. The project includes a full suite of visualizations and was developed as part of a graduate-level bioinformatics course.

---

## Repository Structure

```
/project_root/
├── README.md                  # Project overview and structure
├── code/
│   ├── preprocessing.R        # Data cleaning and harmonization
│   ├── modeling.R             # Machine learning model training and evaluation
│   └── visualization.R        # All plots and visual summaries
├── data/
│   └── METABRIC_RNA_Mutation.csv  # Raw dataset from Kaggle
├── results/
│   ├── auc_scores.csv         # AUC scores from model evaluations
│   └── confusion_matrices.txt # Confusion matrices for all models
└── plots/
    ├── Figure_1.png to Figure_20.png  # All plots used in the final report
```

---

##  Project Objectives

- Harmonize clinical and omics data from the METABRIC dataset.
- Apply PCA to reduce dimensionality of gene expression data.
- Train and evaluate classification models for cancer-specific mortality.
- Identify the most predictive clinical and molecular features.
- Generate interpretable and publication-ready visualizations.

---

## Dataset

- **Source**: [Kaggle - METABRIC Dataset](https://www.kaggle.com/datasets/raghadalharbi/breast-cancer-gene-expression-profiles-metabric)
- **Size**: 1980 samples
- **Features**: Clinical info, survival outcomes, mutation profiles, gene expression data

---

##  Methodology

- **Preprocessing**:
  - Columns with >30% missing values removed.
  - Median/mode imputation for missing values.
  - SMOTE used to balance survival classes.

- **Feature Engineering**:
  - Mutation binarization (TP53, BRCA1/2, PIK3CA).
  - PCA on scaled gene expression data.

- **Models Used**:
  - Logistic Regression
  - Random Forest (via `ranger`)
  - XGBoost

- **Evaluation Metrics**:
  - Confusion Matrix
  - ROC AUC
  - Accuracy, Sensitivity, Specificity

---

## Visualizations

- Bar plots of death outcome by therapy type
- Boxplots for PC1, tumor size, and age
- Violin plots of gene expression
- Mutation frequency barplots
- PCA biplots
- Volcano plot of DE genes
- Heatmap of top 20 DEGs
- UpSet plot of gene mutation overlaps

All visualizations are saved in `/plots/` and referenced in the written report.

---

##  Key Findings

- PCA scores (PC1, PC2), tumor size, and TP53 mutation were strong predictors.
- Random Forest and XGBoost significantly outperformed logistic regression.
- TP53, BRCA1/2, and PIK3CA are consistently altered in deceased patients.

---

##  Final Report

A full journal-style report (`METABRIC_Final_Report_Deepak.docx`) is available upon request or in the course submission. It includes:

- Abstract, Introduction, Methods, Results, and Discussion
- Detailed figure legends and referenced visualizations
- Interpretations aligned with current breast cancer literature

---

##  Author

**Deepak Sunkavalli**  
Master's Student, Bioinformatics & Computational Biology  
Saint Louis University, May 2025

---

## Contact

For questions, please reach out via [GitHub Issues](https://github.com/Deepaksunkavalli/BIOL-5930/issues) 

---

## License

This project is for educational use only. Dataset courtesy of METABRIC Consortium via Kaggle.
