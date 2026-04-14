# 🔥 Regression Analysis in Machine Learning

---

## 📌 What is Regression Analysis?

Regression Analysis is a statistical technique used to **predict a continuous numerical value** based on one or more independent variables (features).

👉 Example:
- Predict **House Price**
- Predict **Sales Amount**
- Predict **Salary**

---

## 🧠 Why Use Regression?

- To understand relationships between variables  
- To make predictions  
- To identify important factors affecting output  

---

## 🔑 Key Terms

| Term | Meaning |
|------|--------|
| Dependent Variable (y) | Target/output (e.g., price) |
| Independent Variable (X) | Input/features |
| Coefficient | Impact of feature on output |
| Intercept | Value when X = 0 |

---

## 📊 Types of Regression

---

### 1️⃣ Simple Linear Regression

👉 One independent variable

### Equation:
$$
y = mx + c
$$

- m → slope  
- c → intercept  

---

### 2️⃣ Multiple Linear Regression

👉 More than one independent variable

### Equation:
$$
y = b_0 + b_1x_1 + b_2x_2 + ... + b_nx_n
$$

---

### 3️⃣ Polynomial Regression

👉 Captures non-linear relationships

$$
y = b_0 + b_1x + b_2x^2 + ... + b_nx^n
$$

---

### 4️⃣ Ridge Regression

👉 Adds penalty to reduce overfitting

---

### 5️⃣ Lasso Regression

👉 Performs feature selection (shrinks coefficients to zero)

---

### 6️⃣ ElasticNet Regression

👉 Combination of Ridge and Lasso

---

## ⚙️ Assumptions of Linear Regression

- Linear relationship between variables  
- No multicollinearity  
- Homoscedasticity (constant variance)  
- Normal distribution of errors  
- No autocorrelation  

---

## ⚡ Implementation in Python

Using **scikit-learn**

```python
from sklearn.linear_model import LinearRegression
from sklearn.model_selection import train_test_split
```

## Example

```python
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression

# Features & target
X = dataset.drop("Price", axis=1)
y = dataset["Price"]

# Split data
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2)

# Model
model = LinearRegression()
model.fit(X_train, y_train)

# Prediction
y_pred = model.predict(X_test)
```

