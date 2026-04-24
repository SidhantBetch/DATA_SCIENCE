# 📌 Stratified K-Fold Cross-Validation

Stratified K-Fold is a variation of K-Fold Cross-Validation that ensures **each fold maintains the same class distribution** as the original dataset.

It is mainly used for **classification problems**, especially when the dataset is **imbalanced**.

---

## 🧠 Why Stratified K-Fold?

In normal K-Fold:

* Class distribution may vary across folds
* Can lead to biased results

Stratified K-Fold solves this by:

* Preserving the **percentage of samples for each class** in every fold

---

## 🔄 How It Works

1. Divide dataset into K folds
2. Ensure each fold has similar class proportions
3. Train on K-1 folds
4. Test on remaining fold
5. Repeat K times
6. Calculate average performance

---

## 📊 Example

### Original Dataset:

| Class | Count |
| ----- | ----- |
| 0     | 80    |
| 1     | 20    |

### Stratified (K = 5):

Each fold will have:

* 16 samples of class 0
* 4 samples of class 1

👉 Maintains **80:20 ratio** in every fold

---

## 🔍 Difference from K-Fold

| Feature            | K-Fold                          | Stratified K-Fold |
| ------------------ | ------------------------------- | ----------------- |
| Class distribution | Not preserved                   | Preserved         |
| Use case           | General                         | Classification    |
| Accuracy           | Less reliable (imbalanced data) | More reliable     |

---

## ⚙️ Python Implementation (Scikit-learn)

### Using StratifiedKFold

```python id="skf1"
from sklearn.model_selection import StratifiedKFold
from sklearn.tree import DecisionTreeClassifier

X = [[1], [2], [3], [4], [5], [6]]
y = [0, 0, 0, 1, 1, 1]

skf = StratifiedKFold(n_splits=3)

model = DecisionTreeClassifier()

for train_index, test_index in skf.split(X, y):
    X_train, X_test = [X[i] for i in train_index], [X[i] for i in test_index]
    y_train, y_test = [y[i] for i in train_index], [y[i] for i in test_index]

    model.fit(X_train, y_train)
    print("Score:", model.score(X_test, y_test))
```

---

### Using cross_val_score

```python id="skf2"
from sklearn.model_selection import cross_val_score, StratifiedKFold

skf = StratifiedKFold(n_splits=5)

scores = cross_val_score(model, X, y, cv=skf)

print("Scores:", scores)
print("Average Score:", scores.mean())
```

---

## ⚖️ Advantages

* Maintains class balance
* More reliable evaluation
* Reduces bias in imbalanced datasets

---

## ⚠️ Disadvantages

* Only applicable to classification
* Slightly more complex than K-Fold

---

