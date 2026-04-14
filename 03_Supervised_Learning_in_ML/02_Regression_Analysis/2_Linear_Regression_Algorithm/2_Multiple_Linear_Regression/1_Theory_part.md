# 🔥 Multiple Linear Regression in Machine Learning

---

## 📌 What is Multiple Linear Regression?

Multiple Linear Regression (MLR) is a technique used to **predict a continuous value** using **two or more independent variables (features)**.

👉 It extends Simple Linear Regression by including multiple inputs.

---

## 🧠 Example

- Predict **House Price** based on:
  - Area  
  - Number of rooms  
  - Location  

- Predict **Sales** based on:
  - Advertising budget  
  - Price  
  - Season  

---

## 📊 Mathematical Equation
$$
y = b0 + b1x1 + b2x2 + b3x3 + ... + bnxn
$$

Where:
- **y** → Dependent variable (target)  
- **x1, x2, ..., xn** → Independent variables (features)  
- **b0** → Intercept  
- **b1, b2, ..., bn** → Coefficients  

---

## 🔍 Understanding the Equation

- Each coefficient (**bi**) represents:
  👉 Change in **y** when **xi increases by 1**, keeping others constant  

---

## ⚙️ Assumptions of MLR

- Linear relationship between variables  
- No multicollinearity (features not highly correlated)  
- Homoscedasticity (constant variance)  
- Normal distribution of errors  
- No autocorrelation  

---

## ⚡ Algorithm Steps

1. Load dataset  
2. Separate features (X) and target (y)  
3. Perform Train-Test Split  
4. Train the model  
5. Make predictions  
6. Evaluate model  

---

## ⚙️ Implementation in Python

---

### 📦 Import Libraries

```python
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
```

#### 🔢 Step 1: Define Features & Target
```python
X = dataset.drop("Price", axis=1)
y = dataset["Price"]
```
#### 🔢 Step 2: Train-Test Split
```python
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)
```
#### 🔢 Step 3: Train Model
```python
model = LinearRegression()
model.fit(X_train, y_train)
```
#### 🔢 Step 4: Prediction
```python
y_pred = model.predict(X_test)
```
#### 🔢 Step 5: Check Coefficients
```python
print(model.coef_)
print(model.intercept_)
```

## 📊 Evaluation Metrics

### 1️⃣ Mean Absolute Error (MAE)
```python
MAE = |y - ŷ|
```
### 2️⃣ Mean Squared Error (MSE)
```python
MSE = (y - ŷ)²
```
### 3️⃣ Root Mean Squared Error (RMSE)
```python
RMSE = √MSE
```
### 4️⃣ R² Score
```python
R² = 1 - (SSR / SST)

```
