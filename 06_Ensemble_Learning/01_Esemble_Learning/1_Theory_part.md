# 📌 Ensemble Learning

Ensemble Learning is a machine learning technique where **multiple models (learners)** are combined to improve overall performance.

👉 Instead of relying on a single model, it uses a **group of models** to make better predictions.

---

## 🔍 Types of Ensemble Learning

### 1. Bagging (Bootstrap Aggregating)

* Models are trained independently
* Uses **random sampling with replacement**
* Final output = average (regression) or majority vote (classification)

#### Example:

* Random Forest

---

### 2. Boosting

* Models are trained sequentially
* Each new model focuses on previous errors
* Improves performance step by step

#### Examples:

* AdaBoost
* Gradient Boosting
* XGBoost

---

### 3. Stacking

* Combines predictions of multiple models
* Uses a **meta-model** to make final prediction

---

## ⚙️ How Ensemble Works

1. Train multiple models
2. Combine predictions
3. Produce final output

---

## 📊 Example

Instead of using one model:

* Model 1 → Prediction A
* Model 2 → Prediction B
* Model 3 → Prediction A

👉 Final Output (majority voting) → **A**

---

## ⚖️ Advantages

* Higher accuracy
* Reduces overfitting
* More stable predictions
* Handles complex data well

---

## ⚠️ Disadvantages

* Computationally expensive
* Harder to interpret
* Requires more memory

---

## 🧪 Applications

* Fraud detection
* Recommendation systems
* Image recognition
* Kaggle competitions

---

## 🛠️ Python Examples (Scikit-learn)

### Bagging Example

```python id="ens1"
from sklearn.ensemble import BaggingClassifier
from sklearn.tree import DecisionTreeClassifier

model = BaggingClassifier(
    base_estimator=DecisionTreeClassifier(),
    n_estimators=10
)

model.fit(X_train, y_train)
```

---

### Random Forest Example

```python id="ens2"
from sklearn.ensemble import RandomForestClassifier

rf = RandomForestClassifier(n_estimators=100)
rf.fit(X_train, y_train)
```

---

### Boosting Example (AdaBoost)

```python id="ens3"
from sklearn.ensemble import AdaBoostClassifier

adb = AdaBoostClassifier(n_estimators=50)
adb.fit(X_train, y_train)
```

---

## 🔍 Comparison

| Method   | Training Style | Goal              |
| -------- | -------------- | ----------------- |
| Bagging  | Parallel       | Reduce variance   |
| Boosting | Sequential     | Reduce bias       |
| Stacking | Hybrid         | Combine strengths |

---
