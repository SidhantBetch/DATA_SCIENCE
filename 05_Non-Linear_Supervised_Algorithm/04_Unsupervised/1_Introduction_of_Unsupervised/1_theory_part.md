# 📌 Unsupervised Learning

Unsupervised Learning is a type of machine learning where the model learns patterns from **unlabeled data**.

👉 There is **no target/output variable** provided.

The goal is to:

* Discover hidden patterns
* Find structure in data
* Group similar data points

---

## 🧠 Key Idea

Unlike supervised learning:

* ❌ No labels (y)
* ✅ Only input data (X)

Model tries to **learn relationships automatically**.

---

## 🔍 Types of Unsupervised Learning

### 1. Clustering

Grouping similar data points together.

#### Examples:

* K-Means
* Hierarchical Clustering
* DBSCAN

---

### 2. Association

Finding relationships between variables.

#### Example:

* Market Basket Analysis
  (e.g., if a person buys bread → likely to buy butter)

#### Algorithms:

* Apriori
* FP-Growth

---

## ⚙️ Common Algorithms

| Category                 | Algorithms         |
| ------------------------ | ------------------ |
| Clustering               | K-Means, DBSCAN    |
| Association              | Apriori, FP-Growth |
| Dimensionality Reduction | PCA, t-SNE         |

---

## ⚖️ Advantages

* No labeled data required
* Useful for exploratory data analysis
* Finds hidden patterns

---

## ⚠️ Disadvantages

* Hard to evaluate performance
* Results may not be meaningful
* Sensitive to noise and parameters

---

## 🧪 Applications

* Customer segmentation
* Recommendation systems
* Anomaly detection
* Image compression

---

## 🛠️ Python Example (K-Means)

```python id="unsup1"
from sklearn.cluster import KMeans

# Sample data
X = [[1,2], [2,3], [10,11], [11,12]]

# Model
kmeans = KMeans(n_clusters=2)

# Fit model
kmeans.fit(X)

# Predict cluster
labels = kmeans.labels_

print(labels)
```

---
