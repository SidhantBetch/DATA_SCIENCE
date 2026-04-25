# 📌 Single Layer Perceptron

A **Single Layer Perceptron** is the simplest type of **artificial neural network**.

👉 It consists of:

* One input layer
* One output neuron
* No hidden layers

It is mainly used for **binary classification problems**.

---

## 🧩 Structure (Diagram)

```
   x1 ----(w1)----\
   x2 ----(w2)-----\ 
   x3 ----(w3)------> [ Σ ] ----> [ Activation ] ----> Output (y)
                    /
               + Bias (b)
```

---

## 🔢 Mathematical Representation

$$
y = f\left(\sum_{i=1}^{n} w_i x_i + b\right)
$$

Where:

* (x_i) = Input features
* (w_i) = Weights
* (b) = Bias
* (f) = Activation function

---

## ⚙️ Working Steps

1. Multiply inputs with weights
2. Add bias
3. Apply activation function
4. Generate output

---

## 🔌 Activation Function (Step Function)

$$
y =
\begin{cases}
1 & \text{if } z \geq 0 \
0 & \text{if } z < 0
\end{cases}
$$

---

## 📊 Example

Inputs:

* x1 = 1, x2 = 0

Weights:

* w1 = 0.5, w2 = 0.3

Bias:

* b = -0.2

$$
z = (1 \times 0.5) + (0 \times 0.3) - 0.2 = 0.3
$$

👉 Output = 1

---

## ⚖️ Advantages

* Simple and easy to understand
* Fast computation
* Works well for linearly separable data

---

## ⚠️ Disadvantages

* Cannot solve non-linear problems (e.g., XOR)
* Limited to binary classification
* No hidden layers

---

## 🛠️ Python Example (Scikit-learn)

```python id="per1"
from sklearn.linear_model import Perceptron

model = Perceptron()

model.fit(X_train, y_train)

y_pred = model.predict(X_test)
```

---
