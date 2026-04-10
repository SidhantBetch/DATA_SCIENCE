# 📊 Feature Selection Techniques (Detailed Guide)

## 📌 What is Feature Selection?

Feature Selection is the process of selecting the most important features (independent variables) from a dataset to improve model performance, reduce overfitting, and decrease computation time.

---

## 🎯 Why Feature Selection is Important

* Improves model accuracy
* Reduces overfitting
* Faster training time
* Enhances model interpretability

---

## 🔑 Types of Feature Selection Techniques

### 1. Filter Methods

* Based on statistical measures
* Independent of machine learning models

**Examples:**

* Correlation
* Chi-Square Test
* ANOVA
* Variance Threshold

---

### 2. Wrapper Methods

* Uses machine learning models to evaluate features
* Computationally expensive but more accurate

**Examples:**

* Forward Selection (Forward Elimination)
* Backward Elimination
* Recursive Feature Elimination (RFE)

---

### 3. Embedded Methods

* Feature selection happens during model training

**Examples:**

* Lasso Regression (L1 Regularization)
* Ridge Regression (L2 Regularization)
* Decision Tree Feature Importance

---

# 🔄 Forward Selection (Forward Elimination)

## 📌 Definition

Forward Selection starts with **no features** and adds one feature at a time based on model performance.

---

## ⚙️ Steps:

1. Start with an empty model (no features)
2. Add each feature one by one
3. Select the feature that improves the model the most
4. Repeat until required number of features is reached

---

## 📊 Example (Code)

```python
from mlxtend.feature_selection import SequentialFeatureSelector
from sklearn.linear_model import LinearRegression

model = LinearRegression()

sfs = SequentialFeatureSelector(
    model,
    k_features=5,
    forward=True,
    scoring='r2',
    cv=5
)

sfs.fit(X, y)

print(sfs.k_feature_names_)
```

---

## ✅ Advantages:

* Simple to understand
* Works well with small datasets

## ❌ Disadvantages:

* Computationally expensive
* May miss best combination of features

---

# 🔙 Backward Elimination

## 📌 Definition

Backward Elimination starts with **all features** and removes the least important feature step by step.

---

## ⚙️ Steps:

1. Start with all features
2. Train the model
3. Remove the least significant feature (based on p-value or importance)
4. Repeat until only significant features remain

---

## 📊 Example (Code using statsmodels)

```python
import statsmodels.api as sm

X = sm.add_constant(X)

model = sm.OLS(y, X).fit()

while True:
    p_values = model.pvalues
    max_p = p_values.max()
    
    if max_p > 0.05:
        feature_to_remove = p_values.idxmax()
        X = X.drop(columns=[feature_to_remove])
        model = sm.OLS(y, X).fit()
    else:
        break

print(model.summary())
```

---

## ✅ Advantages:

* Considers all features initially
* More accurate than forward selection

## ❌ Disadvantages:

* Very slow for large datasets
* Requires high computation power

---

# ⚖️ Forward vs Backward Selection

| Feature     | Forward Selection | Backward Elimination |
| ----------- | ----------------- | -------------------- |
| Start Point | No features       | All features         |
| Process     | Add features      | Remove features      |
| Speed       | Faster            | Slower               |
| Accuracy    | Moderate          | Higher               |

---

