# Risk Analysis Lending Club

This repository contains **Risk_Analysis_Lending_Club.ipynb**, a Jupyter/Colab notebook that walks through:

- **Data ingestion & cleaning**: parsing dates, handling missing values, encoding categoricals  
- **Exploratory Data Analysis (EDA)**: distributions, segment comparisons (good vs. bad loans), region-based time series  
- **Feature engineering**: interest-rate tiers, income categories, credit policy flags  
- **Visualisation**: Seaborn and Plotly charts (histograms, box/violin plots, heatmaps, stacked bars, time series)  
- **Modeling**:  
  - Logistic Regression & Decision Trees (Sklearn)  
  - Deep Neural Networks (TensorFlow / Keras)  
- **Evaluation**: ROC/AUC, confusion matrix, precision/recall, accuracy  

It’s a template you can adapt to any loan-risk dataset, with plenty of custom plotting and interactive visuals.

---

## ✨ Features

- Clean & modular code cells with detailed commentary  
- Interactive Plotly figures for:
  - Correlation heatmap  
  - Income-purpose interest-rate dot plot  
  - Stacked bar of good vs. bad loans by region  
- End-to-end TensorFlow/DNN training using `tf.data.Dataset` pipelines  
- Easy one-line conversion to Google Colab

---

## Data
The primary dataset is Lending Club loan records, containing fields such as:

issue_d, loan_amount, funded_amount, interest_rate, term,
grade, sub_grade, home_ownership, annual_income,
…and loan outcome/status fields

Note: Due to size constraints, the raw CSV is not included here. You can download it from Kaggle or your own data source and place it in data/.

---

## 🛠 Methodology
### 1. Data Cleaning

Parse dates (issue, payment history)

Handle missingness in saving_accounts, checking_account

Convert “36 months” → 36, strip “%” from rates, etc.

### 2. EDA & Visualization

Histograms & KDEs of loan/funded amounts

Box/violin plots by income tier & loan condition

Time-series of loan issuance by region

Correlation heatmap of numeric features

### 3. Feature Engineering

Income buckets (Low/Medium/High)

Interest-rate tiers (Low/High)

Credit-policy flags

### 4. Modeling

**Sklearn**: Logistic Regression, Decision Tree

**TensorFlow/Keras**: 2-layer ReLU DNN

Use tf.data.Dataset with shuffling & prefetch for memory efficiency

### 5. Evaluation

Confusion matrix, ROC/AUC curves

Precision, recall, F1-score

---

## 📈 Results & Visuals
(Some highlights – see the notebook for full-size interactive versions)

| Visualisation  | Insight                                                    |
|----------------|------------------------------------------------------------|
|                | Regional loan‐issue trends over time                       |
|                |  Strong correlation between installment & loan_amount      |
|                |  Higher‐income borrowers tend to get lower rates           |


---
