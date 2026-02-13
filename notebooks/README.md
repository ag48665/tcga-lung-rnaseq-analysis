# TCGA Lung Squamous Cell Carcinoma (LUSC) RNA-seq Analysis

## Project Overview
This project presents a differential gene expression analysis of RNA-seq data from The Cancer Genome Atlas (TCGA) Lung Squamous Cell Carcinoma (LUSC) cohort.  
The objective was to identify genes significantly dysregulated between tumor and normal lung tissue samples and explore global transcriptomic patterns.

This repository demonstrates an end-to-end bioinformatics workflow including preprocessing, exploratory data analysis, dimensionality reduction, and differential expression analysis.

---

## Dataset
Source: The Cancer Genome Atlas (TCGA)

Cancer type: Lung Squamous Cell Carcinoma (LUSC)

The raw sequencing data is not included in this repository due to size and data usage considerations.  
Only processed results and visualizations are provided.

---

## Methods

### 1. Data preprocessing
- Imported RNA-seq expression matrix
- Filtered low-expression genes
- Log2 normalization applied

### 2. Exploratory Data Analysis
Principal Component Analysis (PCA) was performed to evaluate clustering patterns between tumor and normal samples and detect potential batch effects.

### 3. Differential Gene Expression
Differential expression analysis was performed to identify significantly dysregulated genes using statistical testing and multiple testing correction.

Criteria for significance:
- Adjusted p-value (FDR) < 0.05
- |log2 Fold Change| > 1

### 4. Visualization
- gene_expression_matrix
- PCA_class_separation_plot
- PCA_projection_plot
- volcano_tcga_lusc

---

## Results
The analysis identified multiple significantly upregulated and downregulated genes associated with lung squamous cell carcinoma.  
The volcano plot highlights the most statistically significant genes, and the PCA analysis shows clear separation between tumor and normal tissue samples.

Top 100 differentially expressed genes are available in:results/top100_DEGs_TCGA_LUSC.csv


---

## Tools & Technologies
- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook

---

## Biological Interpretation
Tumor samples exhibit a distinct transcriptomic profile compared to normal lung tissue, indicating widespread regulatory changes in gene expression.  
Such changes are consistent with oncogenic transformation and altered cellular pathways in lung squamous cell carcinoma.

---

## Author
Agata Gabara

