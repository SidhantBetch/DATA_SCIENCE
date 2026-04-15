# 🔥 Polynomial Regression in Machine Learning

---

## 📌 What is Polynomial Regression?

Polynomial Regression is a type of regression where the relationship between the **independent variable (X)** and **dependent variable (y)** is **non-linear**, but it is modeled using a polynomial equation.

👉 It is an extension of Linear Regression.

---

## 🧠 Why Use Polynomial Regression?

- When data is **curved (non-linear)**  
- When linear regression gives poor results  
- To capture **complex patterns**  

---

## 📊 Mathematical Equation

$$
y = b_0 + b_1x + b_2x² + b_3x³ + ... + b_nxⁿ
$$

Where:
- **y** → Dependent variable  
- **x** → Independent variable  
- **b0, b1, ..., bn** → Coefficients  
- **n** → Degree of polynomial  

---

## 🔍 Example

👉 Predict salary based on experience:

- Linear: straight line ❌  
- Polynomial: curved line ✅  

---

## 📈 Graph Representation

- X-axis → Input variable  
- Y-axis → Output variable  
- Curve instead of straight line  

---

## ⚙️ How It Works

1. Convert input feature into polynomial features  
2. Apply Linear Regression on transformed data  

👉 Example: $x → [x, x², x³]$

---

## ⚡ Implementation in Python

---

### 📦 Import Libraries

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression
from sklearn.preprocessing import PolynomialFeatures
```


#### 🔢 Step 1: Prepare Data
```python
X = dataset[["Level"]]
y = dataset["Salary"]
```
#### 🔢 Step 2: Create Polynomial Features
```python
poly = PolynomialFeatures(degree=3)
X_poly = poly.fit_transform(X)
```
#### 🔢 Step 3: Train Model
```python
model = LinearRegression()
model.fit(X_poly, y)
```
#### 🔢 Step 4: Prediction
```python
y_pred = model.predict(X_poly)
```
#### 🔢 Step 5: Visualization
```python
plt.scatter(X, y, color="blue")
plt.plot(X, y_pred, color="red")

plt.title("Polynomial Regression")
plt.xlabel("Level")
plt.ylabel("Salary")

plt.show()
```
