## 🎲 RandomizedSearchCV

### 📖 Definition

**RandomizedSearchCV** is a hyperparameter tuning technique that **randomly samples combinations of hyperparameters** from a specified distribution to find the best model settings.

Unlike GridSearchCV, it does **not try all combinations**, making it faster and more efficient for large parameter spaces.

---

### 🧠 Key Idea

* Define hyperparameter distributions
* Randomly select a fixed number of combinations
* Evaluate each using **cross-validation**
* Choose the best-performing combination

---

### ⚙️ Syntax (Scikit-learn)

```python id="random_def"
from sklearn.model_selection import RandomizedSearchCV

random_search = RandomizedSearchCV(
    estimator=model,
    param_distributions=param_dist,
    n_iter=10,
    cv=5,
    scoring='accuracy',
    random_state=42
)
```

---

### 📌 Important Parameters

* **estimator** → Machine learning model
* **param_distributions** → Dictionary of parameter distributions
* **n_iter** → Number of random combinations to try
* **cv** → Number of cross-validation folds
* **scoring** → Evaluation metric
* **random_state** → Ensures reproducibility

---

### 📊 Output

After fitting:

* `random_search.best_params_` → Best hyperparameters
* `random_search.best_score_` → Best score
* `random_search.best_estimator_` → Best model

---

### ⚖️ Pros & Cons

**Advantages:**

* Faster than GridSearchCV
* Efficient for large datasets
* Can find good solutions quickly

**Disadvantages:**

* May miss the absolute best combination
* Results depend on randomness

---
