# Credit Card Customer Segmentation (Unsupervised Learning)

## 📌 Project Overview

This project applies **K-Means clustering** to segment credit card customers based on their financial behavior.  
The objective is to uncover hidden customer groups using unsupervised learning techniques.

The workflow includes:
- Data cleaning
- Feature scaling
- Optimal cluster selection (Elbow + Silhouette)
- PCA dimensionality reduction
- Cluster interpretation

---

## 📊 Dataset

Dataset: Credit Card Dataset for Clustering  
- ~8,950 customers  
- 17 numerical behavioral features  
- Includes balance, purchases, credit limit, payments, cash advance usage, etc.

---

## ⚙️ Methodology

### 1️⃣ Data Preprocessing
- Dropped identifier column (`CUST_ID`)
- Removed missing values
- Standardized features using `StandardScaler`

### 2️⃣ Model Selection
- Used **Elbow Method** to analyze inertia (WCSS)
- Used **Silhouette Score** for cluster quality evaluation
- Selected **K = 2** as optimal number of clusters

### 3️⃣ Dimensionality Reduction
- Applied **PCA (2 components)**
- First 2 components explain ~48% of total variance
- Clustering after PCA improved silhouette score

---

## 📈 Key Results

- Silhouette Score (17D space): ~0.28
- Silhouette Score (2D PCA space): ~0.37
- PCA improved cluster separation by reducing noise
- Clusters primarily separated customers by:
  - Overall spending intensity
  - Credit usage behavior

---

## 🧠 Key Learnings

- Importance of feature scaling in distance-based algorithms
- Curse of dimensionality in high-dimensional clustering
- Difference between inertia and silhouette score
- PCA as a preprocessing step for improved clustering
- Interpreting cluster centroids for business insights
