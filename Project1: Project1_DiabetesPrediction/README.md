# Project 1: Predicting Diabetes Risk Using Patient Health Indicators

## 📌 Overview
This project applies machine learning models to predict the likelihood of diabetes onset using patient health indicators.  
It demonstrates how data-driven methods can support healthcare providers with early detection and prevention strategies.

## 📊 Dataset
- **Source**: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/pima+indians+diabetes) / [Kaggle](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database)  
- **Records**: 768 patients (all female, Pima Indian heritage)  
- **Features**: 8 health indicators (e.g., glucose, BMI, age)  
- **Target**: Binary outcome (1 = diabetes, 0 = non-diabetes)

## ⚙️ Methods
- Data cleaning and preprocessing (handling zero values, scaling, SMOTE balancing)
- Exploratory Data Analysis (EDA): correlation heatmaps, feature distributions
- Models: Logistic Regression, Decision Tree, Random Forest, XGBoost
- Evaluation metrics: Accuracy, Precision, Recall, F1-score, ROC-AUC

## 🏆 Results
- **Best model**: XGBoost (AUC = 0.824, Accuracy = 75%)
- Key features: Glucose, BMI, and Age
- Feature importance: XGBoost balanced feature weighting better than Random Forest

## 📂 Project Files
- `data/` → dataset (or link if too large)
- `notebooks/` → Jupyter Notebook with full code
- `reports/` → Proposal, White Paper, and Presentation slides

## 🔮 Future Work
- Use larger, more diverse datasets
- Add lifestyle and genetic indicators
- Apply explainability methods (e.g., SHAP values) for clinician trust

---
