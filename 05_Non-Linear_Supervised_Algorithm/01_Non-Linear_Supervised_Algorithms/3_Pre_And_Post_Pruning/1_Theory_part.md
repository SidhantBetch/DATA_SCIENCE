# 📌 Pruning

Decision Trees are powerful but prone to **overfitting**, where the model learns noise instead of the actual pattern.

**Pruning** is the process of reducing the size of a decision tree to improve generalization.

There are two main types:

* **Pre-Pruning (Early Stopping)**
* **Post-Pruning (Late Pruning)**

---

## 🌳 Why Pruning is Important

Without pruning:

* Tree becomes too complex
* High variance (overfitting)
* Poor performance on unseen data

With pruning:

* Simpler model
* Better generalization
* Reduced overfitting

---

## ✂️ Pre-Pruning (Early Stopping)

### 📖 Definition

Pre-pruning stops the tree from growing **before it becomes too complex**.

### 🧠 How it Works

The algorithm stops splitting a node when certain conditions are met.

---

### ⚙️ Common Pre-Pruning Parameters

* **max_depth** → Maximum depth of the tree
* **min_samples_split** → Minimum samples required to split a node
* **min_samples_leaf** → Minimum samples required at a leaf node
* **max_leaf_nodes** → Maximum number of leaf nodes
* **min_impurity_decrease** → Minimum reduction in impurity required

---

### 📊 Example

If `max_depth = 3`, the tree will stop growing after 3 levels.

---

### ✅ Advantages

* Reduces training time
* Prevents overfitting early
* Simpler trees

---

### ⚠️ Disadvantages

* May lead to **underfitting**
* Might stop too early before learning patterns

---

## ✂️ Post-Pruning (Late Pruning)

### 📖 Definition

Post-pruning allows the tree to grow fully and then **removes unnecessary branches**.

---

### 🧠 How it Works

1. Build the full tree
2. Evaluate subtrees
3. Remove branches that do not improve performance

---

### 🔍 Methods of Post-Pruning

#### 1. Cost Complexity Pruning (CCP)

* Also called **Weakest Link Pruning**
* Balances:

  * Tree complexity
  * Model accuracy

Formula:

$$
R_\alpha(T) = R(T) + \alpha \cdot |T|
$$

Where:

* ( R(T) ) = Error of the tree
* ( |T| ) = Number of leaves
* ( \alpha ) = Complexity parameter

---

### 📊 Example

If removing a branch does not significantly increase error → remove it.

---

### ✅ Advantages

* Better generalization
* More accurate than pre-pruning
* Reduces overfitting effectively

---

### ⚠️ Disadvantages

* More computationally expensive
* Requires full tree construction

---

## 🔄 Pre-Pruning vs Post-Pruning

| Feature            | Pre-Pruning       | Post-Pruning      |
| ------------------ | ----------------- | ----------------- |
| When applied       | During training   | After training    |
| Speed              | Faster            | Slower            |
| Risk               | Underfitting      | Less underfitting |
| Accuracy           | Lower (sometimes) | Higher            |
| Complexity control | Early stopping    | Tree trimming     |

---

## 🛠️ Python Implementation (Scikit-learn)

### Pre-Pruning Example

```python id="pre123"
from sklearn.tree import DecisionTreeClassifier

model = DecisionTreeClassifier(
    max_depth=3,
    min_samples_split=5,
    min_samples_leaf=2
)

model.fit(X_train, y_train)
```

---

### Post-Pruning Example (Cost Complexity Pruning)

```python id="post123"
from sklearn.tree import DecisionTreeClassifier

model = DecisionTreeClassifier(ccp_alpha=0.01)
model.fit(X_train, y_train)
```

---

## 🧪 When to Use What?

* Use **Pre-Pruning** when:

  * Dataset is large
  * Faster training is needed

* Use **Post-Pruning** when:

  * Accuracy is more important
  * You want better generalization

---

## 📚 Conclusion

Both pruning techniques help improve Decision Tree performance:

* **Pre-Pruning** is fast but may stop too early
* **Post-Pruning** is more reliable but computationally expensive

Choosing the right method depends on your dataset and problem.

---

## 🔖 References

* Scikit-learn Documentation
* Machine Learning Books
* Online Tutorials

---
