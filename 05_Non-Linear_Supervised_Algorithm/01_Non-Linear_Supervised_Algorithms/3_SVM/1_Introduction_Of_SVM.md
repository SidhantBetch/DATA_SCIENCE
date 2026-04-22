# 📌 Support Vector Machine (SVM)

Support Vector Machine (SVM) is a **supervised machine learning algorithm** used for:

* **Classification**
* **Regression (SVR)**
* **Outlier detection**

SVM is powerful for both **linear and non-linear problems** and works well in high-dimensional spaces.

---

## 🧠 Core Idea

SVM tries to find the **optimal hyperplane** that separates data points of different classes with the **maximum margin**.

* **Hyperplane** → Decision boundary
* **Margin** → Distance between hyperplane and nearest data points
* **Support Vectors** → Data points closest to the hyperplane

---

## 📐 Hyperplane Equation

For a linear SVM:

$$
w \cdot x + b = 0
$$

Where:

* ( w ) = weight vector
* ( x ) = input features
* ( b ) = bias

---

## 📏 Margin Concept

The goal is to maximize the margin:

$$
\text{Margin} = \frac{2}{||w||}
$$

Larger margin → Better generalization.

---

## 🔍 Types of SVM

### 1. Linear SVM

* Used when data is **linearly separable**

---

### 2. Non-Linear SVM

* Used when data is not separable by a straight line
* Uses **kernel trick**

---

## 🎯 Kernel Trick

Kernel functions transform data into higher dimensions to make it separable.

### Common Kernels:

#### 1. Linear Kernel

$$
K(x, y) = x \cdot y
$$

#### 2. Polynomial Kernel

$$
K(x, y) = (x \cdot y + c)^d
$$

#### 3. RBF (Gaussian) Kernel

$$
K(x, y) = e^{-\gamma ||x - y||^2}
$$

---

## ⚙️ Important Parameters

* **C (Regularization parameter)**

  * High C → Less margin, low bias, high variance
  * Low C → Large margin, high bias

* **Kernel** → Type of decision boundary

* **Gamma (γ)**

  * Controls influence of a single data point

---

## 📊 Example

### Classification:

If SVM separates two classes:

* Points near boundary → Support vectors
* Hyperplane placed in between with max margin

---

## 🛠️ Python Implementation (Scikit-learn)

### Classification Example

```python id="svm_class"
from sklearn.model_selection import train_test_split
from sklearn.svm import SVC
from sklearn.metrics import accuracy_score

# Sample data
X = [[1,2], [2,3], [3,4], [6,7]]
y = [0, 0, 1, 1]

# Split data
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2)

# Model
model = SVC(kernel='linear', C=1)
model.fit(X_train, y_train)

# Prediction
y_pred = model.predict(X_test)

# Accuracy
print("Accuracy:", accuracy_score(y_test, y_pred))
```

---

### Regression Example (SVR)

```python id="svm_reg"
from sklearn.svm import SVR

model = SVR(kernel='rbf')
model.fit(X_train, y_train)

y_pred = model.predict(X_test)
```

---

## 🧪 Applications

* Image classification
* Face detection
* Text classification
* Bioinformatics
* Handwriting recognition
