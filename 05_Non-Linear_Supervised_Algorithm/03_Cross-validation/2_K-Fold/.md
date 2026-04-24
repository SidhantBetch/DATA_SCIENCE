## 📊 K-Fold Cross-Validation

In **K-Fold Cross-Validation**, the dataset is divided into **K equal parts (folds)**.

### 🧠 Process

1. Split data into K folds
2. Train the model on K-1 folds
3. Test on the remaining fold
4. Repeat K times (each fold becomes test once)
5. Compute average performance

---

### 📌 Example (K = 5)

| Fold | Training Data  | Testing Data |
| ---- | -------------- | ------------ |
| 1    | F2, F3, F4, F5 | F1           |
| 2    | F1, F3, F4, F5 | F2           |
| 3    | F1, F2, F4, F5 | F3           |
| 4    | F1, F2, F3, F5 | F4           |
| 5    | F1, F2, F3, F4 | F5           |

---

## 🔢 Formula (Average Score)

$$
\text{CV Score} = \frac{1}{K} \sum_{i=1}^{K} Score_i
$$

---

### K-Fold Example

```python id="cv_kfold"
from sklearn.model_selection import KFold

kf = KFold(n_splits=5)

for train_index, test_index in kf.split(X):
    print("Train:", train_index, "Test:", test_index)
```

---
