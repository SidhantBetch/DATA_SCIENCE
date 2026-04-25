# 📌 Apriori Algorithm

Apriori is a popular **unsupervised machine learning algorithm** used for **association rule learning**.

👉 It helps in finding **frequent itemsets** and generating **association rules** from large datasets.

---


## 🔍 Terminology

### 1. Itemset

A collection of one or more items.

Example:

* {Milk, Bread}

---

### 2. Frequent Itemset

Itemsets whose **support ≥ minimum support threshold**

---

### 3. Association Rule

$$
A \Rightarrow B
$$

👉 If A occurs, B is likely to occur.

---

## 🔑 Key Metrics

### 1. Support

$$
Support(A) = \frac{\text{Transactions containing A}}{\text{Total Transactions}}
$$

---

### 2. Confidence

$$
Confidence(A \Rightarrow B) = \frac{Support(A \cap B)}{Support(A)}
$$

---

### 3. Lift

$$
Lift(A \Rightarrow B) = \frac{Confidence(A \Rightarrow B)}{Support(B)}
$$

---

## 🔄 How Apriori Works

1. Set minimum support threshold
2. Generate all possible itemsets
3. Remove itemsets below support threshold
4. Generate larger itemsets from smaller ones
5. Repeat until no more frequent itemsets
6. Generate association rules

---

## 📊 Example

Transactions:

| Transaction | Items         |
| ----------- | ------------- |
| T1          | Milk, Bread   |
| T2          | Milk, Butter  |
| T3          | Bread, Butter |
| T4          | Milk, Bread   |

Frequent itemsets:

* {Milk}, {Bread}, {Butter}
* {Milk, Bread}

Rule:
$Milk \Rightarrow Bread$

---

## ⚙️ Advantages

* Simple and easy to understand
* Finds useful patterns
* Widely used in business analysis

---

## ⚠️ Disadvantages

* Computationally expensive
* Generates large number of candidate itemsets
* Slow for large datasets

---

## 🛠️ Python Implementation

```python id="apriori1"
from mlxtend.frequent_patterns import apriori, association_rules
import pandas as pd

# Sample dataset
data = {
    'Milk': [1,0,1,1],
    'Bread': [1,1,1,0],
    'Butter': [0,1,1,1]
}

df = pd.DataFrame(data)

# Generate frequent itemsets
frequent_items = apriori(df, min_support=0.5, use_colnames=True)

# Generate rules
rules = association_rules(frequent_items, metric="confidence", min_threshold=0.7)

print(frequent_items)
print(rules)
```

---

## 📈 Applications

* Market basket analysis
* Product recommendation
* Customer behavior analysis
* Sales pattern analysis

---
