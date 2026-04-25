# 🧠 Classification Tree Analysis – Breast Cancer Dataset

## 📌 Project Overview

This project applies a **Classification Tree model** to the Breast Cancer dataset to classify tumors as **malignant** or **benign**.

The analysis includes:

* Model training and visualization
* Interpretation of how the tree partitions the predictor space
* Overfitting analysis
* Cost-complexity pruning
* Cross-validation for model selection

The goal is to understand how decision trees work and how to optimize them for better generalization.

---

## 📂 Dataset

The dataset used is the **Breast Cancer dataset**, which is built into `scikit-learn`.

* Number of features: 30
* Target variable:

  * `0` → malignant
  * `1` → benign

No external download is required.

---

## ⚙️ Technologies Used

* Python
* Jupyter Notebook
* scikit-learn
* pandas
* numpy
* matplotlib

---

## 🚀 Methodology

### 1. Data Preparation

* Loaded dataset using `sklearn.datasets`
* Converted data into pandas DataFrame
* Split into training and testing sets (80/20)

### 2. Model Training

* Trained a **Decision Tree Classifier**
* Visualized the tree structure

### 3. Interpretation

* Identified key splitting variables (e.g., *mean concave points*)
* Explained how the model partitions the feature space into regions
* Interpreted predictions within each region

### 4. Overfitting Analysis

* Compared training and test accuracy
* Observed **mild overfitting**
* Evaluated misclassification error

### 5. Cost-Complexity Pruning

* Generated multiple trees using different `ccp_alpha` values
* Compared training and test errors
* Selected the optimal pruning level

### 6. Cross-Validation

* Performed **5-fold cross-validation**
* Plotted error vs number of terminal nodes
* Identified optimal tree size

---

## 📊 Results

* **Training Accuracy:** ~97.8%
* **Test Accuracy:** ~94.7%
* **Optimal Tree Depth:** 4
* **Optimal Terminal Nodes:** ~7
* **Best ccp_alpha:** ~0.0043

### 🔍 Key Insights

* The model shows **mild overfitting**, but generalizes well
* Important features include:

  * mean concave points
  * worst radius
  * texture
* A **pruned tree** provides the best balance between complexity and performance

---

## ⚖️ Bias-Variance Trade-off

* Fully grown tree → **low bias, high variance (overfitting)**
* Pruned tree → **slightly higher bias, lower variance**
* Optimal model achieves a good balance between both

---

## 📂 Files in This Repository

- `classification_tree_analysis.Rmd` → Main analysis file   
- `README.md` → Project documentation  


---

## ✅ Conclusion

This project demonstrates that:

* Decision trees are **interpretable and effective** for classification
* Overfitting can be controlled using **pruning techniques**
* Cross-validation helps identify the **optimal model complexity**

---

## 👩‍💻 Author

Peace Ebika  
PhD Student – Artificial Intelligence / Machine Learning Engr 
Case Western Reserve University / UDLAP

---
