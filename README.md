# AIML TASK-1
# Indian Liver Patient Dataset – Preprocessing & Cleaning

This project demonstrates how to clean and preprocess the **Indian Liver Patient Dataset (ILPD)** using a standard machine learning preprocessing workflow originally used for the Titanic dataset.

---

## 🎯 Objective

To prepare the Indian Liver Patient medical dataset for machine learning by handling missing values, encoding categorical variables, standardizing numerical features, and detecting/removing outliers.

---

## 📁 Dataset Info

- **Name:** Indian Liver Patient Dataset
- **File Name:** `Indian Liver Patient Dataset.csv`
- **Target Column:** `Dataset` (1 = Liver Disease, 2 = No Liver Disease)

---

## 🧰 Tools & Libraries

- Python 3 (Google Colab)
- Pandas
- NumPy
- Seaborn
- Matplotlib
- Scikit-learn

---

## ⚙️ Preprocessing Steps Followed

### ✅ 1. Import Dataset & Explore

- Used `pandas.read_csv()` to load the dataset.
- Used `df.info()` and `df.isnull().sum()` to inspect datatypes and missing values.

### ✅ 2. Handle Missing Values

- Replaced missing values in `Albumin_and_Globulin_Ratio` using **median imputation**.

### ✅ 3. Encode Categorical Data

- Encoded `Gender` as:
  - Male → 1
  - Female → 0

### ✅ 4. Standardize Numerical Features

- Used `StandardScaler` from `sklearn.preprocessing` to scale all numerical columns (excluding the target `Dataset`).

### ✅ 5. Visualize and Remove Outliers

- Visualized outliers using **Seaborn boxplots**.
- Removed outliers from all numerical columns using the **IQR (Interquartile Range)** method.

---

## 📊 Final Dataset Format

| Age | Gender | Total_Bilirubin | ... | Albumin_and_Globulin_Ratio | Dataset |
|-----|--------|------------------|-----|-----------------------------|---------|
|0.23 | 1      | -0.56            | ... | 0.45                        | 1       |

- All numerical columns are **standardized**.
- No missing values.
- Categorical features encoded numerically.
- Outliers removed.

---
