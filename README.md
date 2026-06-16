# 🩺 Diabetes Disease Prediction — Logistic Regression


![Python](https://img.shields.io/badge/Python-3.x-blue) ![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

## Overview
A hospital wants to screen patients for diabetes risk using diagnostic measurements. This project builds a logistic regression classifier and evaluates it with clinically appropriate metrics — not just accuracy.

## Dataset
- Pima Indians Diabetes Database — [Kaggle](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database)

## Tech Stack
Python · Pandas · NumPy · Seaborn · Scikit-learn (Logistic Regression)

## Approach
1. Cleaned data — replaced medically-impossible zero values with NaN, imputed with the median
2. Checked class balance and used `class_weight='balanced'` to counter it
3. Scaled features and trained a Logistic Regression classifier
4. Evaluated with precision, recall, F1, AUC-ROC and a confusion matrix
5. Plotted the ROC curve to assess discrimination ability across thresholds
6. Interpreted model coefficients as clinical risk factors

## Key Results & Insights
- **Accuracy ≈ 78%, AUC ≈ 0.83** — strong discrimination between diabetic and non-diabetic patients
- Glucose has the largest logistic regression coefficient — the strongest individual risk factor
- Recall matters more than precision here — missing a diabetic patient is the costlier clinical error
- `class_weight='balanced'` measurably improved recall on the minority diabetic class
- ROC curve sits well above the random-classifier baseline across all thresholds

## How to Run
```bash
pip install -r requirements.txt
jupyter notebook diabetes_logistic_regression.ipynb
```

## Project Structure
```
diabetes-prediction-logistic-regression/
├── notebooks/diabetes_logistic_regression.ipynb
├── images/  (confusion_matrix.png, roc_curve.png, feature_importance.png)
├── requirements.txt
└── README.md
```

## Author
Akshat Kesharwani — [LinkedIn](https://linkedin.com/in/akshat-kesharwani-b0452b346) · [Portfolio](https://akshatkesharwani-info.github.io)
