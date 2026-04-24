# 📌 Leave-One-Out Cross-Validation (LOOCV)

Leave-One-Out Cross-Validation (LOOCV) is a special case of K-Fold Cross-Validation where:

$$
K = N
$$

👉 Here, **N = total number of data points**

This means:

* Each iteration uses **1 data point for testing**
* Remaining **N-1 data points for training**

---

## 🧠 How LOOCV Works

1. Take one data point as the test set
2. Train the model on all remaining data
3. Test on that single point
4. Repeat for all data points
5. Compute average performance

---

## 📊 Example

Dataset with 5 samples:

| Iteration | Train Set | Test Set |
| --------- | --------- | -------- |
| 1         | 2,3,4,5   | 1        |
| 2         | 1,3,4,5   | 2        |
| 3         | 1,2,4,5   | 3        |
| 4         | 1,2,3,5   | 4        |
| 5         | 1,2,3,4   | 5        |

---

## 🔢 Formula (Average Score)

$$
\text{LOOCV Score} = \frac{1}{N} \sum_{i=1}^{N} Score_i
$$

---

## ⚙️ Python Implementation (Scikit-learn)

```python id="loocv1"
from sklearn.model_selection import LeaveOneOut, cross_val_score
from sklearn.tree import DecisionTreeClassifier

X = [[1], [2], [3], [4], [5]]
y = [0, 0, 1, 1, 0]

loo = LeaveOneOut()
model = DecisionTreeClassifier()

scores = cross_val_score(model, X, y, cv=loo)

print("Scores:", scores)
print("Average Score:", scores.mean())
```

---

## ⚖️ Advantages

* Uses maximum data for training
* Very low bias
* Works well for small datasets

---

## ⚠️ Disadvantages

* Computationally expensive (very slow)
* High variance (results may fluctuate)
* Not suitable for large datasets

---

## 🔍 LOOCV vs K-Fold

| Feature    | LOOCV     | K-Fold             |
| ---------- | --------- | ------------------ |
| Value of K | N         | Fixed (e.g., 5,10) |
| Speed      | Very slow | Faster             |
| Bias       | Low       | Moderate           |
| Variance   | High      | Lower              |

---

## 🧪 When to Use

* Small datasets
* When maximum training data is needed
* When computational cost is manageable

---
