# 📌 Clustering in Machine Learning

Clustering is an **unsupervised learning technique** used to group similar data points together.

👉 Data points in the same cluster are **more similar to each other** than to those in other clusters.

---

## 🔍 Types of Clustering

### 1. Partition-Based Clustering

Divides data into K clusters.

#### Example:

* K-Means

---

### 2. Hierarchical Clustering

Creates a tree-like structure of clusters.

#### Types:

* Agglomerative (bottom-up)
* Divisive (top-down)

---

### 3. Density-Based Clustering

Forms clusters based on density.

#### Example:

* DBSCAN

---

### 4. Distribution-Based Clustering

Assumes data follows a distribution.

#### Example:

* Gaussian Mixture Model (GMM)

---

## 📊 How Clustering Works

1. Measure similarity (distance)
2. Group similar data points
3. Form clusters
4. Optimize grouping

---

## 📏 Distance Metrics

* Euclidean Distance
* Manhattan Distance
* Cosine Similarity

---

## 📊 Example

Customer segmentation:

| Customer | Age | Spending |
| -------- | --- | -------- |
| A        | 20  | 2000     |
| B        | 22  | 2100     |
| C        | 45  | 8000     |

👉 A & B → Same cluster
👉 C → Different cluster

---

## ⚙️ Common Algorithms

| Algorithm    | Type            |
| ------------ | --------------- |
| K-Means      | Partition-Based |
| Hierarchical | Tree-Based      |
| DBSCAN       | Density-Based   |
| GMM          | Probabilistic   |

---

## ⚖️ Advantages

* No labeled data needed
* Helps in pattern discovery
* Useful for segmentation

---

## ⚠️ Disadvantages

* Choosing number of clusters is difficult
* Sensitive to noise
* Results depend on distance metric

---

## 🛠️ Python Example (K-Means)

```python id="cluster1"
from sklearn.cluster import KMeans

X = [[1,2], [2,3], [10,11], [11,12]]

kmeans = KMeans(n_clusters=2)

kmeans.fit(X)

print("Cluster Labels:", kmeans.labels_)
print("Centroids:", kmeans.cluster_centers_)
```

---

## 🧪 Applications

* Customer segmentation
* Image segmentation
* Recommendation systems
* Anomaly detection

---
