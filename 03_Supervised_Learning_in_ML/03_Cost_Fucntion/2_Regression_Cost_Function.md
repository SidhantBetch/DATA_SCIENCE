# 🔥 Regression Cost Function in Machine Learning

---

## 📌 What is a Regression Cost Function?

A **Regression Cost Function** is used to measure the **error between actual values (y)** and **predicted values (ŷ)** when the output is **continuous (numeric)**.

👉 It tells us how far our model predictions are from the real values.

---

## 🧠 Why is it Important?

- Helps evaluate model performance  
- Guides optimization (Gradient Descent)  
- Helps in improving predictions  
- Lower cost = better model  

---

## 🎯 Objective

👉 Minimize the cost function to get the best model

---

## 🔍 Basic Idea
$$
Error = y - ŷ
$$


👉 Cost function aggregates this error over all data points

---

# 📊 Types of Regression Cost Functions

---

## 🔹 1️⃣ Mean Absolute Error (MAE)
$$
MAE = \frac{1}{n} Σ |y - ŷ|
$$

### 📌 Explanation:
- Takes absolute difference between actual and predicted values  

### ✔ Advantages:
- Easy to understand  
- Less sensitive to outliers  

### ❌ Disadvantages:
- Not differentiable at zero  
- Slower convergence  

---

## 🔹 2️⃣ Mean Squared Error (MSE)
$$
MSE = \frac{1}{n} Σ (y - ŷ)²
$$

### 📌 Explanation:
- Squares the error  

### ✔ Advantages:
- Penalizes large errors more  
- Smooth and differentiable  
- Widely used  

### ❌ Disadvantages:
- Sensitive to outliers  

---

## 🔹 3️⃣ Root Mean Squared Error (RMSE)
$$
RMSE = \sqrt{MSE}
$$

### 📌 Explanation:
- Square root of MSE  

### ✔ Advantages:
- Same unit as target variable  
- Easy to interpret  

### ❌ Disadvantages:
- Still affected by outliers  

---

## ⚙️ Comparison Table

| Cost Function | Outlier Sensitivity | Differentiable | Use Case |
|--------------|--------------------|---------------|----------|
| MAE | Low | No (at 0) | Robust models |
| MSE | High | Yes | Most common |
| RMSE | High | Yes | Interpretation |

---

## ⚠️ Important Points

- MSE is most commonly used in regression  
- MAE is better when outliers exist  
- RMSE gives error in same unit  
- Choose based on problem type  

---

## ⚡ Implementation in Python

```python
from sklearn.metrics import mean_absolute_error, mean_squared_error
import numpy as np

mae = mean_absolute_error(y_test, y_pred)
mse = mean_squared_error(y_test, y_pred)
rmse = np.sqrt(mse)

print("MAE:", mae)
print("MSE:", mse)
print("RMSE:", rmse)
```
