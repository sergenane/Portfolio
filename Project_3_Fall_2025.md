# Project 3: Movie Review Sentiment Intelligence
### *Fine-Grained Sentiment & Aspect Extraction Using Transformer-Based NLP Models*

---

## Overview
Movie reviews often contain nuanced opinions about acting, plot, pacing, and emotional tone.  
Traditional sentiment classification only outputs **positive or negative**, missing the deeper *why* behind emotions.

This project applies **Natural Language Processing (NLP)** — from **TF-IDF + Logistic Regression** to **Transformer-based BERT models** — to:

- Classify movie review sentiment  
- Extract deeper aspects (acting, plot, direction, genre, etc.)  
- Deliver insights useful for studios and streaming platforms  

---

## Dataset
**Source:** IMDB Large Movie Review Dataset (Kaggle)  
**Records:** 50,000 reviews  
**Classes:** 25,000 positive, 25,000 negative  
**Format:** Raw, noisy text containing HTML tags and inconsistent structure  
**Goal:** Build a reliable sentiment and aspect analysis pipeline  

---

## Methods

### **1. Data Cleaning & Preprocessing**
- Removed HTML tags (like `<br />`)  
- Removed punctuation and numbers  
- Lowercased all text  
- Removed stopwords  
- Lemmatized text to base form  
- Generated cleaned `clean_review` column for modeling  

---

## Exploratory Data Analysis (EDA)

### Key Findings
- Positive reviews commonly use: **great, love, excellent, amazing**  
- Negative reviews emphasize: **bad, worst, boring, awful**  
- Both classes mention: **film, movie, story, character**  
- Average review length ≈ **118 words**  
- Text length alone does not predict sentiment  

<img width="1589" height="562" alt="Word cloud" src="https://github.com/user-attachments/assets/e9ef18cf-377c-489f-b076-ed72150eaa33" />

<img width="1027" height="549" alt="Distribution of Review Lengths by Sentiment" src="https://github.com/user-attachments/assets/4990c344-c8d2-4e15-a58a-16cd3c327878" />

<img width="1786" height="790" alt="Top 20 Words in positive Reviews" src="https://github.com/user-attachments/assets/ac08eda0-c75a-4b6e-a6ad-d5dafee0568d" />


## Models

### **1. Baseline — TF-IDF + Logistic Regression**
- Accuracy: **88.91%**  
- F1-score: **0.89**  
- Balanced precision/recall  
- Strong predictors learned:  
  - Positive: *great, excellent, wonderful, best*  
  - Negative: *worst, awful, boring, terrible*  

<img width="638" height="528" alt="Confusion Matrix" src="https://github.com/user-attachments/assets/82767373-87a2-4ad0-b1b4-85e4b9a83e56" />


---

### **2. Advanced Model — Fine-Tuned BERT**
- Accuracy: **91.23%**  
- F1-score: **0.9131**  
- Precision: **91.22%**  
- Recall: **91.39%**  
- Improvement over baseline: **+2.32%**  
- Handles negation, context, sarcasm (e.g., “not bad”)  

<img width="638" height="528" alt="Confusion Matrix BERT Model" src="https://github.com/user-attachments/assets/7e4786ba-bd3d-4b9e-9b06-a2ae8501d695" />


---

## Aspect Extraction (LDA Topic Modeling)

Topic modeling revealed **five key aspects** reviewers care about:

1. **Overall Film Quality** — 94.3%  
2. **Acting** — 67.2%  
3. **Plot** — 61.5%  
4. **Technical Elements** — 37.6%  
5. **Direction** — 34.6%  

These aspects show *why* sentiment is positive or negative, not just what it is.

---

## Results Summary

| Model | Accuracy | F1-Score |
|-------|----------|-----------|
| TF-IDF + Logistic Regression | 0.8891 | 0.8900 |
| **BERT (Fine-Tuned)** | **0.9123** | **0.9131** |

### Key Insight  
BERT improved accuracy by **+2.32%**, which is significantly meaningful for large-scale review analysis.

---

## Business Impact
- Automates sentiment analysis at **91%+ accuracy**  
- Extracts actionable insights on acting, story, pacing, direction  
- Saves hours of manual review reading  
- Helps studios improve casting decisions, plot refinement, and marketing strategy  
- Enables real-time viewer feedback monitoring  

---

## Ethical Considerations
- Uses only **public, anonymized** IMDB data  
- Protects user privacy (no personal identifiers)  
- Requires monitoring for model bias  
- Intended for decision-support, not automated decision replacement  

---

## Future Work
- Enhance sarcasm detection  
- Expand to multilingual reviews  
- Build real-time interactive dashboards  
- Experiment with hybrid BERT + LDA systems  
- Implement ensemble NLP models for further improvements  

---

## Support Documents
(Add links after uploading your files to GitHub)

- [Project 2 White Paper](https://github.com/sergenane/Portfolio/blob/main/Project2%3A%20Predicting%20Loan/Project%202%20WHITE%20PAPER.docx)  
- [Project 2 Jupyter Notebook](https://github.com/sergenane/Portfolio/blob/main/Project2%3A%20Predicting%20Loan/Project.ipynb)  
- [Project 2 Proposal](https://github.com/sergenane/Portfolio/blob/main/Project2%3A%20Predicting%20Loan/Project%20Proposal.docx)  
- [Project 2 Presentation Slides](https://github.com/sergenane/Portfolio/blob/main/Project2%3A%20Predicting%20Loan/Predicting%20Loan%20Default%20Risk%20Using%20Customer%20Financial%20Profiles.pptx)


---

## Key Takeaway
The fine-tuned BERT model provides **superior, context-aware sentiment analysis**, while aspect extraction reveals the *drivers* of audience sentiment — delivering powerful insights for film studios, marketers, and streaming platforms.

---
