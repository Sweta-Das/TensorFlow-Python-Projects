# Linear Regression Model

- Linear Regression is a fundamental statistical and ML technique.
- It used for modeling the relationship between a dependent var. (target) and one/more independent vars. (predictors).

# Key Concepts

### 1. Simple Linear Regression

- Models the relationship between a single independent var. (X) and a dependent var. (Y).
    
    $Y$ = $\beta_0$ + $\beta_1$ $X$ + $\epsilon$
    
    - $Y$: Dependent variable
    - $X$: Independent variable
    - $\beta_0$: Intercept (the value of Y when X = 0)
    - $\beta_1$: Slope (the change in Y for a unit change for X)
    - $\epsilon$: Error term (captures the variability in Y not explained by X)

### 2. Multiple Linear Regression

- Extends simple linear regression to include multiple independent variables.
    
    $Y$ = $\beta_0$ + $\beta_1X_1$ + $\beta_2X_2$ + ... + $\beta_nX_n$ + $\epsilon$
  
    - $X_1, X_2, ..., X_n$: Multiple independent variables
    - $\beta_0, \beta_1, ..., \beta_n$: Coeff. of the model

### 3. Polynomial Regression

- Extends linear regression by modeling the relationship between the dependent and independent variables as an nth degree polynomial.

# Features

### 1. Linearity

- Assumes a linear relationship between the dependent and independent variables.

### 2. Least Squares Method

- Estimates the parameters ($\beta_0, \beta_1, ..., \beta_n$) by minimizing the sum of the squared differences between observed and predicted values (residuals).

### 3. Assumptions

- ***Independence***: Observations are independent of each other.
- ***Homoscedasticity***: Residuals have constant variance.
- ***Normality***: Residuals of the model are normally distributed (particularly important for small sample sizes)

### 4. Model Evaluation

- ***R-squared*** ($R^2$): Measures the proportion of variability in the dependent var. explained by the independent vars. Ranges from 0 to 1.
- ***Adjusted R-squared***: Adjusts $R^2$ for the no. of predictors in the model, providing a more accurate measure when multiple predictors are involved.
- ***Mean Squared Error (MSE)***: Avg. of the squared differences between observed and predicted values.
- ***Root Mean Squared Error (RMSE)***: Square root of MSE, providing a measure in the same units as the dependent variable.

### 5. Statistical Significance

- ***p-value***: Tests the null hypothesis that a coefficient = 0 (no effect). A low p-value (< 0.05) indicates statistical significance.
- ***t-statistic***: Used to determine if a particular coeff. is significantly different from 0.

### 6. Diagnostics & Validation

- ***Residual Plots***: Checks for non-random patterns to diagnose issues like non-linearity or heteroscedasticity.
- ***Variance Inflation Factor (VIF)***: Detects multi-collinearity among predictors. High VIF (> 10) indicate multicollinearity.
- ***Cross-validation***: Splitting the dataset into training and testing sets to evaluate the model’s performance on unseen data.
