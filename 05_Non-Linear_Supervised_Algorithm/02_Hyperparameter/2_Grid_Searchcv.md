## 🔍 GridSearchCV

### 📖 Definition

**GridSearchCV** is a hyperparameter tuning technique in machine learning that performs an **exhaustive search over a specified parameter grid** to find the best combination of hyperparameters for a model.

It uses **cross-validation (CV)** to evaluate each combination and selects the one that gives the best performance.

---

### 🧠 Key Idea

* Define a set of hyperparameters and their possible values
* Try **all possible combinations**
* Evaluate each using **cross-validation**
* Select the best-performing combination

---

### ⚙️ Syntax (Scikit-learn)

```python id="grid_def"
from sklearn.model_selection import GridSearchCV

grid = GridSearchCV(
    estimator=model,
    param_grid=param_grid,
    cv=5,
    scoring='accuracy'
)
```

---

### 📌 Important Parameters

* **estimator** → The machine learning model
* **param_grid** → Dictionary of hyperparameters
* **cv** → Number of cross-validation folds
* **scoring** → Evaluation metric

---

### 📊 Output

After fitting:

* `grid.best_params_` → Best hyperparameters
* `grid.best_score_` → Best score
* `grid.best_estimator_` → Best model

---

### ⚖️ Pros & Cons

**Advantages:**

* Finds optimal parameters
* Improves model performance

**Disadvantages:**

* Computationally expensive
* Slow for large parameter spaces

---
