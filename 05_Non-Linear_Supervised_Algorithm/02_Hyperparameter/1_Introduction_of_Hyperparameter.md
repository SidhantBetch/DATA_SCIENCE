# 📌 Hyperparameters, Model, and Parameters in Machine Learning

In Machine Learning, understanding the difference between **Model**, **Parameters**, and **Hyperparameters** is very important for building accurate systems.

---

## 🤖 What is a Model?

A **model** is a mathematical representation or function that learns patterns from data and makes predictions.

### Examples:

* Linear Regression
* Decision Tree
* KNN
* SVM

### General Form:

$$
y = f(x)
$$

Where:

* ( x ) = Input features
* ( y ) = Output prediction

---

## ⚙️ What are Parameters?

**Parameters** are internal variables of a model that are **learned from data during training**.

### Examples:

* Weights in Linear Regression
* Splits in Decision Tree
* Support vectors in SVM

### Example (Linear Regression):

$$
y = mx + b
$$

* ( m ) = slope (parameter)
* ( b ) = intercept (parameter)

---

## 🎛️ What are Hyperparameters?

**Hyperparameters** are settings that are **set before training** and control how the model learns.

They are **not learned from data**.

---

## 🔍 Examples of Hyperparameters

| Algorithm     | Hyperparameters              |
| ------------- | ---------------------------- |
| KNN           | K (number of neighbors)      |
| Decision Tree | max_depth, min_samples_split |
| SVM           | C, kernel, gamma             |
| Random Forest | n_estimators, max_features   |

---

## 🔄 Parameters vs Hyperparameters

| Feature           | Parameters            | Hyperparameters          |
| ----------------- | --------------------- | ------------------------ |
| Learned from data | Yes                   | No                       |
| Set manually      | No                    | Yes                      |
| Role              | Define model behavior | Control training process |

---

## 🎯 What is Hyperparameter Tuning?

Hyperparameter tuning is the process of finding the **best combination of hyperparameters** to improve model performance.

---

## 🧠 Why Tuning is Important

* Improves model accuracy
* Reduces overfitting/underfitting
* Optimizes performance

---

## 🔧 Methods of Hyperparameter Tuning

### 1. Grid Search

* Tries **all possible combinations**
* Exhaustive but slow

---

### 2. Random Search

* Tries **random combinations**
* Faster than grid search

---

### 3. Bayesian Optimization

* Uses probability to find best parameters
* More efficient for large spaces

---

### 4. Automated Methods

* AutoML tools
* Libraries like Optuna, Hyperopt

---

## 🛠️ Python Implementation (Scikit-learn)

### Grid Search Example

```python id="grid123"
from sklearn.model_selection import GridSearchCV
from sklearn.svm import SVC

# Model
model = SVC()

# Hyperparameter grid
param_grid = {
    'C': [0.1, 1, 10],
    'kernel': ['linear', 'rbf'],
    'gamma': [0.1, 1]
}

# Grid Search
grid = GridSearchCV(model, param_grid, cv=5)
grid.fit(X_train, y_train)

# Best parameters
print("Best Parameters:", grid.best_params_)
```

---

### Random Search Example

```python id="random123"
from sklearn.model_selection import RandomizedSearchCV

random = RandomizedSearchCV(model, param_grid, cv=5, n_iter=5)
random.fit(X_train, y_train)

print("Best Parameters:", random.best_params_)
```

---
