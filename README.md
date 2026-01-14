# Leveraging Machine Learning for Predicting Health Perceptions: A Behavioral Analytics Approach Using U.S. National Survey Data    
 
***Published in the 25th International Conference on Electronic Business (ICEB 2025),  affiliated  with  the 
Association  for  Information  Systems  (AIS)***

---

## Project overview

This repository showcases an interpretable machine learning pipeline for predicting self-rated health (good vs poor) among U.S. adults using the **2023 Behavioral Risk Factor Surveillance System (BRFSS)** national survey dataset. The project accompanies the ICEB 2025 paper “Leveraging Machine Learning for Predicting Health Perceptions: A Behavioral Analytics Approach Using U.S. National Survey Data.

The work emphasizes the importance of **behavioral and socio-economic** factors in shaping perceived health and contributes to the intersection of **data science**, **public health**, and **behavioral analytics**.

---

## Key contributions

- End-to-end pipeline: data cleaning, feature engineering, class balancing, model training, and evaluation on BRFSS 2023.
- Focus on health perceptions: modeling self-rated health (SRH) using socio-demographic, behavioral, psychosocial, and clinical factors.
- Imbalanced learning: comparison of SMOTE, ENN, SMOTE-ENN, and a repeated under-sampling strategy with detailed performance reporting.
- Interpretable modeling: logistic regression and a stacked ensemble achieve AUC ≈ 0.81–0.82 with balanced F1 across both health classes.
- Research-ready code: implemented in Python 3.11 with scikit-learn, XGBoost, imbalanced-learn, and SHAP for explainability.

---

## Repository structure

ML_model_train.ipynb – Main notebook containing:
---

- BRFSS 2023 loading and preprocessing (selection of 19 features, cleaning, encoding).​
- Multiple balancing strategies: SMOTE, ENN, SMOTE-ENN, and repeated under-sampling.​
- Model training: Logistic Regression, Random Forest, XGBoost, Decision Tree, and Stacked Ensemble.​
- Evaluation: confusion matrices, classification reports, cross-validated AUC/F1, and ROC curves.​
- SHAP-based interpretation for feature importance and directional effects.

Leveraging-Machine-Learning-for-Predicting-Health-Perceptions.pdf – Published ICEB 2025 paper describing the theoretical framing, methodology, and empirical findings.

---

## Methods and models

# Data & target:
- Source: 2023 BRFSS (Behavioral Risk Factor Surveillance System), 433,324 records and 350+ attributes; after cleaning, 117,386 records are used.
- Target: Self-rated general health recoded to binary – “Good” (excellent/very good/good) vs “Poor” (fair/poor).
- Predictors (19 features): age group, sex, race/ethnicity, education, income, employment, exercise, smoking, heavy drinking, diabetes, heart attack, stroke, cancer, BMI category, depression, days of poor mental health, healthcare provider, and checkup regularity.

# Handling class imbalance
Class distribution is skewed (≈76% good vs 24% poor health), so multiple strategies are evaluated.
Implemented in the notebook:
- SMOTE oversampling.
- ENN (Edited Nearest Neighbours).
- SMOTE-ENN hybrid.
- Repeated under-sampling: create 5 balanced subsets, train models on each, and aggregate performance.

Repeated under-sampling yields the most balanced F1 for both classes and is used in the final models.

# Models
All models are implemented with scikit-learn / XGBoost APIs in Python 3.11.
- Logistic Regression (baseline and cross-validated).
- Random Forest (with class weights and CV).
- XGBoost classifier.
- Decision Tree (depth-constrained with CV).
- Stacked Ensemble (LR, RF, XGB, DT, KNN as base learners with LR meta-learner).

### Model performance

| Model              | AUC  | Precision | Recall | F1-score |
|--------------------|:----:|:---------:|:------:|:--------:|
| Logistic Regression| 0.81 | 0.73      | 0.73   | 0.73     |
| Random Forest      | 0.72 | 0.71      | 0.71   | 0.71     |
| XGBoost            | 0.73 | 0.73      | 0.73   | 0.73     |
| Decision Tree      | 0.72 | 0.72      | 0.72   | 0.72     |
| Stacked Ensemble   | 0.82 | 0.74      | 0.74   | 0.74     |



# Interpretation & key findings
- Top predictors: poor mental health days, exercise, income, employment, and diabetes show the strongest influence on self-rated health in SHAP analysis.
- Behavioral and socioeconomic factors (mental health, physical activity, income, employment) dominate over traditional clinical risk behaviours like smoking or heavy drinking for perceived health.
- Under Social Determinants of Health (SDOH) and Health Belief Model (HBM), results highlight how lived social context and beliefs shape perceived health beyond purely clinical status.

# Academic & portfolio use
- Applied health analytics on large-scale national survey data (BRFSS 2023).
- Handling severe class imbalance with multiple resampling techniques.
- Building interpretable models with logistic regression and SHAP, alongside stronger ensembles.
- Connecting ML results to public health theory (SDOH and HBM) in a peer-reviewed conference paper.

If you use this project in academic work, please cite the journal paper. You can also access it online at - https://aisel.aisnet.org/iceb2025/1/

---

