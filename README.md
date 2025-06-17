
# 🛍️ Consumer Spending Prediction from Mailing Campaigns

## 📌 Overview

This project explores how consumer characteristics influence purchasing behavior and spending levels in response to a marketing mailing campaign. The task is to predict the **Spending** amount using customer attributes and evaluate multiple regression models for performance comparison.

## 🎯 Problem Statement

Given anonymized consumer data, the goal is to:
1. Predict **Spending** based on customer attributes (excluding the binary `Purchase` variable).
2. Compare predictive performance across various regression models.
3. Evaluate model performance differences between the full dataset and a restricted subset where `Purchase = 1`.

## 📁 Dataset

- Provided via course portal: anonymized customer mailing data
- Features include demographic, behavioral, and campaign-specific variables
- Two targets:
  - `Purchase`: whether the customer made a purchase (0/1)
  - `Spending`: dollar amount spent (numeric)

## 🧠 Models Implemented

| Model Type         | Techniques Used                     |
|--------------------|-------------------------------------|
| Linear Regression  | Ordinary Least Squares              |
| k-NN Regression    | Scikit-learn's `KNeighborsRegressor`|
| Regression Tree    | DecisionTreeRegressor               |
| SVM Regression     | Support Vector Regression (`SVR`)   |
| Neural Network     | MLPRegressor                        |
| Ensemble Methods   | Random Forest, Gradient Boosting    |

- Feature scaling applied using `StandardScaler`
- Hyperparameter tuning via `GridSearchCV`
- Evaluation based on RMSE and R² metrics

## 📊 Key Results

- Ensemble models (especially Random Forest) yielded the lowest prediction error and highest R² score.
- SVM required careful tuning and performed well with scaled data.
- Linear regression underperformed due to lack of nonlinear flexibility.
- Models were also trained on a filtered dataset (`Purchase = 1`) to predict spending only for actual buyers. Results were compared with models trained on the full dataset.
- Filtering for buyers only (Task b) generally improved predictive accuracy across models.
- Models trained on the full dataset (including non-buyers) exhibited greater variance and reduced performance, likely due to noise from zero-spending consumers.

## 👤 Author

Yi Hsiang (Royce) Yen  
MS in Business Analytics, University of Minnesota
