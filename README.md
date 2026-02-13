# TCGA-LUSC RNA-seq Gene Expression Analysis

## Project overview

This project performs an exploratory and differential gene expression analysis of the **TCGA-LUSC (Lung Squamous Cell Carcinoma)** RNA-seq dataset using Python.

The goal of this analysis is to distinguish tumor and normal lung tissue samples based on gene expression profiles and identify significantly differentially expressed genes (DEGs).

The workflow includes:

* loading and preprocessing TCGA expression matrix
* separating tumor and normal samples
* dimensionality reduction using PCA
* statistical testing for differential expression
* identification of highly significant genes
* visualization of transcriptomic separation

This project was created as part of a bioinformatics learning portfolio.

---

## Dataset

**Source:** The Cancer Genome Atlas (TCGA)

**Cancer type:** Lung Squamous Cell Carcinoma (LUSC)

The dataset contains normalized RNA-seq gene expression values:

* ~56,907 genes
* 551 patient samples

Sample types:

* Tumor samples
* Normal tissue samples

---

## Technologies and libraries

Python 3.10 (Anaconda environment)

Main libraries:

* pandas
* numpy
* matplotlib
* seaborn
* scikit-learn
* scipy

---

## Project structure

```
tcga-lung-rnaseq-analysis/
│
├── data/
│   └── LUSCexpfile.csv
│
├── notebooks/
│   └── 01_TCGA_LUSC_analysis.ipynb
│
└── README.md
```

---

## Analysis workflow

### 1. Data preprocessing

The RNA-seq expression matrix was loaded into a pandas DataFrame.
Genes are represented as rows and samples as columns.

Steps performed:

* reading CSV expression matrix
* extracting sample identifiers
* identifying sample type (tumor vs normal)
* handling missing values

---

### 2. Principal Component Analysis (PCA)

To evaluate global transcriptomic differences between tumor and normal tissue, PCA was applied after standardization of gene expression values.

Results:

* clear clustering of tumor vs normal samples
* demonstrates strong transcriptomic alteration in cancer tissue

---

### 3. Differential Gene Expression (DEG) Analysis

For each gene, tumor and normal groups were compared using statistical testing.

Calculated metrics:

* log2 Fold Change (log2FC)
* p-value
* −log10(p-value)

Genes with strong statistical significance were identified as differentially expressed.

---

## Key results

The analysis identified multiple highly significant genes including:

* AL049555.1
* FAM83B
* AUNIP
* CASC9
* TFAP2A
* E2F7
* EFNA3

These genes are associated with cell proliferation, DNA repair, and cancer progression pathways.

---

## Example outputs

The project generates:

* PCA tumor vs normal clustering plot
* ranked DEG gene table
* statistical significance measurements

---

## How to run

1. Clone the repository

```
git clone https://github.com/yourusername/tcga-lung-rnaseq-analysis.git
```

2. Create environment (Anaconda)

```
conda create -n bioinfo python=3.10
conda activate bioinfo
pip install pandas numpy matplotlib seaborn scikit-learn scipy jupyter
```

3. Run Jupyter

```
jupyter lab
```

4. Open:

```
notebooks/01_TCGA_LUSC_analysis.ipynb
```

---

## Purpose

This project demonstrates practical skills in:

* RNA-seq data handling
* cancer transcriptomics
* statistical analysis in bioinformatics
* Python-based data science workflow

---

## Author

Agata Gabara
