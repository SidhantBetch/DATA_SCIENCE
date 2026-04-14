# 🔥 Simple Linear Regression in Machine Learning

---

## 📌 What is Simple Linear Regression?

Simple Linear Regression is a statistical method used to **predict a continuous value** using **one independent variable**.

👉 It finds a **linear relationship** between:
- Input (X) → Independent Variable  
- Output (Y) → Dependent Variable  

---

## 🧠 Example

- Predict **salary** based on **years of experience**  
- Predict **sales** based on **advertising budget**  

---

## 📊 Mathematical Equation
$$
y = mx + c
$$


Where:
- **y** → Predicted value  
- **x** → Input variable  
- **m** → Slope (coefficient)  
- **c** → Intercept  

---

## 🔍 Understanding the Equation

- **Slope (m):**  
  👉 Change in Y when X increases by 1  

- **Intercept (c):**  
  👉 Value of Y when X = 0  

---

## 📈 Graph Representation

- Straight line  
- X-axis → Independent variable  
- Y-axis → Dependent variable  

---

## ⚙️ Assumptions

- Linear relationship between X and Y  
- No outliers  
- Homoscedasticity (constant variance)  
- Normal distribution of errors  

---

## ⚡ Implementation in Python

### Import Libraries

```python
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
```

#### Step 1: Prepare Data
```python
X = dataset[["Experience"]]   # Independent variable
y = dataset["Salary"]         # Dependent variable
```
#### Step 2: Train-Test Split
```python
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)
```
#### Step 3: Train Model
```python
model = LinearRegression()
model.fit(X_train, y_train)
Step 4: Prediction
y_pred = model.predict(X_test)
```
#### Step 5: Visualization
```python
plt.scatter(X_train, y_train, color="blue")
plt.plot(X_train, model.predict(X_train), color="red")

plt.title("Simple Linear Regression")
plt.xlabel("Experience")
plt.ylabel("Salary")
plt.show()
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

👉 Measures model accuracy

0 → Poor
1 → Perfect
