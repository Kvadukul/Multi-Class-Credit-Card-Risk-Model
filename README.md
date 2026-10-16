# Multi-Class-Credit-Card-Risk-Model

This repository benchmarks a Multi-Class Credit Risk Prediction Model (30,000-row financial dataset across 4 risk tiers: 0 to 3). It evaluates the impact of Bayesian hyperparameter optimization (Optuna) and compares a traditional gradient boosting tree architecture (XGBoost) against a deep learning self-attention model (FT-Transformer).



##  Model Evaluation & Architecture Comparison

| Model Architecture | Optimization Strategy | Best Macro F1-Score | Overall Accuracy |
| :--- | :--- | :--- | :--- |
| XGBoost Classifier | Bayesian Tuned (Optuna) | 0.7018 | 90% |
| FT-Transformer | Bayesian Tuned (Optuna) | 0.6194 | 85% |

---

##  Classification Report & Confusion Matrix (XGBoost)

Evaluated on a held-out test set of 6,000 samples:


              precision    recall  f1-score   support

           0       0.94      0.97      0.96      4622
           1       0.73      0.79      0.76       771
           2       0.67      0.42      0.52       529
           3       0.66      0.51      0.58        78

    accuracy                           0.90      6000
   macro avg       0.75      0.67      0.70      6000
weighted avg       0.89      0.90      0.89      6000

|Confusion Matrix:|
| :--- | :--- | :--- | :--- |
| 4505 | 114 | 2 | 1 |
| 56 | 607 | 96 | 12 |
| 207| 92 | 222 | 8 |
| 6 | 23 | 9 | 40 |
