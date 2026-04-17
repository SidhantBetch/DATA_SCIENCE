# 🔥 Confusion Matrix in Machine Learning

---

## 📌 What is a Confusion Matrix?

A **Confusion Matrix** is a table used to **evaluate the performance of a classification model**.

👉 It compares:
- **Actual values** (True labels)
- **Predicted values** (Model output)

---

## 🧠 Why is Confusion Matrix Important?

- Gives detailed performance analysis  
- Helps understand types of errors  
- Better than accuracy alone  
- Useful for imbalanced datasets  

---

## 📊 Structure of Confusion Matrix (Binary Classification)

|                | Predicted Positive | Predicted Negative |
|----------------|-------------------|-------------------|
| **Actual Positive** | True Positive (TP) | False Negative (FN) |
| **Actual Negative** | False Positive (FP) | True Negative (TN) |

---

## 🔍 Key Terms Explained

---

### ✔ True Positive (TP)
👉 Model correctly predicts **Positive class**

---

### ✔ True Negative (TN)
👉 Model correctly predicts **Negative class**

---

### ✔ False Positive (FP)
👉 Model incorrectly predicts Positive (Type I Error)

---

### ✔ False Negative (FN)
👉 Model incorrectly predicts Negative (Type II Error)

---

# 🔥 Confusion Matrix – Detailed Example

---

## 📌 Problem Statement

Suppose we are building a **Spam Detection Model**.

- Class 1 → Spam  
- Class 0 → Not Spam  

---

## 📊 Actual vs Predicted Data

| Email | Actual | Predicted |
|------|--------|-----------|
| 1 | Spam (1) | Spam (1) |
| 2 | Spam (1) | Not Spam (0) |
| 3 | Not Spam (0) | Spam (1) |
| 4 | Not Spam (0) | Not Spam (0) |
| 5 | Spam (1) | Spam (1) |
| 6 | Not Spam (0) | Not Spam (0) |
| 7 | Spam (1) | Spam (1) |
| 8 | Not Spam (0) | Spam (1) |

---

### ✔ True Positive (TP)
👉 Actual = Spam, Predicted = Spam  
Emails: 1, 5, 7  
👉 TP = 3  

---

### ✔ True Negative (TN)
👉 Actual = Not Spam, Predicted = Not Spam  
Emails: 4, 6  
👉 TN = 2  

---

### ✔ False Positive (FP)
👉 Actual = Not Spam, Predicted = Spam  
Emails: 3, 8  
👉 FP = 2  

---

### ✔ False Negative (FN)
👉 Actual = Spam, Predicted = Not Spam  
Email: 2  
👉 FN = 1  

---

## 📊 Confusion Matrix Table

|                | Predicted Spam | Predicted Not Spam |
|----------------|---------------|-------------------|
| Actual Spam     | TP = 3        | FN = 1            |
| Actual Not Spam | FP = 2        | TN = 2            |
