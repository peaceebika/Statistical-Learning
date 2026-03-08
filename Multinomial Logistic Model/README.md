---
title: "Multinomial Logistic Regression: Wine Classification"
author: "Peace Ebika"
output: github_document
---

# Multinomial Logistic Regression: Wine Classification

## Project Overview

This project demonstrates the implementation of a **Multinomial Logistic Regression model** to classify different types of wine using their chemical properties. The goal of this analysis is to build a classification model capable of predicting the wine class based on various chemical attributes.

Multinomial logistic regression is appropriate for this task because the response variable contains **more than two categories**.

---

# Dataset Description

The dataset used in this project is the **Wine Dataset**, a well-known dataset used for classification problems.

The dataset contains:

- **178 observations**
- **14 variables**

Among these variables:

- **13 predictor variables** represent chemical characteristics of wine samples
- **1 categorical target variable** called `class`

The predictor variables include measurements such as:

- Alcohol
- Malic acid
- Ash
- Magnesium
- Flavanoids
- Proanthocyanins
- Color intensity
- Hue
- Proline

The **target variable (`class`)** contains **three wine categories**:

- Class 1
- Class 2
- Class 3

All predictor variables are **continuous numerical variables**, while the class variable is **categorical**.

Source: **UCI Machine Learning Repository – Wine Dataset**

---

# Data Preprocessing

The following preprocessing steps were performed before training the model:

1. The dataset was loaded into Python using the **Pandas** library.
2. The structure of the dataset was inspected to verify the number of observations and variables.
3. Missing values were checked and none were found.
4. The dataset was separated into:
   - **Predictor variables (X)**
   - **Target variable (y)**
5. The data was split into training and testing datasets.

---

# Train-Test Split

The dataset was divided into training and testing sets using **Scikit-learn's `train_test_split()` function**.

- **75% of the data was used for training**
- **25% of the data was used for testing**

This allows the model to learn patterns from the training data and then evaluate its performance on unseen data.

---

# Model Implementation

A **Multinomial Logistic Regression model** was implemented using the **Scikit-learn library**.

The model configuration included:

- `solver = "lbfgs"`
- `multi_class = "multinomial"`

The model was trained using the training dataset so that it could learn the relationship between the wine's chemical attributes and the wine class.

---

# Model Analysis

The model estimates a set of coefficients for each class of wine.

Each coefficient represents the relationship between a predictor variable and the probability of belonging to a specific wine class.

- A **positive coefficient** increases the likelihood of that class.
- A **negative coefficient** decreases the likelihood of that class.

By examining the magnitude of the coefficients, we can identify which chemical variables have the strongest influence in distinguishing between the different wine classes.

---

# Model Validation

The model was evaluated using the testing dataset.

The following performance metrics were calculated:

- **Confusion Matrix**
- **Accuracy**
- **Precision**
- **Recall**
- **F1 Score**

### Accuracy

The model achieved an **accuracy of 1.00 (100%)**, meaning that all test samples were correctly classified.

### Confusion Matrix

The confusion matrix showed that:

- 15 samples of Class 1 were correctly predicted
- 18 samples of Class 2 were correctly predicted
- 12 samples of Class 3 were correctly predicted

No misclassifications occurred.

### Precision, Recall, and F1 Score

All classes achieved:

- **Precision = 1.00**
- **Recall = 1.00**
- **F1 Score = 1.00**

This indicates perfect classification performance on the test dataset.

---

# Conclusion

The multinomial logistic regression model performed exceptionally well on the wine dataset.

The chemical attributes of the wine samples provide strong predictive power for distinguishing between the different wine classes.

This project demonstrates how multinomial logistic regression can be applied to **multi-class classification problems** and how model performance can be evaluated using standard metrics such as confusion matrix, accuracy, precision, recall, and F1 score.

---

# Technologies Used

- Python
- Google Colab
- Pandas
- Scikit-learn
- NumPy

---

# Repository Structure

