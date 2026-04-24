# 📌 K-Means Clustering

K-Means is one of the most popular **unsupervised machine learning algorithms** used for **clustering**.

It groups data into **K number of clusters** based on similarity.

---

## 🔄 How K-Means Works

1. Initialize K centroids randomly
2. Assign each data point to the nearest centroid
3. Recalculate centroids (mean of assigned points)
4. Repeat steps 2 & 3 until clusters stabilize

---

## 📐 Objective Function

K-Means minimizes the **Within-Cluster Sum of Squares (WCSS)**:

$$
WCSS = \sum_{i=1}^{K} \sum_{x \in C_i} (x - \mu_i)^2
$$

Where:

* ( C_i ) = Cluster i
* ( \mu_i ) = Centroid of cluster i

---

## 📊 Example

Data points:

* (1,2), (2,3), (10,11), (11,12)

If K = 2:

👉 Cluster 1 → (1,2), (2,3)
👉 Cluster 2 → (10,11), (11,12)

---

## 📏 Distance Metric

Usually uses **Euclidean Distance**:

$$
d = \sqrt{(x_1 - x_2)^2 + (y_1 - y_2)^2}
$$

---

## 🎯 Choosing K (Elbow Method)

* Plot WCSS vs K
* Choose point where decrease slows down
  👉 That point = optimal K

---

## ⚙️ Advantages

* Simple and fast
* Works well for large datasets
* Easy to implement

---

## ⚠️ Disadvantages

* Need to choose K manually
* Sensitive to initial centroids
* Not suitable for non-spherical data
* Affected by outliers

---

## 🛠️ Python Implementation (Scikit-learn)

```python id="kmeans1"
from sklearn.cluster import KMeans

# Sample data
X = [[1,2], [2,3], [10,11], [11,12]]

# Model
kmeans = KMeans(n_clusters=2, random_state=42)

# Fit model
kmeans.fit(X)

# Outputs
print("Labels:", kmeans.labels_)
print("Centroids:", kmeans.cluster_centers_)
```

---

## 📈 Elbow Method Example

```python id="kmeans2"
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans

wcss = []

for i in range(1, 10):
    kmeans = KMeans(n_clusters=i)
    kmeans.fit(X)
    wcss.append(kmeans.inertia_)

plt.plot(range(1, 10), wcss)
plt.xlabel("Number of Clusters")
plt.ylabel("WCSS")
plt.title("Elbow Method")
plt.show()
```

---

## 🧪 Applications

* Customer segmentation
* Image compression
* Document clustering
* Market analysis

---
