# 🧬 TCGA Lung Squamous Cell Carcinoma (LUSC) RNA-seq Differential Expression Analysis

## Project Description
This repository presents an end-to-end RNA-seq analysis workflow using publicly available data from **The Cancer Genome Atlas (TCGA)** Lung Squamous Cell Carcinoma (LUSC) cohort.

The aim of the project was to compare gene expression profiles between tumor and normal lung tissue samples and identify significantly differentially expressed genes (DEGs). The analysis includes preprocessing, exploratory analysis, dimensionality reduction, statistical testing, and visualization.

This project serves as a practical demonstration of a typical bioinformatics pipeline used in computational biology and biomedical data science.

---

## Objectives
- Process RNA-seq gene expression matrix
- Perform exploratory data analysis
- Evaluate sample clustering using PCA
- Identify differentially expressed genes
- Generate publication-style visualizations
- Demonstrate reproducible research workflow

---

## Dataset
**Source:** The Cancer Genome Atlas (TCGA)  
**Cancer Type:** Lung Squamous Cell Carcinoma (LUSC)

The raw sequencing files (FASTQ/BAM) are not included due to their large size and TCGA data distribution policies.  
This repository contains processed expression data and analysis outputs required to reproduce the results.

---

## Bioinformatics Workflow

### 1. Data Preprocessing
- Loaded gene expression matrix
- Assigned sample labels (tumor vs normal)
- Filtered low-expression genes
- Applied log2 normalization

### 2. Exploratory Data Analysis
Principal Component Analysis (PCA) was performed to:
- assess global transcriptomic structure
- detect outliers
- evaluate separation between tumor and normal samples

### 3. Differential Expression Analysis
Statistical testing was performed to identify genes with significantly different expression levels between tumor and normal tissue.

**Significance criteria**
- Adjusted p-value (FDR) < 0.05
- |log2 Fold Change| > 1

### 4. Visualization
The analysis generated the following plots:
- PCA projection plot
- PCA tumor vs normal separation
- Volcano plot of differential expression

---

## Results

### PCA (Tumor vs Normal Separation)
The PCA shows clustering differences between tumor and normal samples, indicating substantial transcriptomic changes associated with cancer.

![PCA Tumor vs Normal](results/PCA_class_separation_plot.png)

### PCA Projection
Global variance in gene expression captured by principal components.

![PCA Projection](results/PCA_projection_plot.png)

### Differential Expression (Volcano Plot)
The volcano plot highlights significantly upregulated and downregulated genes in tumor samples.

![Volcano Plot](results/volcano_tcga_lusc.png)

The top 100 differentially expressed genes are available in:

results/top100_DEGs_TCGA_LUSC.csv


---

## Repository Structure

tcga-lung-rnaseq-analysis/
│
├── notebooks/
│ └── 01_TCGA_LUSC_analysis.ipynb # full analysis workflow
│
├── results/
│ ├── PCA_class_separation_plot.png
│ ├── PCA_projection_plot.png
│ ├── volcano_tcga_lusc.png
│ └── top100_DEGs_TCGA_LUSC.csv
│
├── .gitignore
└── README.md


---

## Technologies Used
- Python 3
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook

---

## How to Reproduce the Analysis

### 1. Clone the repository
```bash
git clone https://github.com/ag48665/tcga-lung-rnaseq-analysis.git
cd tcga-lung-rnaseq-analysis

2. Install dependencies
pip install pandas numpy matplotlib scikit-learn jupyter

3. Run the notebook
jupyter notebook


Open:

notebooks/01_TCGA_LUSC_analysis.ipynb

Run all cells to reproduce the analysis and plots.

Biological Interpretation

Tumor samples exhibit a distinct gene expression profile compared to normal lung tissue.
The large number of significantly dysregulated genes reflects major alterations in cellular pathways typical for cancer, including proliferation, metabolism, and cell cycle regulation.

Skills Demonstrated

RNA-seq data handling

Data preprocessing and normalization

PCA dimensionality reduction

Statistical hypothesis testing

Multiple testing correction (FDR)

Scientific data visualization

Reproducible research practices

Git & GitHub workflow

Author

Bioinformatics portfolio project created as part of hands-on training in computational biology and RNA-seq data analysis.

License

This project is provided for educational and demonstration purposes using publicly available TCGA data.


---

After you commit it, refresh your repo homepage — you’ll see a **full project page with figures**.  
At that moment, you officially have something you can put in CV:

> *“RNA-seq differential gene expression analysis of TCGA LUSC cohort (Python, PCA, statistical testing, visualization) — GitHub portfolio project.”*

Next we can add a short **CV bullet point** recruiters actually notice (this matters more than the degree).


The top 100 differentially expressed genes are available in:

