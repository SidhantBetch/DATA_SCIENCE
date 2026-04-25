# 📌 Voting & Averaging Techniques in Ensemble Learning

Voting and averaging are simple yet powerful **ensemble techniques** used to combine predictions from multiple models.

👉 They help improve accuracy and reduce errors by combining outputs from different models.

---

## 🔍 Types of Voting & Averaging

1. **Max Voting (Majority Voting)**
2. **Averaging (Simple Average)**
3. **Weighted Average Voting**

---

## 🗳️ 1. Max Voting (Majority Voting)

### 📖 Definition

Max Voting is used in **classification problems** where the final prediction is the class that gets the **highest number of votes** from different models.

---

### 🧠 How It Works

* Train multiple classifiers
* Each model predicts a class
* Count votes for each class
* Final output = class with **maximum votes**

---

### 📊 Example

| Model   | Prediction |
| ------- | ---------- |
| Model 1 | A          |
| Model 2 | B          |
| Model 3 | A          |

👉 Final Prediction = **A** (majority)

---

### ⚙️ Python Example

```python id="vote1"
from sklearn.ensemble import VotingClassifier
from sklearn.tree import DecisionTreeClassifier
from sklearn.svm import SVC
from sklearn.linear_model import LogisticRegression

model = VotingClassifier(
    estimators=[
        ('dt', DecisionTreeClassifier()),
        ('svm', SVC()),
        ('lr', LogisticRegression())
    ],
    voting='hard'
)

model.fit(X_train, y_train)
```

---

## 📊 2. Averaging (Simple Average)

### 📖 Definition

Used in **regression problems**, where the final prediction is the **average of predictions** from all models.

---

### 🧠 How It Works

$$
\text{Final Prediction} = \frac{y_1 + y_2 + y_3 + ... + y_n}{n}
$$

---

### 📊 Example

Predictions:

* Model 1 → 10
* Model 2 → 20
* Model 3 → 30

👉 Final Prediction:
$\frac{10 + 20 + 30}{3} = 20$

---

### ⚙️ Python Example

```python id="avg1"
import numpy as np

pred1 = model1.predict(X_test)
pred2 = model2.predict(X_test)
pred3 = model3.predict(X_test)

final_pred = np.mean([pred1, pred2, pred3], axis=0)
```

---

## ⚖️ 3. Weighted Average Voting

### 📖 Definition

Each model is assigned a **weight** based on its importance or performance.

👉 Better models get higher weight.

---

### 🧠 How It Works

$$
\text{Final Prediction} = \frac{w_1 y_1 + w_2 y_2 + w_3 y_3}{w_1 + w_2 + w_3}
$$

---

### 📊 Example

Predictions:

* Model 1 → 10 (weight = 0.5)
* Model 2 → 20 (weight = 0.3)
* Model 3 → 30 (weight = 0.2)

$$
= \frac{(0.5 \times 10) + (0.3 \times 20) + (0.2 \times 30)}{1} = 17
$$

---

### ⚙️ Python Example

```python id="wavg1"
import numpy as np

weights = [0.5, 0.3, 0.2]

pred1 = model1.predict(X_test)
pred2 = model2.predict(X_test)
pred3 = model3.predict(X_test)

final_pred = np.average(
    [pred1, pred2, pred3],
    axis=0,
    weights=weights
)
```

---

## 🔍 Comparison

| Method           | Use Case       | Idea                  |
| ---------------- | -------------- | --------------------- |
| Max Voting       | Classification | Majority class wins   |
| Averaging        | Regression     | Equal contribution    |
| Weighted Average | Both           | Weighted contribution |

---

## ⚖️ Advantages

* Simple to implement
* Improves model performance
* Reduces overfitting

---

## ⚠️ Disadvantages

* Requires multiple models
* Choosing weights can be tricky
* Not always better than single strong model

---
