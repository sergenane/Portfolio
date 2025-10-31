# Project 2: Predicting Loan Default Risk Using Customer Financial Profiles

## Overview
Loan default poses a major financial challenge for lending institutions, directly affecting profitability and credit stability.  
This project applies **machine learning** techniques to predict whether a borrower will default based on their financial and demographic information.  
By identifying potential defaulters early, lenders can make more informed, ethical, and data-driven loan approval decisions.

---

## Dataset
**Source:** LendingClub Loan Default Prediction Dataset (Kaggle)  
**Records:** 255,347 borrowers  
**Features:** 17 financial and demographic attributes (e.g., Age, Income, CreditScore, LoanAmount, InterestRate, MonthsEmployed)  
**Target:** Binary — `Default` (1 = Default, 0 = Non-Default)  
**Challenge:** Imbalanced data — only 11.6% of loans defaulted  

---

## Methods
- **Data cleaning and preprocessing:**  
  - Removed unique identifiers  
  - Encoded categorical variables  
  - Standardized numerical columns  
  - Balanced data using **SMOTE (Synthetic Minority Oversampling Technique)**

- **Exploratory Data Analysis (EDA):**  
  - Correlation heatmap of numerical features  
  - Distribution comparison between default and non-default borrowers  
  - Default rate analysis by employment, marital status, and loan purpose

- **Models tested:**  
  - Logistic Regression  
  - Random Forest  
- **Evaluation metrics:**  
  Accuracy, Precision, Recall, F1-Score, ROC-AUC  

---

## Correlation Matrix
Correlation analysis revealed strong relationships between default likelihood and:
- **Age** (negative correlation)
- **Interest Rate** (positive correlation)
- **Income** (negative correlation)
- **Months Employed** (negative correlation)

<img width="1108" height="1016" alt="Correlation Matrix for numerical features" src="https://github.com/user-attachments/assets/78d5cebb-8dda-444a-baef-7b6b9ecd654b" />

<img width="989" height="590" alt="Correlation of each feature with defaut" src="https://github.com/user-attachments/assets/8b5a7756-b930-4cda-9208-782b92b6b8ec" />



---

## Model Performance Comparison

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|--------|-----------|------------|----------|------------|-----------|
| Logistic Regression | 0.68 | 0.22 | **0.70** | 0.34 | **0.753** |
| Random Forest | **0.88** | **0.46** | 0.09 | 0.14 | 0.735 |

---

## Results
- **Best model:** Logistic Regression (prioritizing recall)  
- **Key finding:** Logistic Regression correctly identified 70% of actual defaulters, while Random Forest missed most default cases.  
- In financial risk management, **recall is more critical** than accuracy — it’s better to flag a few extra customers than to approve risky ones.  

<img width="1490" height="1189" alt="Model performance comparaison" src="https://github.com/user-attachments/assets/4754e784-8db1-4b06-9118-f51f44f0a60b" />


---

## Key Features
Both models consistently identified the following as top predictors:
1. Age  
2. Interest Rate  
3. Income  
4. Months Employed  
5. Employment Type  

**Insight:** Younger borrowers with higher interest rates and shorter employment histories are more likely to default.

---

## Future Work
- Test **XGBoost** for enhanced predictive power  
- Apply **threshold tuning** to optimize the precision–recall balance  
- Add **macroeconomic variables** (e.g., inflation, credit market trends)  
- Build a simple dashboard using **Streamlit** or **Flask** for business integration  

---

## Support Documents
- [Project 2 White Paper](https://github.com/sergenane/Portfolio/blob/main/Project2%3A%20Predicting%20Loan/Project%202%20WHITE%20PAPER.docx)  
- [Project 2 Jupyter Notebook](https://github.com/sergenane/Portfolio/blob/main/Project2%3A%20Predicting%20Loan/Project.ipynb)  
- [Project 2 Proposal](Project%20Proposal.docx)  
- [Project 2 Presentation Slides](https://github.com/sergenane/Portfolio/blob/main/Project2%3A%20Predicting%20Loan/Predicting%20Loan%20Default%20Risk%20Using%20Customer%20Financial%20Profiles.pptx)

---

## Key Takeaway
Logistic Regression proved to be the most **interpretable** and **business-aligned** model, offering higher recall and actionable insights for credit risk mitigation.

---


