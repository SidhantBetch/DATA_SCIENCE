# 📌  DBSCAN Clustering (Density-Based Spatial Clustering of Applications with Noise)

DBSCAN is an **unsupervised machine learning algorithm** used for clustering based on **data density**.

👉 It groups together points that are closely packed and marks points in low-density regions as **outliers (noise)**.

---

## 🔑 Key Parameters

### 1. eps (ε)

* Maximum distance between two points to be considered neighbors

---

### 2. min_samples

* Minimum number of points required to form a dense region

---

## 🔍 Types of Points

### 1. Core Points

* Have at least `min_samples` points within `eps` radius

---

### 2. Border Points

* Within `eps` of a core point but have fewer neighbors

---

### 3. Noise Points

* Not reachable from any core point

---

## 🔄 How DBSCAN Works

1. Pick an unvisited point
2. Check if it is a core point
3. If yes → form a cluster
4. Expand cluster by adding neighbors
5. Repeat until all points are processed

---

## 📊 Example

Data:

* Dense region → forms cluster
* Sparse region → labeled as noise

👉 DBSCAN can detect clusters of **arbitrary shapes**

---

## ⚙️ Advantages

* No need to choose number of clusters (K)
* Handles noise/outliers well
* Can find non-spherical clusters

---

## ⚠️ Disadvantages

* Sensitive to `eps` and `min_samples`
* Not suitable for varying density datasets
* Difficult to choose optimal parameters

---

## 🛠️ Python Implementation (Scikit-learn)

```python id="dbscan1"
from sklearn.cluster import DBSCAN

# Sample data
X = [[1,2], [2,3], [10,11], [11,12], [50,60]]

# Model
db = DBSCAN(eps=3, min_samples=2)

# Fit model
labels = db.fit_predict(X)

print("Cluster Labels:", labels)
```

---

## 📊 Output Interpretation

* Cluster labels → 0, 1, 2, ...
* Noise points → labeled as **-1**

---

## 📈 Parameter Selection Tips

* Use **k-distance graph** to choose `eps`
* Start with:

  * `min_samples = 2 * number_of_features`

---

## 🧪 Applications

* Anomaly detection
* Spatial data analysis
* Image processing
* Fraud detection

---

## 🔍 DBSCAN vs K-Means

| Feature        | DBSCAN    | K-Means   |
| -------------- | --------- | --------- |
| Need K         | ❌ No      | ✅ Yes     |
| Shape          | Arbitrary | Spherical |
| Noise handling | ✅ Yes     | ❌ No      |
| Speed          | Slower    | Faster    |

---
