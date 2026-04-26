# 📌 Loss Functions in Machine Learning

A **Loss Function** measures how well a machine learning model’s predictions match the actual values.

👉 It quantifies the **error** between predicted output and true output.

---

## 🔍 Types of Loss Functions

Loss functions depend on the type of problem:

* **Regression Problems**
* **Classification Problems**

---

## 📊 1. Regression Loss Functions

---

### 🔹 Mean Squared Error (MSE)

$$
MSE = \frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2
$$

### 📖 Explanation

* Squares the error
* Penalizes large errors more

---

### 🔹 Mean Absolute Error (MAE)

$$
MAE = \frac{1}{n} \sum_{i=1}^{n} |y_i - \hat{y}_i|
$$

### 📖 Explanation

* Absolute difference
* Less sensitive to outliers

---

### 🔹 Root Mean Squared Error (RMSE)

$$
RMSE = \sqrt{\frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2}
$$

---

### 🔹 Huber Loss 

$$
\
Huber =
\begin{cases}
\frac{1}{2}(y - \hat{y})^2 & \text{if } |y - \hat{y}| \le \delta \\\\
\delta \left(|y - \hat{y}| - \frac{1}{2}\delta \right) & \text{if } |y - \hat{y}| > \delta
\end{cases}
\
$$


---

## 📊 2. Classification Loss Functions

---

### 🔹 Binary Cross-Entropy (Log Loss)

$$
L = -\frac{1}{n} \sum [y \log(\hat{y}) + (1-y) \log(1-\hat{y})]
$$

### 📖 Use

* Binary classification problems

---

### 🔹 Categorical Cross-Entropy

$$
L = -\sum y_i \log(\hat{y}_i)
$$

### 📖 Use

* Multi-class classification

---

### 🔹 Hinge Loss

$$
L = \max(0, 1 - y \cdot \hat{y})
$$

### 📖 Use

* Support Vector Machines (SVM)

---

## 🔍 Loss vs Cost Function

| Term          | Meaning                       |
| ------------- | ----------------------------- |
| Loss Function | Error for a single data point |
| Cost Function | Average loss over dataset     |

---

## ⚙️ Properties of Good Loss Function

* Differentiable
* Convex (ideally)
* Easy to optimize

---

## ⚖️ Choosing Loss Function

| Problem Type | Recommended Loss          |
| ------------ | ------------------------- |
| Regression   | MSE, MAE                  |
| Binary Class | Binary Cross-Entropy      |
| Multi-Class  | Categorical Cross-Entropy |

---

## 🛠️ Python Example (Scikit-learn)

```python id="loss1"
from sklearn.metrics import mean_squared_error, mean_absolute_error

y_true = [3, -0.5, 2]
y_pred = [2.5, 0.0, 2]

print("MSE:", mean_squared_error(y_true, y_pred))
print("MAE:", mean_absolute_error(y_true, y_pred))
```

---

## 🧪 Applications

* Model training
* Optimization
* Deep learning
* Performance evaluation

---
