# Bank Churn Prediction
**Problem Statement:** Banks face financial loss when customers leave. The goal is to build a predictive model that can help retain customers by identifying those most likely to churn.

**Aim:** This project aims to predict whether a customer will churn or not using classification models. The objective is to identify high-risk customers while avoiding unnecessary alerts to loyal ones, balancing both recall and precision through the F1 score.

**Data Preprocessing:**
1. Dropped non-informative features like CustomerID and Surname.
2. Handled outliers in Age and CreditScore by binning them into meaningful categories.
3. Scaled numerical features and encoded categoricals using ColumnTransformer.

**Imbalanced Dataset:** Used Balanced Random Forest Classifier from imblearn, which handles imbalance without oversampling.
- Tuned hyperparameters using Optuna to maximize F1 Score.
- Best model: BalancedRandomForestClassifier.

**Results and Evaluation:**
- F1 Score (churn class): 60.5%
- Accuracy: 81.8%
- ROC AUC: 0.86
- Used classification report and ROC Curve for model evaluation.
- Built a pipeline with a preprocessing and model for easy reuse and deployment.
