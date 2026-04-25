# Regression Tree Analysis - Insurance Dataset

## 📊 Project Overview
This project applies a **Regression Tree model** to analyze and predict medical insurance charges using the *Medical Cost Personal Insurance Dataset*.  

The goal is to:
- Understand how predictors influence insurance costs
- Detect overfitting in tree-based models
- Apply pruning techniques to improve performance
- Use cross-validation to select the optimal model

---

## 📁 Dataset
The dataset used is `insurance.csv`, which contains:

- **age** – Age of the individual  
- **sex** – Gender  
- **bmi** – Body Mass Index  
- **children** – Number of dependents  
- **smoker** – Smoking status  
- **region** – Residential region  
- **charges** – Medical insurance cost (**target variable**)  

---

## ⚙️ Methods Used

### 1. Regression Tree Modeling
- Built using `DecisionTreeRegressor`
- Initial model trained with limited depth
- Fully grown tree used to analyze overfitting

---

### 2. Tree Visualization
- Visualized using `plot_tree`
- Identified key splits:
  - Smoking status (most important)
  - Age
  - BMI

---

### 3. Overfitting Analysis
- Compared:
  - Training Mean Squared Error (MSE)
  - Test Mean Squared Error (MSE)

✔ Result:  
The full tree showed **clear overfitting** (low training error, high test error)

---

### 4. Cost-Complexity Pruning
- Generated multiple trees using `ccp_alpha`
- Evaluated model performance across different complexity levels
- Selected best alpha using test error

---

### 5. Cross-Validation
- Applied **5-fold cross-validation**
- Evaluated error vs number of terminal nodes
- Identified optimal model size

---

## 📈 Key Results

- ✅ Optimal number of terminal nodes: **13**
- ✅ Best cross-validation MSE: **≈ 23,304,297**
- ✅ Best model achieved after pruning

---

## 🧠 Interpretation

### ✔ Does pruning improve performance?
Yes.  
Pruning reduces overfitting by simplifying the model, leading to better generalization on unseen data.

---

### ✔ Bias-Variance Trade-off
- Full tree → Low bias, **high variance** (overfitting)
- Pruned tree → Slightly higher bias, **lower variance**

✔ Result: Better overall performance

---

### ✔ Predictor Importance
- Smoking status is the most influential variable
- Age and BMI further refine predictions
- Tree partitions the data into meaningful regions for prediction

---

## 📂 Files in This Repository

- `regression_tree_analysis.Rmd` → Main analysis file  
- `insurance.csv` → Dataset  
- `README.md` → Project documentation  

---

## 🚀 How to Run

1. Open the `.Rmd` file in **RStudio**
2. Ensure `reticulate` is installed:
   ```r
   install.packages("reticulate")
