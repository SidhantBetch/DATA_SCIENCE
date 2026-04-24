# 📌 Silhouette Score

Silhouette Score is a metric used to evaluate the quality of **clustering models**.

👉 It measures how well each data point fits within its cluster compared to other clusters.

---

## 🔢 Formula

$$
s = \frac{b - a}{\max(a, b)}
$$

Where:

* ( a ) = Average distance to points in the same cluster
* ( b ) = Average distance to points in the nearest cluster

---

## 📊 Score Range

| Value | Meaning              |
| ----- | -------------------- |
| +1    | Perfect clustering   |
| 0     | Overlapping clusters |
| -1    | Wrong clustering     |

---

## 📈 Interpretation

* **s ≈ 1** → Well-separated clusters
* **s ≈ 0** → Clusters are overlapping
* **s < 0** → Data points assigned to wrong clusters

---

## 🔍 Why Use Silhouette Score?

* Helps determine **optimal number of clusters (K)**
* Evaluates clustering performance
* Works without labeled data

---

## ⚙️ Python Implementation (Scikit-learn)

```python id="sil1"
from sklearn.metrics import silhouette_score
from sklearn.cluster import KMeans

# Sample data
X = [[1,2], [2,3], [10,11], [11,12]]

# Model
kmeans = KMeans(n_clusters=2, random_state=42)
labels = kmeans.fit_predict(X)

# Silhouette Score
score = silhouette_score(X, labels)

print("Silhouette Score:", score)
```

---

## 📊 Finding Best K

```python id="sil2"
from sklearn.metrics import silhouette_score
from sklearn.cluster import KMeans

scores = []

for i in range(2, 10):
    kmeans = KMeans(n_clusters=i, random_state=42)
    labels = kmeans.fit_predict(X)
    scores.append(silhouette_score(X, labels))

print(scores)
```

---

## ⚖️ Advantages

* Easy to interpret
* No need for true labels
* Works for most clustering algorithms

---

## ⚠️ Disadvantages

* Not suitable for clusters with varying density
* Can be slow for large datasets
* Assumes convex clusters

---

## 🧪 Applications

* Choosing optimal K in K-Means
* Evaluating clustering quality
* Comparing clustering algorithms

---
