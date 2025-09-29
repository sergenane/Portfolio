# Project 1: Predicting Diabetes Risk Using Patient Health Indicators

##  Oerview
Diabetes is one of the most prevalent chronic diseases worldwide, leading to severe complications like cardiovascular disease, kidney failure, and blindness. Early identification of at-risk individuals is critical to reduce complications and healthcare costs. However, current diagnosis usually happens after symptoms appear, limiting prevention opportunities. This project applies machine learning on patient health indicators to predict diabetes onset.

## Dataset
- **Source**: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/pima+indians+diabetes) / [Kaggle](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database)  
- **Records**: 768 patients (all female, Pima Indian heritage)  
- **Features**: 8 health indicators (e.g., glucose, BMI, age)  
- **Target**: Binary outcome (1 = diabetes, 0 = non-diabetes)

## Methods
- Data cleaning and preprocessing (handling zero values, scaling, SMOTE balancing)
- Exploratory Data Analysis (EDA): correlation heatmaps, feature distributions

<img width="960" height="872" alt="Correlation Matrix" src="https://github.com/user-attachments/assets/90d832b6-d0de-42c0-8256-1c7ce0c19691" />

  - Models: Logistic Regression, Decision Tree, Random Forest, XGBoost
- Evaluation metrics: Accuracy, Precision, Recall, F1-score, ROC-AUC
## Model Performance Comparison

| Model                | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|-----------------------|----------|-----------|--------|----------|---------|
| Logistic Regression   | 0.71     | 0.58      | 0.67   | 0.62     | 0.811   |
| Decision Tree         | 0.70     | 0.57      | 0.61   | 0.59     | 0.681   |
| Random Forest         | 0.75     | 0.63      | 0.72   | 0.67     | 0.814   |
| XGBoost              | 0.73     | 0.60      | 0.65   | 0.62     | 0.808   |

 
## Results
- **Best model**: XGBoost (AUC = 0.824, Accuracy = 75%)

<img width="701" height="556" alt="ROC Curve default vs tuned" src="https://github.com/user-attachments/assets/1853a2e6-b870-4f11-8939-c19cb2f050ce" />

<img width="416" height="325" alt="XGBoost optimized confusion matrrix" src="https://github.com/user-attachments/assets/8f2af701-ea09-4e7d-9fff-3085946d9819" />

- Key features: Glucose, BMI, and Age
- Feature importance: XGBoost balanced feature weighting better than Random Forest

<img width="876" height="479" alt="Feature importance Random Forest" src="https://github.com/user-attachments/assets/7df84c89-149b-4cea-94ce-ac1fde802cc1" />

<img width="876" height="479" alt="Feature importance XGBoost" src="https://github.com/user-attachments/assets/e40b6822-910d-44c5-a572-81d97064bb76" />


## Future Work
- Use larger, more diverse datasets
- Add lifestyle and genetic indicators
- Apply explainability methods (e.g., SHAP values) for clinician trust

## Support documents
- [Project 1 Jupyter notebook](https://github.com/sergenane/Portfolio/blob/main/Project1%3A%20Project1_DiabetesPrediction/Project%201.ipynb)
- [Project 1 Report/White Paper](https://github.com/sergenane/Portfolio/blob/main/Project1%3A%20Project1_DiabetesPrediction/Project%201%20White%20Paper.docx)
- [Project 1 Proposal](https://github.com/sergenane/Portfolio/blob/main/Project1%3A%20Project1_DiabetesPrediction/Project%20Proposal.docx)
---
