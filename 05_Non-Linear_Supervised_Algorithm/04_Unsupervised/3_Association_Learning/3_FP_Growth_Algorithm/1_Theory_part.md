# 📌 FP-Growth Algorithm (Frequent Pattern Growth)

FP-Growth is an efficient **unsupervised machine learning algorithm** used for **association rule mining**.

👉 It is an improved version of the Apriori algorithm and is designed to find **frequent itemsets without generating candidate sets**.

---

## 🌳 FP-Tree (Frequent Pattern Tree)

An FP-Tree is a compact representation of the dataset.

### Features:

* Stores item frequency
* Shares common prefixes
* Reduces dataset size

---

## 🔑 Key Concepts

### 1. Frequent Itemset

Itemsets whose **support ≥ minimum support threshold**

---

### 2. Conditional Pattern Base

Subsets of the dataset related to a specific item

---

### 3. Conditional FP-Tree

A smaller FP-tree built for a specific item

---

## 🔄 How FP-Growth Works

### Step 1: Scan Dataset

* Calculate support of each item
* Remove infrequent items

---

### Step 2: Build FP-Tree

* Sort items by frequency
* Insert transactions into tree

---

### Step 3: Mine the FP-Tree

* Extract patterns recursively
* Generate frequent itemsets

---

## 📊 Example

Transactions:

| TID | Items         |
| --- | ------------- |
| T1  | Milk, Bread   |
| T2  | Milk, Butter  |
| T3  | Bread, Butter |
| T4  | Milk, Bread   |

👉 FP-Tree compresses this data and finds patterns like:

* {Milk, Bread}
* {Bread, Butter}

---

## ⚙️ Advantages

* Faster than Apriori
* No candidate generation
* Efficient for large datasets
* Reduced database scans

---

## ⚠️ Disadvantages

* Complex implementation
* Tree structure can be memory-intensive
* Less intuitive than Apriori

---

## 🛠️ Python Implementation (mlxtend)

```python id="fpgrowth1"
from mlxtend.frequent_patterns import fpgrowth, association_rules
import pandas as pd

# Sample dataset
data = {
    'Milk': [1,0,1,1],
    'Bread': [1,1,1,0],
    'Butter': [0,1,1,1]
}

df = pd.DataFrame(data)

# Generate frequent itemsets
frequent_items = fpgrowth(df, min_support=0.5, use_colnames=True)

# Generate association rules
rules = association_rules(frequent_items, metric="confidence", min_threshold=0.7)

print(frequent_items)
print(rules)
```

---

## 📈 Applications

* Market basket analysis
* Recommendation systems
* Web usage mining
* Customer behavior analysis

---

## 🔍 FP-Growth vs Apriori

| Feature        | FP-Growth     | Apriori   |
| -------------- | ------------- | --------- |
| Speed          | Faster        | Slower    |
| Candidate sets | Not generated | Generated |
| Efficiency     | High          | Low       |
| Complexity     | Higher        | Lower     |

---
