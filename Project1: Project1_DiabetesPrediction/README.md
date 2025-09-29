# Project 1: Predicting Diabetes Risk Using Patient Health Indicators

## Overview
This project explores how machine learning can be applied to predict diabetes onset using patient health indicators.  
The goal is to demonstrate how data-driven models can support healthcare providers with early detection, prevention, and better decision-making.  

---

## Dataset
- **Source**: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/pima+indians+diabetes) / [Kaggle](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database)  
- **Records**: 768 patients (all female, Pima Indian heritage)  
- **Features**: 8 health indicators (pregnancies, plasma glucose, blood pressure, skin thickness, insulin, BMI, diabetes pedigree function, age)  
- **Target Variable**: Binary (1 = diabetes, 0 = non-diabetes)

---

## Methods
1. **Data Preparation**
   - Handled zero values in features like insulin and skin thickness by replacing them with median values.  
   - Standardized continuous variables to avoid scale bias.  
   - Applied **SMOTE (Synthetic Minority Oversampling Technique)** to address class imbalance.

2. **Exploratory Data Analysis (EDA)**
   - Correlation heatmap to examine feature relationships.  
   - Distribution plots for each variable.  
   - Target class balance visualization.

3. **Modeling**
   - Logistic Regression (baseline, interpretable).  
   - Decision Tree (rule-based, prone to overfitting).  
   - Random Forest (ensemble of trees, improved stability).  
   - XGBoost (gradient boosting, best performance).  

4. **Evaluation Metrics**
   - Accuracy, Precision, Recall, F1-score, ROC-AUC.  
   - ROC curves and confusion matrices were used for performance comparison.

---

## Results
- **Best Model**: **XGBoost**  
  - Accuracy: ~75%  
  - ROC-AUC: 0.824  
  - Improved recall after threshold tuning.  

- **Key Predictors**: Glucose, BMI, and Age.  
- **Feature Importance**: XGBoost distributed importance more evenly, reducing over-reliance on a single variable compared to Random Forest.  

---

## Project Files
- `data/` → Pima Indians Diabetes dataset (or download via UCI/Kaggle links above).  
- `notebooks/` → Jupyter Notebook (`Project1.ipynb`) with code and analysis.  
- `reports/` →  
  - `Milestone1_Proposal.docx`  
  - `Project1_WhitePaper.docx`  
  - `Presentation_Slides.pptx`  

---

## Future Work
- Expand to larger, more diverse datasets.  
- Add lifestyle and genetic indicators.  
- Apply **explainability tools (e.g., SHAP values)** to increase clinician trust.  

---

## Ethical Considerations
- Data is anonymized to protect patient privacy.  
- Models must avoid predictive bias and be applied fairly.  
- Predictions should **support, not replace**, clinical judgment.  

---
