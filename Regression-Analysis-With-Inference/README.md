# Linear Regression: Core Concepts, Inference, and Diagnostics

## 1. Linear Regression Model

### Population Model
The population regression model is

$$
y_i = \beta_0 + \beta_1 x_i + \varepsilon_i
$$

where:
- \(y_i\) is the response variable  
- \(x_i\) is the predictor variable  
- \(\beta_0\) is the population intercept  
- \(\beta_1\) is the population slope  
- \(\varepsilon_i\) is the random error term  

---

### Estimated Regression Model
Using sample data, the estimated regression model is

$$
\hat{y}_i = b_0 + b_1 x_i
$$

where:
- \(b_0\) and \(b_1\) are least-squares estimates of \(\beta_0\) and \(\beta_1\)
- The estimates are obtained by minimizing the sum of squared errors

---

## 2. Residuals and Error

### Residual Definition
Residuals are defined as

$$
e_i = y_i - \hat{y}_i
$$

- Residuals measure the difference between observed and predicted values
- Residuals are observable
- True errors \(\varepsilon_i\) are unobservable
- Residuals are used to assess model assumptions and fit

---

## 3. Variability and Sums of Squares

### Total Sum of Squares (SST)
Measures total variability in the response:

$$
\text{SST} = \sum_{i=1}^{n} (y_i - \bar{y})^2
$$

---

### Regression Sum of Squares (SSR)
Measures variability explained by the model:

$$
\text{SSR} = \sum_{i=1}^{n} (\hat{y}_i - \bar{y})^2
$$

---

### Sum of Squared Errors (SSE)
Measures unexplained variability:

$$
\text{SSE} = \sum_{i=1}^{n} (y_i - \hat{y}_i)^2
$$

---

### Decomposition of Variability
The total variability decomposes as

$$
\text{SST} = \text{SSR} + \text{SSE}
$$

---

## 4. Coefficient of Determination (R²)

The coefficient of determination is

$$
R^2 = 1 - \frac{\text{SSE}}{\text{SST}}
$$

### Interpretation
- \(R^2\) represents the proportion of total variation explained by the model
- \(R^2\) does not imply causation
- A high \(R^2\) does not guarantee good prediction
- Adjusted \(R^2\) accounts for the number of predictors

---

## 5. Statistical Inference for Regression Coefficients

### Standard Error (SE)
The standard error measures the variability of coefficient estimates across repeated samples.

- Smaller SE indicates more precise estimation
- Larger SE indicates more uncertainty

---

### t-statistic
The t-statistic for a coefficient is

$$
t = \frac{b_j}{SE(b_j)}
$$

This tests the null hypothesis

$$
H_0: \beta_j = 0
$$

- Large absolute values of \(t\) indicate strong evidence against \(H_0\)
- Small absolute values indicate weak evidence

---

### p-value
The p-value is the probability of observing a t-statistic as extreme as the one obtained, assuming the null hypothesis is true.

- Small p-value → strong evidence against \(H_0\)
- Large p-value → insufficient evidence against \(H_0\)

---

### Confidence Interval for a Coefficient
A \(100(1-\alpha)\%\) confidence interval for \(\beta_j\) is

$$
b_j \pm t_{\alpha/2,\,n-2} \cdot SE(b_j)
$$

- If zero is not in the interval, the coefficient is statistically significant
- Confidence intervals and p-values provide equivalent conclusions

---

## 6. Diagnostic Checks and Model Assumptions

Linear regression assumes:
- Linearity
- Independence of errors
- Constant variance (homoscedasticity)
- Normally distributed errors (for inference)

Residual plots are used to assess these assumptions and identify:
- Outliers
- High-leverage points
- Influential observations (e.g., Cook’s Distance)

---

## 7. Multiple Linear Regression

The multiple linear regression model is

$$
\hat{y} = b_0 + b_1 x_1 + b_2 x_2 + \cdots + b_p x_p
$$

- Each coefficient represents the effect of a predictor while holding others constant
- Multicollinearity can inflate standard errors
- Overall model significance is tested using the F-statistic

---

## Key Takeaways
- Linear regression combines descriptive and inferential statistics
- Inference relies on sampling variability and model assumptions
- p-values and confidence intervals quantify uncertainty
- Diagnostic checks are essential for valid conclusions
