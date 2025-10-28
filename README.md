# 🧠 PCA on Arcene Dataset

## 📄 Project Overview
This project demonstrates **Principal Component Analysis (PCA)** on the **Arcene dataset**, a high-dimensional dataset commonly used for feature selection and dimensionality reduction experiments.  
The goal is to reduce the large number of features while retaining most of the variance in the data.

---

## 📂 Dataset Description
The dataset contains several files:

| File Name              | Description |
|------------------------|-------------|
| `arcene_train.data`    | Training features (numeric values) |
| `arcene_train.labels`  | Labels for the training data (+1 or -1) |
| `arcene_valid.data`    | Validation features (used for testing) |
| `arcene.param`         | Parameter file (not used in this analysis) |

> Note: This dataset does **not include** `arcene_valid.labels`, so PCA is performed without validation labels.

---

## ⚙️ Steps Performed

### 1. Import Libraries
Used essential Python libraries:
- `pandas` and `numpy` for data handling  
- `sklearn.preprocessing.StandardScaler` for feature scaling  
- `sklearn.decomposition.PCA` for dimensionality reduction  
- `matplotlib.pyplot` for visualization  

### 2. Load the Dataset
Read the training and validation data files using `pandas.read_csv()` with `delim_whitespace=True` since the dataset is space-separated.

## 🧩 Standardize the Data

Before applying PCA, the dataset is standardized so that each feature has a **mean of 0** and a **variance of 1**.  
This step ensures that features with large numerical ranges do not dominate the principal components.

---

## ⚙️ Apply PCA

After standardization, PCA is applied to reduce the **high-dimensional feature space** into **50 principal components**.  
This helps capture the most important variance in the data while significantly reducing computational complexity.

---

## 📊 Visualize Explained Variance

The **cumulative explained variance curve** is plotted to observe how much total variance is captured as the number of components increases.  
This helps determine the optimal number of components needed to represent most of the data’s information effectively.
