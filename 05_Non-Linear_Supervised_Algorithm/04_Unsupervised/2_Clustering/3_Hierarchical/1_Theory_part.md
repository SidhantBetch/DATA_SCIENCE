# 📌 Hierarchical Clustering

Hierarchical Clustering is an **unsupervised machine learning algorithm** used to group similar data points into clusters.

It builds a **hierarchy (tree structure)** of clusters, unlike K-Means which creates flat clusters.

---

## 🌳 Key Idea

* Create clusters step by step
* Represent clusters using a **tree (dendrogram)**
* No need to specify number of clusters initially

---

## 🔍 Types of Hierarchical Clustering

### 1. Agglomerative (Bottom-Up)

* Start with each data point as a separate cluster
* Merge closest clusters step by step
* Continue until one cluster remains

👉 Most commonly used method

---

### 2. Divisive (Top-Down)

* Start with all data in one cluster
* Split clusters recursively
* Continue until each point is its own cluster

---

## 📏 Distance Measures

Used to calculate similarity:

* Euclidean Distance
* Manhattan Distance
* Cosine Similarity

---

## 🔗 Linkage Methods

Define how distance between clusters is calculated:

### 1. Single Linkage

* Distance between closest points

---

### 2. Complete Linkage

* Distance between farthest points

---

### 3. Average Linkage

* Average distance between all points

---

### 4. Ward’s Method

* Minimizes variance within clusters

---

## 📊 Dendrogram

A **dendrogram** is a tree-like diagram that shows how clusters are merged.

👉 Used to decide the **optimal number of clusters**

---

## 📈 Example

Data points:

* (1,2), (2,3), (10,11), (11,12)

Clusters merge step-by-step:

* First: (1,2) & (2,3)
* Then: (10,11) & (11,12)
* Finally: both clusters merge

---

## ⚙️ Advantages

* No need to specify number of clusters initially
* Produces a clear hierarchy
* Works well for small datasets

---

## ⚠️ Disadvantages

* Computationally expensive
* Not suitable for large datasets
* Sensitive to noise and outliers

---

## 🛠️ Python Implementation (Scikit-learn)

### Step 1: Dendrogram

```python id="hc1"
import matplotlib.pyplot as plt
import scipy.cluster.hierarchy as sch

dendrogram = sch.dendrogram(sch.linkage(dataset, method='ward'))
plt.title("Dendrogram")
plt.xlabel("Data Points")
plt.ylabel("Distance")
plt.show()
```

---

### Step 2: Apply Clustering

```python id="hc2"
from sklearn.cluster import AgglomerativeClustering

hc = AgglomerativeClustering(n_clusters=2, metric='euclidean', linkage='ward')

labels = hc.fit_predict(dataset)

print(labels)
```

---

## 🧪 Applications

* Customer segmentation
* Biological classification
* Document clustering
* Image segmentation

---
