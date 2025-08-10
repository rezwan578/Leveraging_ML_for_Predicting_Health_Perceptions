# Leveraging Machine Learning for Predicting Health Perceptions: A Behavioral Analytics Approach Using U.S. National Survey Data    
 
***Accepted at the 25th International Conference on Electronic Business (ICEB 2025),  affiliated  with  the 
Association  for  Information  Systems  (AIS)***

---

## Overview

This repository accompanies a research paper that uses interpretable machine learning to identify key predictors of **self-reported health (SRH)** among American adults, using data from the **2023 Behavioral Risk Factor Surveillance System (BRFSS)**.

The work emphasizes the importance of **behavioral and socio-economic** factors in shaping perceived health and contributes to the intersection of **data science**, **public health**, and **behavioral analytics**.

---

## Abstract (Summary)

This study applies machine learning to identify the key predictors of self-reported health (SRH) among U.S. adults using the 2023 BRFSS dataset. Five models were evaluated: **Logistic Regression, Random Forest, XGBoost, Decision Tree**, and a **Stacked ensemble**. 

To address class imbalance, **Edited Nearest Neighbors (ENN)**, **SMOTE**, and **Repeated Undersampling** were tested, with the latter showing the best performance. Logistic Regression achieved an AUC of **0.81**, and the Stacked model slightly improved it to **0.82**.

**SHAP and feature importance analysis** revealed that income, employment status, physical activity, and mental health status were stronger predictors than traditional risk factors like smoking or heavy drinking. The results are interpreted using the **Social Determinants of Health (SDOH)** and **Health Belief Model (HBM)** frameworks.

> **Key Insight**: Behavioral and socio-economic variables outweigh clinical and lifestyle risks in shaping health perception.

---

## Methods (High-Level)

- **Dataset**: BRFSS 2023 (CDC)
- **Preprocessing**: Feature selection, missing value handling
- **Class Balancing**: ENN, SMOTE, Repeated Undersampling
- **Models Used**:
  - Logistic Regression
  - Decision Tree
  - Random Forest
  - XGBoost
  - Stacked Ensemble Model
- **Interpretability**: SHAP values, Feature Importances
- **Evaluation Metric**: AUC

---

## Repository Notice

Parts of the codebase and complete structure will be shared after the official presentation to preserve originality and intellectual contribution. The goal is to maintain academic integrity and avoid premature duplication.

---

## Keywords

`Self-reported Health` · `BRFSS` · `Machine Learning` · `Class Imbalance` · `Health Analytics` · `Behavioral Data`


---

## Repository Structure (Coming Soon)

