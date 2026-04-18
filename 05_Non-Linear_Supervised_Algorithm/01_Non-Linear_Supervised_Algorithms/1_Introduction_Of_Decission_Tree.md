# Decision Tree Algorithm

## 📌 Introduction

A **Decision Tree** is a **supervised machine learning algorithm** used for both:

* Classification
* Regression

It works like a **flowchart structure**, where:

* Each **internal node** represents a feature (decision)
* Each **branch** represents a rule
* Each **leaf node** represents the final outcome

---

## 🌳 How Decision Tree Works

The algorithm splits the dataset into subsets based on the most important feature.

### Basic Steps:

1. Select the best feature using a splitting criterion
2. Split the dataset into subsets
3. Repeat recursively for each subset
4. Stop when:

   * All data belongs to the same class, or
   * Maximum depth is reached

---

## 📊 Splitting Criteria

### 1. Gini Impurity

Used in classification tasks (CART algorithm)

$$
Gini = 1 - \sum_{i=1}^{n} p_i^2
$$

* Measures impurity (how mixed the classes are)
* Lower value = better split

---

### 2. Entropy (Information Gain)

Used in ID3 algorithm

$$
Entropy = -\sum_{i=1}^{n} p_i \log_2(p_i)
$$

**Information Gain:**

$$
IG = Entropy(Parent) - \sum Weighted\ Entropy(Children)
$$

* Higher Information Gain = better split

---

## 🧠 Types of Decision Trees

### 1. Classification Tree
#### 📌 Introduction
A Decision Tree is a supervised machine learning algorithm used for classification and regression tasks.
In classification, it predicts the class label of a given input by learning simple decision rules inferred from data features.

It works like a flowchart structure:
- Internal nodes → feature tests
- Branches → outcomes of tests
- Leaf nodes → final class labels

#### 🧩 Example

Suppose we want to classify whether a person will **Buy Product or Not** based on:

* Age
* Income
* Student
* Credit Score

The tree may look like:

```
           Age?
         /      \
     <30        >=30
     /             \
 Student?        Credit Score?
  /    \           /       \
Yes    No      Good       Poor
 |      |         |          |
Buy   Not Buy   Buy       Not Buy
```

---


### 2. Regression Tree

#### 📌 Introduction

Decision Tree Regression is a supervised machine learning algorithm used to predict continuous numerical values.

Unlike classification trees, which predict categories, regression trees predict real-valued outputs by splitting the data into regions and assigning an average value to each region.

---

#### 📊 Example
Suppose we want to predict house price based on size:

Size (sq ft) |	Price
-------------|----------
1000	| 2L
1500	| 3L
2000	| 4L

***Tree splits like:***
- If size < 1500 → Predict ~2L
- Else → Predict average (~3.5L)

---

## 🌱 Important Terms

* **Root Node** → Topmost node
* **Decision Node** → Internal node where splitting happens
* **Leaf Node** → Final output node
* **Branch** → Connection between nodes
* **Depth** → Maximum levels in the tree

---

## ⚙️ Advantages

* Easy to understand and visualize
* No need for feature scaling
* Works with both numerical and categorical data
* Handles non-linear relationships

---

## ⚠️ Disadvantages

* Prone to **overfitting**
* Sensitive to small changes in data
* Can become complex for large datasets

---

## ✂️ Overfitting & Pruning

### Overfitting

When the model learns noise instead of patterns.

### Pruning

Reducing the size of the tree to improve generalization:

* **Pre-pruning** → Stop early (max depth, min samples)
* **Post-pruning** → Remove unnecessary branches

---

## 📊 Example

Suppose we want to predict whether a person will buy a product based on:

* Age
* Income

The tree might split like:

* Age < 30 → No
* Age ≥ 30 → Check Income

  * High → Yes
  * Low → No

---

## 🛠️ Python Implementation (Scikit-learn)

```python
from sklearn.model_selection import train_test_split
from sklearn.tree import DecisionTreeClassifier
from sklearn.metrics import accuracy_score

# Sample data
X = [[25, 50000], [35, 60000], [45, 80000], [20, 20000]]
y = [0, 1, 1, 0]

# Split data
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2)

# Model
model = DecisionTreeClassifier(criterion='gini')
model.fit(X_train, y_train)

# Prediction
y_pred = model.predict(X_test)

# Accuracy
print("Accuracy:", accuracy_score(y_test, y_pred))
```

---

## 🧪 Applications

* Fraud detection
* Medical diagnosis
* Customer segmentation
* Credit risk analysis

---

## 📚 Conclusion

Decision Trees are one of the most **intuitive and powerful algorithms** in machine learning.
They are easy to interpret but require proper tuning to avoid overfitting.

---

## 🔖 References

* Scikit-learn Documentation
* Machine Learning Books
* Online Tutorials

---
