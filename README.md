# Clustering Biological Specimens by Morphological Features

End-to-end unsupervised learning pipeline for clustering Dry Bean biological specimens using morphological shape and size features. Includes full workflow: data extraction, preprocessing, feature engineering, optimal-k selection (Elbow + Silhouette), K-Means training, inference on production data, and internal evaluation.

---

## 📌 Project Overview

This project applies **unsupervised clustering (K-Means)** to group Dry Bean samples based on their geometric and morphological characteristics.  The goal is to automatically discover natural structure among bean types and support research, automated classification, and agricultural decision-making.

---

## 🎯 Problem Statement / Business Goal

Traditional dry bean identification depends on slow, subjective manual inspection.  
This project builds an **automated clustering system** that groups beans purely from shape-related features—enabling:

- Faster and scalable bean categorization  
- Objective and consistent grouping  
- Better support for agricultural research and quality control  

---

## 📂 Dataset Source & Citation

**Dataset:** Dry Bean Dataset  
**Source:** UCI Machine Learning Repository  
🔗 https://archive.ics.uci.edu/dataset/602/dry+bean+dataset  

**Citation:**  
Seker, Barbunya, Bombay, Cali, Dermosan, Horoz, and Sira — Dry Bean Dataset.  
UCI Machine Learning Repository (CC BY 4.0).

---
## 📁 Repository Structure (The structure and files formed after executing the entire notebook)

```txt
project/
├── data/
│   ├── Bean_Data_Full.csv
│   ├── Bean_Data_75pct.csv
│   ├── Bean_Data_25pct_Eval_Inf.csv
│   ├── predictions.csv
│   ├── result_summary.csv
|
├── artifacts/
│   ├── selected_features.pkl
│   ├── kmeans_model.pkl
│
├── Vector_Minds_Phase_1_and_4.ipynb
│
├── plots/
│   ├── training_clusters.png
│   ├── production_clusters.png
│   ├── training_vs_production_clusters.png
```
---

## 🚀 How to Run the Project

### 1️⃣ Open the Notebook
Use the main notebook:

`Vector_Minds_Phase_1_and_4.ipynb`

You may run it in:

- Google Colab (recommended)  
- Jupyter Notebook / VS Code  

---

### 2️⃣ Install Required Libraries

Upload or Copy the requirements.txt to your  project folder and run the pip install cell in the notebook
```
pip install -r requirements.txt
```



---

### 3️⃣ Run All Cells

Running the notebook will:

- Fetch the dataset (via `ucimlrepo`)
- Clean & preprocess the data  
- Apply PowerTransformer + StandardScaler  
- Reduce correlated features  
- Identify optimal k using Elbow + Silhouette  
- Train **K-Means (k = 7)**  
- Run inference on production dataset  
- Generate analysis plots  
- Save artifacts for reuse  

---

## 📊 Outputs Generated

### **✔ Visualizations**
- Training cluster scatter plot  
- Production cluster scatter plot  
- Training vs inference comparison  
- Correlation heatmap  
- Distribution & skew plots  

---

### **✔ Model Artifacts**
- `selected_features.pkl`  
- `kmeans_model.pkl`  

---

### **✔ Evaluation Metrics**
- Silhouette Score  
- Davies–Bouldin Index (Training & Inference)  
- Optional internal evaluation:
  - ARI / AMI  
  - Confusion Matrix  
  - Cluster Purity  

---
