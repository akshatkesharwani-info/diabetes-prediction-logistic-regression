🩺 Diabetes Disease Prediction — Logistic Regression


Show Image Show Image

Overview

A hospital wants to screen patients for diabetes risk using diagnostic measurements. This project builds a logistic regression classifier and evaluates it with clinically appropriate metrics — not just accuracy.

Dataset


Pima Indians Diabetes Database — Kaggle


Tech Stack

Python · Pandas · NumPy · Seaborn · Scikit-learn (Logistic Regression)

Approach


Cleaned data — replaced medically-impossible zero values with NaN, imputed with the median
Checked class balance and used class_weight='balanced' to counter it
Scaled features and trained a Logistic Regression classifier
Evaluated with precision, recall, F1, AUC-ROC and a confusion matrix
Plotted the ROC curve to assess discrimination ability across thresholds
Interpreted model coefficients as clinical risk factors


Key Results & Insights


Accuracy ≈ 78%, AUC ≈ 0.83 — strong discrimination between diabetic and non-diabetic patients
Glucose has the largest logistic regression coefficient — the strongest individual risk factor
Recall matters more than precision here — missing a diabetic patient is the costlier clinical error
class_weight='balanced' measurably improved recall on the minority diabetic class
ROC curve sits well above the random-classifier baseline across all thresholds


How to Run

bashpip install -r requirements.txt
jupyter notebook diabetes_logistic_regression.ipynb

Project Structure

diabetes-prediction-logistic-regression/
├── notebooks/diabetes_logistic_regression.ipynb
├── images/  (confusion_matrix.png, roc_curve.png, feature_importance.png)
├── requirements.txt
└── README.md

Author

Akshat Kesharwani — LinkedIn · Portfolio
