# 🧬 Comparative Gene Expression Analysis of Breast Tumor and Normal Samples (GSE25066 Dataset)

---

## 📊 Project Overview  

This project analyzes gene expression data from breast tumor and normal tissue samples to identify differential gene activity associated with breast cancer.

The analysis combines **statistical testing**, **correlation analysis**, **dimensionality reduction**, and **visualization techniques** to explore gene-level expression patterns between both conditions.

---

## 🎯 Objectives  

- Compare gene expression profiles between tumor and normal samples  
- Identify significantly differentially expressed genes  
- Perform statistical testing to evaluate gene-level differences
- Visualize expression patterns and sample relationships

---

## 📁 Dataset Overview  

- **Dataset:** GSE25066 Breast Cancer Gene Expression Dataset  
- **Source:** Mendeley Data / Public gene expression repository  
- **Reference:** [Mendeley Data – Gene Expression Profiles of Breast Cancer](https://data.mendeley.com/datasets/v3cc2p38hb/1)  

---

## 📊 Dataset Structure  

This dataset consists of gene expression measurements from breast tumor and normal tissue samples.

- Each **row** represents a gene (Hybridization REF)
- Each **column** represents a patient sample (tumor or normal)  
- Each **cell value** represents the expression level of a gene in a specific sample  

After preprocessing, the tumor and normal datasets were merged into a single expression matrix for comparative analysis:

```python
df = pd.concat([tumor, normal], axis=1)
```

---

## 🛠️ Tools & Technologies

- Python (Pandas, NumPy)  
- SciPy (Statistical Analysis)  
- Scikit-learn (Principal Component Analysis)  
- Matplotlib & Seaborn (Data Visualization)  
- Jupyter Notebook

---

## 🔬 Project Workflow

1. **Data Collection, Overview & Transformation**

* Loaded tumor and normal gene expression datasets
* Checked dataset structure, missing values, and duplicates
* Renamed sample columns for consistency
* Merged datasets into a single dataframe

2. **Statistical Analysis**

* Computed Pearson correlation between tumor and normal expression profiles
* Performed Welch’s t-test to identify differential gene expression
* Applied Benjamini–Hochberg False Discovery Rate (FDR) correction
* Calculated log2 fold change for gene expression comparison

3. **Visualization**

* Bar Plot (Top Differentially Expressed Genes)
* Expression Heatmap
* Correlation Heatmap
* Volcano Plot
* Principal Component Analysis (PCA)

---

## 📈 Statistical Insights

### 🔗 Pearson Correlation Analysis

* Pearson correlation analysis showed a very strong similarity (~0.99) between average tumor and normal gene expression profiles
* This indicates that many genes maintain similar expression patterns across both conditions

### 🧪 Differential Expression Analysis

* Welch’s t-test was used to compare gene expression between tumor and normal samples
* Benjamini–Hochberg FDR correction was applied to reduce false-positive results from multiple testing

#### Key Findings

* Several genes showed statistically significant expression differences after FDR correction
* Some genes showed higher expression in tumor samples, while others showed lower expression compared to normal samples
* Most genes remained relatively stable across both groups, suggesting that expression changes are concentrated in specific genes rather than across the entire genome

---

## 📊 Visual Insights

### 📉 Bar Plot (Top Differentially Expressed Genes)

* The bar plot highlighted genes with the strongest expression differences between tumor and normal samples
* Genes extending to the right showed higher expression in tumor tissues, while genes extending to the left showed lower expression in tumors compared to normal tissues


### 🔥 Expression Heatmap

* The heatmap displayed expression patterns of the top differentially expressed genes across all samples
* Tumor and normal samples showed noticeable differences in expression intensity
* Similar color patterns within groups suggested shared expression behavior among samples


### 🔗 Correlation Heatmap

* The correlation heatmap showed relationships among the top differentially expressed genes
* Some genes displayed strong positive correlations, suggesting similar expression behavior across samples


### 🌋 Volcano Plot

* The volcano plot combined fold change and statistical significance into a single visualization
* Genes farther from the center and above the significance threshold represented the strongest differentially expressed genes in the dataset


### 📉 Principal Component Analysis (PCA)

* PCA reduced the high-dimensional dataset into two principal components for visualization
* Tumor and normal samples showed partial separation, indicating differences in overall expression patterns
* Tumor samples appeared more dispersed, suggesting greater variability compared to normal samples

---

## 🔍 Key Findings

* Tumor and normal samples show high overall similarity in global gene expression profiles
* Despite this similarity, several genes exhibit statistically significant differential expression
* Differential expression patterns are concentrated in specific genes rather than across the entire genome
* Visualizations consistently revealed expression differences between tumor and normal tissues
* PCA indicated partial separation between both sample groups, supporting differences in overall gene activity

---

## 📌 Recommendations

* Perform pathway enrichment analysis (GO / KEGG) to investigate biological functions associated with significant genes
* Validate findings using external datasets such as GEO or TCGA
* Explore predictive modeling approaches for tumor vs normal classification
* Investigate gene–gene interaction patterns using co-expression or network analysis
* Further study top differentially expressed genes for potential biomarker exploration

---

## 🧠 Conclusion

This project demonstrates how statistical analysis and visualization techniques can be applied to gene expression data to identify meaningful differences between breast tumor and normal tissue samples.

Although tumor and normal samples showed strong overall similarity, several genes displayed significant differential expression patterns that may contribute to tumor-related biological processes.
 
---

## 📌 Limitations

* No clinical metadata (e.g., cancer subtype, treatment outcome, survival data) was included
* High-dimensional gene expression data may introduce statistical complexity
* Possible batch effects or technical variation were not explicitly controlled
* Findings are exploratory and not intended for clinical or diagnostic use
  
---

## 📂 Repository Structure

```bash
breast-cancer-expression-analysis/
├── notebook/
│   └── gene_expression_analysis.ipynb
├── images/
│   ├── volcano_plot.png
│   ├── expression_heatmap.png
│   └── pca_plot.png
└── README.md
```

---

## 🚀 Key Takeaway  

This project demonstrates how statistical analysis and visualization techniques can be applied to gene expression data to identify biologically meaningful differences between tumor and normal tissue samples.

---

## 👤 Author  

Emmanuel Achugo  
Data Analyst |Machine Learning & Predictive Analytics
