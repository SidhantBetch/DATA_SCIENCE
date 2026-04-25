# 📌 Multi-Layer Perceptron (MLP)

A **Multi-Layer Perceptron (MLP)** is a type of **artificial neural network** that consists of **multiple layers of neurons**.

👉 Unlike a single-layer perceptron, MLP can solve **non-linear problems**.

---

## 🧩 Structure of MLP

```id="mlpdiag1"
Input Layer  →  Hidden Layer(s)  →  Output Layer

   x1  ----\
   x2  -----\        (Hidden Neurons)        ----> Output
   x3  ------>  [ ● ● ● ● ● ]  ---->
```

---

## 🔢 Mathematical Representation

For one neuron:

$y = f\left(\sum_{i=1}^{n} w_i x_i + b\right)$

👉 In MLP:

* This computation happens **across multiple layers**

---

## 🔄 How MLP Works

### 1. Forward Propagation

* Input passes through layers
* Each neuron computes weighted sum
* Activation function applied

---

### 2. Loss Calculation

* Compare predicted vs actual output

---

### 3. Backpropagation

* Calculate gradients
* Update weights using optimization

---

## 🔌 Activation Functions

Common functions:

* ReLU (Rectified Linear Unit)
* Sigmoid
* Tanh
* Softmax (for multi-class output)

---

## 📊 Example

Problem:

* Predict house price

Input:

* Area, Bedrooms, Location

MLP learns:

* Complex relationship between features

---

## ⚙️ Advantages

* Handles non-linear data
* Flexible architecture
* High accuracy for complex tasks

---

## ⚠️ Disadvantages

* Requires large data
* Computationally expensive
* Needs parameter tuning

---

## 🛠️ Python Implementation (Scikit-learn)

```python id="mlp1"
from sklearn.neural_network import MLPClassifier

model = MLPClassifier(
    hidden_layer_sizes=(100, 50),
    activation='relu',
    max_iter=500
)

model.fit(X_train, y_train)

y_pred = model.predict(X_test)
```

---

## 📊 Regression Example

```python id="mlp2"
from sklearn.neural_network import MLPRegressor

model = MLPRegressor(
    hidden_layer_sizes=(100, 50),
    max_iter=500
)

model.fit(X_train, y_train)
```

---

## 🔍 Single Layer vs Multi-Layer

| Feature             | Single Layer | MLP   |
| ------------------- | ------------ | ----- |
| Hidden Layers       | ❌ No         | ✅ Yes |
| Non-linear Problems | ❌ No         | ✅ Yes |
| Complexity          | Low          | High  |

---

## 🧪 Applications

* Image recognition
* Speech recognition
* NLP tasks
* Recommendation systems

---
