# Multiple Linear Regression: Model Interpretation and Statistical Inference

## Overview
This project explores **Multiple Linear Regression (MLR)** and focuses on how to **build, interpret, and evaluate regression models** with more than one predictor.  
The work extends simple linear regression by incorporating multiple explanatory variables, categorical predictors, and statistical inference tools.

The goal is not only to fit a model, but to understand:
- how each predictor contributes to the response,
- how reliable the coefficient estimates are,
- and what potential problems may affect interpretation.

---

## Objectives
The main objectives of this project are to:

- Understand the structure of a **Multiple Linear Regression model**
- Interpret regression coefficients while **holding other variables constant**
- Assess the **accuracy and reliability of coefficient estimates**
- Use **t-tests and p-values** to evaluate individual predictors
- Use the **F-test** to assess overall model significance
- Incorporate **categorical variables** using dummy coding
- Identify potential issues such as **multicollinearity**
- Compare **R² and Adjusted R²** for model evaluation

---

## Model Framework
The general multiple linear regression model used is:

\[
y = \beta_0 + \beta_1 x_1 + \beta_2 x_2 + \cdots + \beta_p x_p + \varepsilon
\]

where:
- \(y\) is the response variable,
- \(x_1, x_2, \ldots, x_p\) are predictor variables,
- \(\beta_0\) is the intercept,
- \(\beta_1, \ldots, \beta_p\) are regression coefficients,
- \(\varepsilon\) represents random error.

---

## Key Concepts Covered

### 1. Multiple Predictors
Unlike simple regression, MLR allows several predictors to be included simultaneously, enabling the effect of each variable to be isolated while controlling for others.

---

### 2. Coefficient Interpretation
Each coefficient represents the **expected change in the response variable** for a one-unit change in that predictor, **holding all other predictors constant**.

---

### 3. Statistical Inference
- **Standard Error (SE):** Measures uncertainty in coefficient estimates.
- **t-statistic:** Compares the size of a coefficient to its uncertainty.
- **p-value:** Assesses whether a predictor has statistically significant evidence of association with the response.

---

### 4. Overall Model Significance (F-test)
The F-test evaluates whether **at least one predictor** in the model explains variation in the response variable.

---

### 5. Categorical Variables (Dummy Variables)
Categorical predictors (e.g., State) are included using **dummy variables**, with one category chosen as a reference group.

---

### 6. Model Evaluation
- **R²:** Proportion of variance explained by the model.
- **Adjusted R²:** Adjusts R² for the number of predictors to penalize unnecessary variables.

---

### 7. Potential Issues
- **Multicollinearity:** High correlation among predictors can inflate standard errors and make individual coefficients difficult to interpret.
- Emphasis is placed on understanding that multicollinearity affects **interpretation more than prediction**.

---

## Files in This Repository
- `Homework3.ipynb` — Main notebook containing analysis and results
- `README.md` — Project description and explanation

---

## Key Takeaway
Multiple Linear Regression provides a powerful framework for modeling complex relationships, but meaningful interpretation requires careful attention to statistical inference, model assumptions, and diagnostic measures.


