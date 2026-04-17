# 📌 What is an Imbalanced Dataset?
An **Imbalanced Dataset** is a dataset where the **classes are not equally distributed**.  
👉 One class (majority) has significantly more samples than the other class (minority).

---

## 📊 Example

| Class | Count |
|------|------|
| 0 (Not Fraud) | 950 |
| 1 (Fraud) | 50 |

👉 This is highly imbalanced ❌

---

## 🧠 Why is it a Problem?

- Model becomes **biased toward majority class**  
- High accuracy but poor real performance  
- Fails to detect minority class  

---

## ⚠️ Example Problem

👉 Model predicts all samples as "Not Fraud":

- Accuracy = 95% ✅  
- But detects **0 fraud cases** ❌  

---

## 📉 Impact on Metrics

| Metric | Behavior |
|--------|---------|
| Accuracy | Misleading ❌ |
| Precision | Useful ✔ |
| Recall | Very important ✔ |
| F1 Score | Balanced metric ✔ |

---

## 📊 Types of Imbalance

---

### 🔹 Mild Imbalance
- Ratio ~ 60:40  

---

### 🔹 Moderate Imbalance
- Ratio ~ 80:20  

---

### 🔹 Severe Imbalance
- Ratio ~ 95:5 or worse  

---

# 🔧 Techniques to Handle Imbalanced Data


## 🔹 1️⃣ Random Under Sampling

---

### 📌 Definition

Random Under Sampling reduces the size of the **majority class** by randomly removing samples.


#### 📊 Example

| Before | After |
|-------|------|
| Majority = 950 | 50 |
| Minority = 50 | 50 |


#### 🧠 How It Works

- Randomly remove data points from majority class  
- Match size with minority class  


#### ✔ Advantages

- Reduces dataset size  
- Faster training  
- Simple to implement  

#### ❌ Disadvantages
- Loss of important information  
- Risk of underfitting  


#### ⚙️ Python Example

```python
from imblearn.under_sampling import RandomUnderSampler

rus = RandomUnderSampler()
X_res, y_res = rus.fit_resample(X, y)
```

---

## 🔹 2️⃣ Random Over Sampling

---

### 📌 Definition
Random Over Sampling increases the size of the minority class by duplicating samples.

#### 📊 Example

Before	| After
--------|--------
Majority = 950 |	950
Minority = 50	| 950

#### 🧠 How It Works
- Randomly duplicate minority class samples
- Match size with majority class

#### ✔ Advantages
- No loss of data
- Better for small datasets

#### ❌ Disadvantages
- Overfitting risk
- Duplicate data reduces diversity


#### ⚙️ Python Example
```python
from imblearn.over_sampling import RandomOverSampler

ros = RandomOverSampler()
X_res, y_res = ros.fit_resample(X, y)
```
