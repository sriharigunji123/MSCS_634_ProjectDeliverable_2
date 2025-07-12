# MSCS_634_ProjectDeliverable_2

## Deliverable 2: Regression Modeling and Performance Evaluation

This deliverable focuses on predicting cholesterol levels (`chol`) using regression techniques on a heart disease dataset. The tasks included feature engineering, building regression models, performance evaluation, and applying cross-validation to assess model generalizability.

---

##  Feature Engineering

Performed one-hot encoding on all categorical columns (`sex`, `cp`, `fbs`, `restecg`, `exang`, `slope`, `ca`, `thal`) to convert them into numeric form. This transformation is necessary for machine learning algorithms that require numerical input. `drop_first=True` was used to avoid the dummy variable trap.

---

##  Target Variable

The target variable selected for this regression task is `chol` (serum cholesterol in mg/dl). All other features were used as independent variables.

---

##  Train-Test Split

The data was split into:
- **80% Training set** (used to train the models)
- **20% Testing set** (used to evaluate model performance)

This allows unbiased evaluation of the model’s ability to generalize.

---

##  Models Used

1. **Linear Regression** – A basic linear model assuming no regularization.
2. **Ridge Regression** – A linear model with L2 regularization to help mitigate overfitting and handle multicollinearity.

---

##  Model Evaluation Metrics

Both models were evaluated using the following:
- **MSE**: Mean Squared Error
- **RMSE**: Root Mean Squared Error
- **R² Score**: Explained variance

Cross-validation (5-fold) was used to evaluate model robustness and prevent overfitting.

---

## Results Summary

### Linear Regression:
- R² Score: Low
- RMSE: High
- CV MSE: Higher

### Ridge Regression:
- R² Score: Slightly better
- RMSE: Lower than Linear Regression
- CV MSE: Improved

---

### ✅ Best Performing Model: Ridge Regression

Ridge Regression showed slightly improved performance over Linear Regression, particularly in cross-validation. It proved to be more robust due to its regularization component.

---

##  Key Insights

- The dataset may not be highly predictive of `chol` using the provided features.
- Ridge Regression improved generalization slightly, validating the use of L2 regularization.
- Future work could explore:
  - Using different target variables
  - Feature selection techniques
  - Switching to classification (e.g., predicting `target` column)

---

##  Challenges Encountered

- Limited correlation between features and `chol` reduced model effectiveness.
- Initial feature formats were incompatible until encoded.
- R² scores were low for both models, indicating weak relationships.
