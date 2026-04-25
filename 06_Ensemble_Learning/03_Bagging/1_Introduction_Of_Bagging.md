# 📌 Bagging (Bootstrap Aggregating) in Machine Learning

Bagging (Bootstrap Aggregating) is an **ensemble learning technique** used to improve the stability and accuracy of machine learning models.

👉 It reduces **variance** and helps prevent **overfitting**.

---

## 🔄 How Bagging Works

1. Create multiple subsets of the dataset using **sampling with replacement** (bootstrap sampling)
2. Train a model on each subset
3. Make predictions using all models
4. Combine predictions:

   * **Classification** → Majority voting
   * **Regression** → Averaging

---

## 📊 Example

Original dataset:

* 100 samples

Create subsets:

* Dataset 1 → Random 100 samples (with replacement)
* Dataset 2 → Another random 100 samples
* Dataset 3 → Another random 100 samples

👉 Train separate models on each dataset

---

## 🔑 Key Concepts

### 1. Bootstrap Sampling

* Sampling with replacement
* Same data point can appear multiple times

---

### 2. Base Learner

* Model used in bagging (e.g., Decision Tree)

---

### 3. Aggregation

* Combining predictions from all models

---

## ⚙️ Advantages

* Reduces overfitting
* Improves model stability
* Works well with high-variance models (like Decision Trees)

---

## ⚠️ Disadvantages

* Increased computational cost
* Less interpretable
* Not effective for low-variance models

---

## 🌲 Bagging vs Random Forest

| Feature           | Bagging    | Random Forest             |
| ----------------- | ---------- | ------------------------- |
| Base model        | Any model  | Decision Trees            |
| Feature selection | Not random | Random subset of features |
| Performance       | Good       | Better (usually)          |

---

## 🛠️ Python Implementation (Scikit-learn)

```python id="bag1"
from sklearn.ensemble import BaggingClassifier
from sklearn.tree import DecisionTreeClassifier

# Model
model = BaggingClassifier(
    base_estimator=DecisionTreeClassifier(),
    n_estimators=10,
    random_state=42
)

# Train
model.fit(X_train, y_train)

# Predict
y_pred = model.predict(X_test)
```

---

## 📊 Regression Example

```python id="bag2"
from sklearn.ensemble import BaggingRegressor

model = BaggingRegressor(
    n_estimators=10,
    random_state=42
)

model.fit(X_train, y_train)
```

---

## 🧪 Applications

* Fraud detection
* Medical diagnosis
* Stock prediction
* Image classification

---
