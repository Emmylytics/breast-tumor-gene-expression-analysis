# 🧬 Comparative Gene Expression Analysis of Breast Tumor and Normal Samples (GSE25066 Dataset)

---

## 📊 Project Overview  

This project analyzes gene expression data from breast tumor and normal tissue samples to identify differential gene activity associated with breast cancer.

The analysis focuses on statistical comparison, correlation analysis, and visualization to uncover meaningful differences between both conditions at the gene level.

---

## 🎯 Objectives  

- Compare gene expression profiles between tumor and normal samples  
- Identify significantly differentially expressed genes  
- Validate expression differences using statistical testing  
- Visualize gene-level patterns for biological interpretation  

---

## 📁 Dataset Overview  

- **Dataset:** GSE25066 Breast Cancer Gene Expression Dataset  
- **Source:** Mendeley Data / Public gene expression repository  
- **Reference:** [Mendeley Data – Gene Expression Profiles of Breast Cancer](https://data.mendeley.com/datasets/v3cc2p38hb/1)  

---

## 📊 Dataset Structure  

This dataset consists of gene expression measurements from breast tumor and normal tissue samples.

- Each **row** represents a gene (geneID)  
- Each **column** represents a patient sample (tumor or normal)  
- Each **cell value** represents the expression level of a gene in a specific sample  

After preprocessing, the tumor and normal datasets were merged into a single expression matrix for comparative analysis:

```python
df = pd.concat([tumor, normal], axis=1)
```
---

## 🛠️ Tools Used  

- Python (Pandas, NumPy)  
- SciPy (t-test, Pearson correlation)  
- Matplotlib / Seaborn (Data Visualization)
- Jupyter Notebook  

---

## 🔬 Methodology  

1. **Data Loading & Inspection**  
   - Imported gene expression dataset  
   - Reviewed structure and sample distribution  

2. **Data Preprocessing**  
   - Handled missing or inconsistent values  
   - Aligned tumor and normal sample groups  
   - Prepared data for statistical comparison  

3. **Exploratory Data Analysis (EDA)**  
   - Examined overall expression distributions  
   - Identified patterns across gene sets  

4. **Statistical Analysis**  
   - Performed **Pearson correlation analysis (`pearsonr`)** to measure global similarity between tumor and normal expression profiles  
   - Conducted **t-tests** to identify genes with statistically significant differences  
   - Evaluated p-values to determine significance thresholds  

5. **Visualization**  
   - Bar plots for top differentially expressed genes  
   - Heatmaps to show expression relationships  

---

## 📈 Statistical Insights  

### 🔗 Pearson Correlation Analysis  
- Pearson correlation coefficient (~0.99) was computed using `scipy.stats.pearsonr`  
- Indicates a strong overall similarity between tumor and normal gene expression profiles  
- Despite this, gene-level differences still exist, requiring further statistical testing  

---

### 🧪 t-test Analysis  
- Positive t-statistic → higher expression in tumor samples  
- Negative t-statistic → higher expression in normal samples  
- p-value < 0.05 → statistically significant gene difference  

Key findings:
- A subset of genes showed statistically significant differences (p < 0.01)  
- Many genes showed no significant difference, indicating stable expression across conditions  

---

## 📊 Visual Insights  

### 📉 Bar Plot (Top Differential Genes)  
- Displays genes with the largest expression differences between tumor and normal samples  
- Highlights genes with strongest biological contrast  

---

### 🔥 Heatmap (Gene Expression Patterns)  
- Visualizes expression similarity across samples   
- Helps identify genes with correlated expression behavior  

---

## 🔍 Key Findings  

- Tumor and normal samples exhibit high overall similarity in gene expression profiles  
- Despite this, specific genes show statistically significant differential expression  
- Gene-level variation is more informative than global expression trends  
- Expression differences are not uniform but concentrated in specific gene sets  
- Visualization confirms clear separation patterns for selected genes

---

## 📌 Recommendations  

- Apply multiple testing correction (e.g., False Discovery Rate) to improve statistical reliability  
- Extend analysis with PCA to better visualize sample separation  
- Map significant genes to biological pathways for functional interpretation  
- Validate findings using external datasets for stronger biological confidence  
- Focus on top differentially expressed genes for biomarker exploration

---

## 🧠 Conclusions  

- Tumor and normal samples show high overall similarity in gene expression  
- However, specific genes exhibit statistically significant differences  
- These genes may serve as potential biomarkers for breast cancer research  
- Combination of Pearson correlation and t-tests provides both global and gene-level insight  

---

## 📌 Limitations  

- No clinical metadata (e.g., cancer stage, subtype, outcomes) for deeper biological interpretation  
- High-dimensional data with limited samples may affect statistical stability  
- No multiple testing correction (e.g., FDR), increasing risk of false positives  
- Pearson correlation reflects global similarity and may hide gene-level differences  
- Possible batch effects or technical variation were not explicitly controlled  
- Analysis is exploratory and not suitable for clinical or diagnostic use  
  
---

## 🚀 Key Takeaway  

This project demonstrates how statistical analysis and visualization techniques can be applied to gene expression data to identify biologically meaningful differences between tumor and normal tissue samples.

---

## 👤 Author  

Emmanuel Achugo  
Data Analyst | SQL • Python • Power BI • Machine Learning
