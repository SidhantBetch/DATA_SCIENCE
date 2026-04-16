# 🔥 Cost Function in Machine Learning (Detailed)

---

## 📌 What is a Cost Function?

A **Cost Function** (also called **Loss Function**) is a mathematical function used to **measure the error** between:

- Actual value (y)  
- Predicted value (ŷ)  

👉 It helps evaluate how well a machine learning model is performing.

---

## 🧠 Why is Cost Function Important?

- Guides model training  
- Helps in optimization  
- Used in algorithms like Gradient Descent  
- Lower cost = better predictions  

---

## 🎯 Objective

👉 Minimize the cost function to improve model accuracy

---

## 🔁 Cost Function vs Loss Function

| Term | Meaning |
|------|--------|
| Loss Function | Error for a single data point |
| Cost Function | Average error over the dataset |

---

# 📊 Types of Cost Functions

---

# 🔹 1️⃣ Regression Cost Functions

Used when output is **continuous (numeric values)**

---

## ✔ Mean Absolute Error (MAE)

$$
MAE = (1/n) * Σ |y - ŷ|
$$

### 📌 Explanation:
- Measures average absolute difference  

### ✔ Advantages:
- Less sensitive to outliers  

### ❌ Disadvantages:
- Not differentiable at zero  

---

## ✔ Mean Squared Error (MSE)

$$
MSE = (1/n) * Σ (y - ŷ)²
$$

### 📌 Explanation:
- Squares the error  

### ✔ Advantages:
- Penalizes large errors more  
- Smooth for optimization  

### ❌ Disadvantages:
- Sensitive to outliers  

---

## ✔ Root Mean Squared Error (RMSE)

$$
RMSE = √MSE
$$

### 📌 Explanation:
- Square root of MSE  

### ✔ Advantages:
- Same unit as output  
- Easy interpretation  

---

---

# 🔹 2️⃣ Binary Classification Cost Function

Used when output is **0 or 1**

---

## ✔ Binary Cross Entropy (Log Loss)
$$
Loss = -[y log(ŷ) + (1 - y) log(1 - ŷ)]
$$

### 📌 Explanation:
- Measures difference between actual and predicted probability  

### ✔ Advantages:
- Works well with probability outputs  
- Used in Logistic Regression  

### ❌ Disadvantages:
- Computationally expensive  

---

## 🔍 Example:

| Actual (y) | Predicted (ŷ) | Loss |
|-----------|--------------|------|
| 1 | 0.9 | Low |
| 1 | 0.1 | High |

---

---

# 🔹 3️⃣ Multi-Class Classification Cost Function

Used when output has **more than two classes**

---

## ✔ Categorical Cross Entropy
$$
Loss = - Σ yᵢ log(ŷᵢ)
$$

### 📌 Explanation:
- Compares predicted probability distribution with actual class  

---

## 🔍 Example:

| Class | Actual | Predicted |
|------|--------|-----------|
| A | 1 | 0.8 |
| B | 0 | 0.1 |
| C | 0 | 0.1 |

👉 Loss will be low if correct class has high probability  

---

## ✔ Sparse Categorical Cross Entropy

👉 Used when labels are integers instead of one-hot encoded  

---

# ⚙️ Summary Table

| Type | Cost Function | Use Case |
|------|--------------|----------|
| Regression | MAE, MSE, RMSE | Continuous output |
| Binary Classification | Binary Cross Entropy | 2 classes |
| Multi-Class | Categorical Cross Entropy | Multiple classes |

---

# ⚠️ Important Points

- Always choose cost function based on problem type  
- Cost function must be differentiable for optimization  
- Used with Gradient Descent  

---

# 🧠 Interview Questions

**Q1:** What is a cost function?  
👉 Measures error between actual and predicted values  

**Q2:** Which cost function is used in regression?  
👉 MAE, MSE, RMSE  

**Q3:** Which is used in classification?  
👉 Cross Entropy  

**Q4:** Why MSE is preferred over MAE?  
👉 Smooth and easier for optimization  

---

# 🧾 Summary

- Cost function measures model error  
- Goal is to minimize it  
- Different types for different problems:
  - Regression → MAE, MSE, RMSE  
  - Binary → Binary Cross Entropy  
  - Multi-class → Categorical Cross Entropy  

---
