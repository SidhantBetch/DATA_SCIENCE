# 📌 Cross-Validation in Machine Learning

Cross-validation is a technique used to evaluate the performance of a machine learning model by testing it on different subsets of the dataset.

It helps ensure that the model performs well on **unseen data** and reduces **overfitting**.

---

## 🧠 Why Cross-Validation is Important

* Provides a more reliable estimate of model performance
* Uses all data for both training and testing
* Reduces overfitting
* Helps in model selection and hyperparameter tuning

---

## 🔍 Types of Cross-Validation

### 1. K-Fold CV

* Most common method

---

### 2. Stratified K-Fold

* Maintains class distribution
* Used in classification problems

---

### 3. Leave-One-Out (LOOCV)

* Each data point is used as test once
* Very accurate but slow

---

### 4. Shuffle Split

* Random splitting multiple times

---

## ⚙️ Python Implementation (Scikit-learn)

### Basic Cross-Validation

```python id="cv_basic"
from sklearn.model_selection import cross_val_score
from sklearn.tree import DecisionTreeClassifier

model = DecisionTreeClassifier()

scores = cross_val_score(model, X, y, cv=5)

print("Scores:", scores)
print("Average Score:", scores.mean())
```

---

## ⚖️ Advantages

* Better performance estimation
* Uses full dataset efficiently
* Reduces bias from single split

---

## ⚠️ Disadvantages

* Computationally expensive
* Slower for large datasets

---

## 🧪 Applications

* Model evaluation
* Hyperparameter tuning (GridSearchCV, RandomizedSearchCV)
* Model comparison

---
