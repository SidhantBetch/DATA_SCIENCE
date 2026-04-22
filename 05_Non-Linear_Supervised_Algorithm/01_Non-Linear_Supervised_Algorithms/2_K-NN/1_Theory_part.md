# 📌 K-Nearest Neighbors (KNN) Algorithm

K-Nearest Neighbors (KNN) is a **supervised machine learning algorithm** used for:

* **Classification**
* **Regression**

It is a **lazy learning algorithm**, meaning it does not learn a model during training but makes predictions based on stored data.

---

## 🧠 How KNN Works

KNN works by finding the **K closest data points (neighbors)** to a given input and making predictions based on them.

### Steps:

1. Choose the number of neighbors (K)
2. Calculate distance between the query point and all training points
3. Select the K nearest neighbors
4. * **Classification** → Majority voting
   * **Regression** → Average of values

---

## 📏 Distance Metrics

Distance calculation is the core of KNN.

### 1. Euclidean Distance

$$
d = \sqrt{\sum_{i=1}^{n} (x_i - y_i)^2}
$$

---

### 2. Manhattan Distance

$$
d = \sum_{i=1}^{n} |x_i - y_i|
$$

---

### 3. Minkowski Distance

General form:

$$
d = \left( \sum_{i=1}^{n} |x_i - y_i|^p \right)^{1/p}
$$

---

## 📊 Example

### Classification Example:

Data points:

* Red class
* Blue class

New point:

* K = 3

If 2 neighbors are Red and 1 is Blue → Output = **Red**

---

### Regression Example:

Neighbors' values:

* 10, 20, 30

Prediction:

$$
\frac{10 + 20 + 30}{3} = 20
$$

---

## ⚙️ Choosing the Value of K

* Small K → High variance (overfitting)
* Large K → High bias (underfitting)

### Common practice:

* Use **odd values** (for classification)
* Use **cross-validation** to find optimal K

---

## ⚖️ Advantages

* Simple and easy to understand
* No training phase
* Works well with small datasets
* Flexible (classification + regression)

---

## ⚠️ Disadvantages

* Slow for large datasets
* Memory intensive
* Sensitive to irrelevant features
* Requires feature scaling

---

## 📉 Importance of Feature Scaling

KNN is distance-based, so scaling is important.

### Common methods:

* Standardization
* Normalization

---

## 🛠️ Python Implementation (Scikit-learn)

### Classification Example

```python id="knn_class"
from sklearn.model_selection import train_test_split
from sklearn.neighbors import KNeighborsClassifier
from sklearn.metrics import accuracy_score

# Sample data
X = [[1,2], [2,3], [3,4], [6,7]]
y = [0, 0, 1, 1]

# Split data
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2)

# Model
model = KNeighborsClassifier(n_neighbors=3)
model.fit(X_train, y_train)

# Prediction
y_pred = model.predict(X_test)

# Accuracy
print("Accuracy:", accuracy_score(y_test, y_pred))
```

---

### Regression Example

```python id="knn_reg"
from sklearn.neighbors import KNeighborsRegressor

model = KNeighborsRegressor(n_neighbors=3)
model.fit(X_train, y_train)

y_pred = model.predict(X_test)
```
