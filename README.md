# 🎬 Predicting Box Office Success with ML Models on Metacritic Data

## 📘 Project Overview

In this project, we investigate how various features — including expert reviews, production budgets, and emotional tone — affect the **box office performance of movies**. Using the Metacritic dataset, our goal is to predict financial success using multiple machine learning models, embedding techniques, and explainability methods.

This work was completed for the **AI Methods for Business (2024/25)** course.

---

## 🎯 Business Question

**Can we predict a movie’s box office success using pre-release expert reviews and production-related features?**

### Sub-questions:
1. How does emotional tone in expert reviews relate to box office performance?
2. Can embedding-based review features improve predictive power?
3. Which model performs best: Linear Regression, Random Forest, or ANN?
4. What factors most influence the predictions?
5. Can SHAP and counterfactual explanations provide actionable business insight?

---

## 🧪 Methodology

### 🔹 1. Exploratory Data Analysis
- Performed in `Prediction_ML.ipynb`
- Explored two datasets (`sales.csv`, `metaclean.csv`)
- Cleaned and merged on `movie_title`
- Visualized key features and their relationships with revenue
- Addressed missing values using **KNN imputation** and **median fill**; chose **median** due to better correlation performance

### 🔹 2. Feature Engineering
- Used **ANOVA** and **Pearson correlation** for feature selection
- One-hot encoding of categorical variables
- Applied **SVD** for dimensionality reduction

### 🔹 3. Expert Review Embeddings
- Implemented in `Transformer_1.ipynb`
- Selected only **pre-release expert reviews**
- Used **HuggingFace Transformers** for embedding extraction
- Applied **PCA** to reduce dimensions
- Output stored in `expert_transformer_1.xlsx` and later merged into the main model

### 🔹 4. Model Training
- Split data into train/test sets (80/20)
- Trained:
  - Linear Regression (baseline)
  - Random Forest
  - Artificial Neural Network (ANN)
- Monitored ANN loss over epochs

### 🔹 5. Explainability
- Used **SHAP** for global and local feature importance
- Added **counterfactual examples** to test model robustness

---

## 🧠 Tools & Libraries

- `pandas`, `numpy`, `matplotlib`, `seaborn`
- `sklearn`: regression, RandomForest, SVD, train/test split
- `tensorflow` / `keras` for ANN
- `shap` for explainability
- `transformers` (HuggingFace) for NLP embedding

---

## 📁 Repository Structure

```bash
.
├── Prediction_ML.ipynb                 # Main notebook: EDA, modeling, SHAP
├── Transformer_1.ipynb                 # Embedding expert reviews before release
├── expert_transformer_1.xlsx           # PCA-reduced review embeddings
├── data/                               # Raw & processed datasets
├── docs/
│   └── Final_Assignment_Report.pdf     # Full report (optional)
├── README.md                           # This file
