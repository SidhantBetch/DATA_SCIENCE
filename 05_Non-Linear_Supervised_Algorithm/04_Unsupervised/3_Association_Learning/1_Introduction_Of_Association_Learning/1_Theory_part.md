# Association Learning

## 📌 Introduction

Association Learning is an **unsupervised machine learning technique** used to discover **relationships between variables** in large datasets.

👉 It is widely used in **market basket analysis** to find items that are frequently purchased together.

---

## 🔗 Association Rule

General form:

$A \Rightarrow B$

👉 Meaning:
If item **A** is present, item **B** is likely to be present.

---

## 📊 Example

If customers buy:

* Bread → also buy Butter

Rule:
$Bread \Rightarrow Butter$

---

## 🔑 Key Metrics

### 1. Support

Frequency of occurrence of an itemset:

$$
Support(A) = \frac{\text{Number of transactions containing A}}{\text{Total transactions}}
$$

---

### 2. Confidence

Probability that B occurs given A:

$$
Confidence(A \Rightarrow B) = \frac{Support(A \cap B)}{Support(A)}
$$

---

### 3. Lift

Measures strength of rule:

$$
Lift(A \Rightarrow B) = \frac{Confidence(A \Rightarrow B)}{Support(B)}
$$

### Interpretation:

* Lift > 1 → Positive association
* Lift = 1 → No association
* Lift < 1 → Negative association

---

## 🔍 Common Algorithms

1. Apriori Algorithm
2. FP-Growth
3. Eclat Algorithm

---

## ⚙️ How Association Learning Works

1. Scan dataset
2. Find frequent itemsets
3. Generate association rules
4. Evaluate rules using support, confidence, lift

---

## ⚖️ Advantages

* Finds hidden relationships
* Useful in recommendation systems
* Easy to interpret

---

## ⚠️ Disadvantages

* Computationally expensive
* Generates too many rules
* Requires proper threshold tuning

---

## 🧪 Applications

* Market basket analysis
* Recommendation systems
* Web usage mining
* Fraud detection

---
