# Diabetes Prediction: Model Tuning & Validation

## Project Overview

This project focuses on predicting diabetes using the Pima Indians Diabetes Dataset. The objective was to improve model performance through hyperparameter tuning and validate the model using cross-validation techniques.

The project demonstrates the complete machine learning workflow, including data preprocessing, baseline model creation, hyperparameter optimization, model validation, and performance comparison.

---

## Problem Statement

Early detection of diabetes is critical for preventing severe health complications. This project aims to build a machine learning model capable of predicting whether a patient is likely to have diabetes based on medical diagnostic measurements.

---

## Dataset

Dataset: Pima Indians Diabetes Dataset

Features include:

* Pregnancies
* Glucose
* Blood Pressure
* Skin Thickness
* Insulin
* BMI
* Diabetes Pedigree Function
* Age

Target Variable:

* Outcome (0 = Non-Diabetic, 1 = Diabetic)

---

## Tools & Libraries

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn

---

## Data Preprocessing

The following preprocessing steps were performed:

* Loaded dataset into Pandas DataFrame
* Checked for missing values
* Replaced invalid zero values where necessary
* Split data into training and testing sets
* Feature scaling where required

---

## Baseline Model

Model Used:

* Random Forest Classifier

Initial Performance:

| Metric    | Before Tuning |
| --------- | ------------- |
| Accuracy  | 72.08%        |
| Precision | 60.71%        |
| Recall    | 61.82%        |
| F1 Score  | 61.26%        |
| ROC-AUC   | 69.80%        |

---

## Hyperparameter Tuning

Technique Used:

* GridSearchCV

Parameters Tested:

* n_estimators
* max_depth

Best Parameters Found:

```python
{
    'max_depth': 10,
    'n_estimators': 200
}
```

Cross Validation:

* 5-Fold Cross Validation
* Scoring Metric: Accuracy

Best Cross-Validation Score:

```python
0.8329
```

---

## Optimized Model Performance

| Metric    | After Tuning |
| --------- | ------------ |
| Accuracy  | 73.38%       |
| Precision | 62.07%       |
| Recall    | 65.45%       |
| F1 Score  | 63.72%       |
| ROC-AUC   | 71.62%       |

---

## Performance Comparison

The tuned Random Forest model outperformed the baseline model across all evaluation metrics.

Key improvements observed:

* Higher Accuracy
* Better Recall
* Improved F1 Score
* Better ROC-AUC performance
* Stronger model generalization

---

## Key Findings

* Hyperparameter tuning improved overall model performance.
* Cross-validation provided a more reliable estimate of model performance.
* Recall improved significantly, allowing the model to identify more diabetic patients.
* Random Forest proved effective for this classification problem.

---

## Challenges Encountered

* Selecting the right hyperparameters for tuning.
* Understanding the tradeoff between model complexity and generalization.
* Comparing multiple evaluation metrics beyond accuracy.
* Interpreting cross-validation results.

---

## Conclusion

The optimized Random Forest model achieved better predictive performance than the baseline model. Through Grid Search and Cross-Validation, the model became more reliable and generalizable. This project highlights the importance of model tuning and validation in building effective machine learning solutions.

---

## Author

Funbi Olowojesiku

Machine Learning & Data Analytics Intern

AnalystLab Africa Internship Program
