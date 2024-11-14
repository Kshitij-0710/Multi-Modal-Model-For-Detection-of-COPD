
---

# Machine Learning Model Ensemble for Classification

This project implements an ensemble of machine learning models for binary classification, using various techniques to enhance predictive performance and model robustness. The goal is to leverage multiple models, hyperparameter tuning, feature engineering, and ensemble methods to achieve the best possible accuracy and stability in predictions.

## Project Overview

This repository contains the following key components:

1. **Data Preparation**:
   - The dataset is loaded and processed to handle missing values through imputation.
   - Features and labels are split into training and test sets for model evaluation.

2. **Feature Engineering**:
   - Standard scaling is applied to normalize the feature values.
   - Polynomial feature expansion (degree 2) is used to introduce interaction terms, helping capture complex relationships between features.

3. **Model Selection and Hyperparameter Tuning**:
   - Four base models are selected:
     - **Random Forest**
     - **Support Vector Machine (SVM)**
     - **XGBoost**
     - **Logistic Regression**
   - Each model undergoes hyperparameter tuning with `RandomizedSearchCV` to identify the optimal settings, improving individual model performance.

4. **Individual Model Evaluation**:
   - Each tuned model is evaluated separately on the test set.
   - Metrics include **Accuracy**, **ROC AUC**, and a detailed **Classification Report** (Precision, Recall, F1-Score) for both classes.

5. **Model Agreement Calculation**:
   - The percentage of predictions on which all models agree is calculated, providing insight into prediction consistency across models.

6. **Ensemble Techniques**:
   - **Stacking Ensemble**: The project uses a stacking classifier, where a logistic regression model acts as a meta-classifier to combine predictions from the base models.
   - The stacking ensemble aims to improve overall accuracy by learning from the strengths of each individual model.

7. **Final Evaluation**:
   - The stacking ensemble is evaluated with the same metrics as the individual models, allowing a direct comparison of ensemble versus individual model performance.

## Results

The project includes the following outputs:
- Best hyperparameters for each individual model.
- Performance metrics for each model (Accuracy, ROC AUC, Classification Report).
- Percentage of agreement among models for test predictions.
- Final performance of the stacking ensemble model.

