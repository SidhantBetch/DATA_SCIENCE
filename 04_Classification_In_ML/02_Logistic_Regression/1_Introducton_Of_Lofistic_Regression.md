# 🔥 Logistic Regression in Machine Learning

---

## 📌 What is Logistic Regression?

Logistic Regression is a **supervised machine learning algorithm** used for **classification problems**, especially when the output is:

- Binary (0 or 1)  
- Yes / No  
- True / False  

👉 Example:
- Email → Spam or Not Spam  
- Loan → Approved or Rejected  

---

## 🧠 Why Not Linear Regression?

- Linear regression outputs values from **(-∞ to +∞)**  
- But classification needs **probabilities (0 to 1)**  

👉 Solution: Use **Sigmoid Function**

---

## 📊 Sigmoid Function
$$
σ(z) = 1 / (1 + e^(-z))
$$

👉 Converts any value into range **(0,1)**  

---

## 🔍 Hypothesis Function
$$
z = b0 + b1x1 + b2x2 + ... + bnxn
ŷ = σ(z)
$$

👉 Used instead of MSE  

---

## ⚙️ Algorithm Steps

1. Initialize weights  
2. Apply sigmoid function  
3. Calculate cost  
4. Update weights using Gradient Descent  
5. Repeat until convergence  

---

## ⚡ Implementation in Python

---

### 📦 Import Libraries

```python
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression
```

---

### 🔢 Step 1: Prepare Data
```python
X = dataset.drop("Target", axis=1)
y = dataset["Target"]
```
### 🔢 Step 2: Train-Test Split
```python
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)
```
### 🔢 Step 3: Train Model
```python
model = LogisticRegression()
model.fit(X_train, y_train)
```
### 🔢 Step 4: Prediction
```python
y_pred = model.predict(X_test)
```
---

## 📊 Evaluation Metrics
### ✔ Accuracy
```python
from sklearn.metrics import accuracy_score
accuracy_score(y_test, y_pred)
```
### ✔ Confusion Matrix
```python
from sklearn.metrics import confusion_matrix
confusion_matrix(y_test, y_pred)
```
### ✔ Precision, Recall, F1 Score
```python
from sklearn.metrics import classification_report
print(classification_report(y_test, y_pred))
```

---

# 📊 Types of Logistic Regression

## 🔹 1️⃣ Binary Logistic Regression

### 📌 Definition:
Binary Logistic Regression is used when the **target variable has only two classes**.

---

### 🎯 Output:
- 0 or 1  
- Yes / No  
- True / False  

---

### 🧠 Example:
- Spam vs Not Spam  
- Pass vs Fail  
- Loan Approved vs Rejected  

---

### ⚙️ Key Point:
👉 Uses **Sigmoid Function** to convert output into probability (0 to 1)

---

---

## 🔹 2️⃣ Multinomial Logistic Regression

### 📌 Definition:
Multinomial Logistic Regression is used when the **target variable has more than two classes** and **no natural order** exists.

---

### 🎯 Output:
- Multiple categories (unordered)

---

### 🧠 Example:
- Color: Red, Blue, Green  
- Product Category: Electronics, Clothing, Grocery  

---

### ⚙️ Key Point:
👉 Uses **Softmax Function** instead of sigmoid

---

---

## 🔹 3️⃣ Ordinal Logistic Regression

### 📌 Definition:
Ordinal Logistic Regression is used when the **target variable has multiple classes with a meaningful order**.

---

### 🎯 Output:
- Ordered categories  

---

### 🧠 Example:
- Ratings: Poor < Average < Good < Excellent  
- Education Level: High School < Graduate < Postgraduate  

---

### ⚙️ Key Point:
👉 Takes into account the **order
