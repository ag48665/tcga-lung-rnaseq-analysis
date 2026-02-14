🧬 TCGA Lung Squamous Cell Carcinoma (LUSC) RNA-seq Differential Expression Analysis
Project Overview
This repository presents an end-to-end RNA-seq bioinformatics workflow using publicly available data from The Cancer Genome Atlas (TCGA) Lung Squamous Cell Carcinoma (LUSC) cohort.
The goal of the project is to compare gene expression profiles between tumour and normal lung tissue and identify significantly differentially expressed genes (DEGs).
The analysis demonstrates a typical computational biology pipeline including preprocessing, exploratory data analysis, dimensionality reduction, statistical testing, and visualization.
This project was created as part of my bioinformatics learning portfolio.

Objectives
•	Process RNA-seq gene expression matrix
•	Perform exploratory data analysis (EDA)
•	Evaluate sample clustering using PCA
•	Identify differentially expressed genes (DEGs)
•	Visualize transcriptomic separation
•	Demonstrate a reproducible research workflow

Dataset
Source: The Cancer Genome Atlas (TCGA) https://www.kaggle.com/datasets/noepinefrin/tcga-lusc-lung-cell-squamous-carcinoma-gene-exp

Cancer type: Lung Squamous Cell Carcinoma (LUSC)
The dataset contains normalized RNA-seq expression values:
•	~56,900 genes
•	551 patient samples
Sample types:
•	Tumour tissue
•	Normal lung tissue

Technologies & Libraries
Language
•	Python 3.10 (Anaconda environment)
Libraries
•	pandas
•	numpy
•	matplotlib
•	seaborn
•	scikit-learn
•	scipy
•	jupyter

Repository Structure
tcga-lung-rnaseq-analysis/
│
├── data/
│   └── LUSCexpfile.csv
│
├── notebooks/
│   └── 01_TCGA_LUSC_analysis.ipynb
│
├── results/
│   ├── PCA_class_separation_plot.png
│   ├── PCA_projection_plot.png
│   ├── volcano_tcga_lusc.png
│   └── top100_DEGs_TCGA_LUSC.csv
│
├── .gitignore
└── README.md

Analysis Workflow
1. Data Preprocessing
•	Loaded RNA-seq expression matrix into pandas DataFrame
•	Extracted sample identifiers
•	Assigned sample labels (tumor vs normal)
•	Handled missing values
•	Applied log2 normalization

2. Exploratory Data Analysis (PCA)
Principal Component Analysis (PCA) was performed after standardizing gene expression values to evaluate global transcriptomic differences.
Findings
•	Clear clustering of tumour vs normal samples
•	Indicates strong transcriptomic alteration in cancer tissue

3. Differential Gene Expression Analysis
For each gene, tumour and normal groups were compared using statistical hypothesis testing.
Calculated metrics
•	log2 Fold Change (log2FC)
•	p-value
•	−log10(p-value)

Significance criteria
•	Adjusted p-value (FDR) < 0.05
•	|log2FC| > 1

4. Visualization
The analysis generated:
•	PCA projection plot
•	Tumour vs normal clustering plot
•	Volcano plot of differential expression
•	Ranked DEG gene table

Key Results
Multiple highly significant genes were identified, including:
•	FAM83B
•	AUNIP
•	CASC9
•	TFAP2A
•	E2F7
•	EFNA3

These genes are associated with cancer-related pathways such as:
•	cell proliferation
•	DNA repair
•	cell cycle regulation

The top 100 differentially expressed genes are available in:
results/top100_DEGs_TCGA_LUSC.csv

How to Run
1. Clone the repository
git clone https://github.com/ag48665/tcga-lung-rnaseq-analysis.git
cd tcga-lung-rnaseq-analysis
2. Create environment
conda create -n bioinfo python=3.10
conda activate bioinfo
pip install pandas numpy matplotlib seaborn scikit-learn scipy jupyter
3. Launch Jupyter
jupyter lab
Open:
notebooks/01_TCGA_LUSC_analysis.ipynb
Run all cells to reproduce the analysis.

Biological Interpretation
Tumour samples exhibit a distinct gene expression profile compared to normal lung tissue.
The large number of dysregulated genes reflects major alterations in cancer-related pathways, particularly proliferation, metabolism, and cell-cycle regulation.

Skills Demonstrated
•	RNA-seq data handling
•	Data preprocessing & normalization
•	PCA dimensionality reduction
•	Statistical hypothesis testing
•	Multiple testing correction (FDR)
•	Scientific visualization
•	Reproducible research
•	Git & GitHub workflow
•	Python for bioinformatics

Author
Agata Gabara
Bioinformatics portfolio project demonstrating RNA-seq differential expression analysis using Python.

License
This project uses publicly available TCGA data and is provided for educational and demonstration purposes.


