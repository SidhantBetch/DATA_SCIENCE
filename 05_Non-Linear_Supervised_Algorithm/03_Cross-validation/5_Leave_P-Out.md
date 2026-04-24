# 📌 Leave-P-Out Cross-Validation (LPOCV)

Leave-P-Out Cross-Validation (LPOCV) is an extension of Leave-One-Out Cross-Validation (LOOCV), where instead of leaving **one** data point out, we leave **P data points** out for testing.

👉 In each iteration:

* **P samples** are used as the test set
* Remaining **N - P samples** are used for training

---

## 🧠 How It Works

1. Select P data points as the test set
2. Train the model on the remaining data
3. Evaluate the model
4. Repeat for all possible combinations of P samples
5. Compute average performance

---

## 🔢 Number of Iterations

The total number of combinations is:

$$
\binom{N}{P} = \frac{N!}{P!(N - P)!}
$$

Where:

* ( N ) = Total number of samples
* ( P ) = Number of samples left out

---

## 📊 Example

Dataset with 5 samples (N = 5), P = 2:

Possible test sets:

* (1,2), (1,3), (1,4), (1,5)
* (2,3), (2,4), (2,5)
* (3,4), (3,5)
* (4,5)

👉 Total iterations = 10

---

## ⚙️ Python Implementation (Scikit-learn)

```python id="lpocv1"
from sklearn.model_selection import LeavePOut, cross_val_score
from sklearn.tree import DecisionTreeClassifier

X = [[1], [2], [3], [4], [5]]
y = [0, 0, 1, 1, 0]

lpo = LeavePOut(p=2)
model = DecisionTreeClassifier()

scores = cross_val_score(model, X, y, cv=lpo)

print("Scores:", scores)
print("Average Score:", scores.mean())
```

---

## ⚖️ Advantages

* Uses multiple data points for testing
* More flexible than LOOCV
* Better performance estimation than simple splits

---

## ⚠️ Disadvantages

* Extremely computationally expensive
* Number of combinations grows very fast
* Not practical for large datasets

---

## 🔍 LPOCV vs LOOCV

| Feature      | LOOCV (P=1) | LPOCV (P>1) |
| ------------ | ----------- | ----------- |
| Test samples | 1           | P           |
| Iterations   | N           | C(N, P)     |
| Complexity   | High        | Very high   |
| Flexibility  | Low         | High        |

---

## 🧪 When to Use

* Very small datasets
* When more flexible validation is required
* When computational cost is manageable

---
