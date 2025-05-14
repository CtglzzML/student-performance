# Student Performance Analysis

This project explores and compares three different regression models using the "student-mat.csv" dataset:

- Simple Linear Regression  
- Multiple Linear Regression  
- Polynomial Regression  
- Logistic Regression (for classification)

## Dataset

The dataset is based on student performance in Portuguese schools, including attributes such as grades, family background, study time, and final results. The target variable is `G3` (final grade).

Source: UCI Machine Learning Repository

## Models Used

### 1. Simple Linear Regression
We predict the final grade `G3` using a single feature: the second period grade `G2`.

### 2. Multiple Linear Regression
We predict `G3` using multiple features: `G1`, `G2`, `famrel`, `studytime`, and `Pstatus`. Pstatus is ordinal-encoded before modeling.

### 3. Polynomial Regression
We model a curved relationship between `G1` and `G3` by applying `PolynomialFeatures(degree=2)` to the feature before using `LinearRegression`.

### 4. Logistic Regression
We create a binary classification problem: predicting whether a student passed (`G3 >= 10`) or not. We use `G1` and `G2` as input features. We also experiment with tuning the `C` parameter to improve performance.

## Evaluation Metrics

- **Linear & Polynomial Regression**:  
  - R² Score  
  - SSE (Sum of Squared Errors)

- **Logistic Regression**:  
  - Accuracy  
  - Confusion Matrix

## Conclusion

- Simple and multiple linear regression models perform well, especially when using `G2` and `G1` together.  
- Polynomial regression may overfit if not properly regularized or scaled.  
- Logistic regression with tuned `C` improves classification performance noticeably.

