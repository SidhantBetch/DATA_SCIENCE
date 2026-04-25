# 📌 Activation Functions in Neural Networks

Activation functions are mathematical functions used in neural networks to introduce **non-linearity**.

👉 Without activation functions, a neural network behaves like a **linear model**.

---

## 🧠 Why Activation Functions?

* Enable learning of complex patterns
* Introduce non-linearity
* Help neural networks solve real-world problems

---

## 🧩 Where It Is Used?

```id="actdiag1"
Input → [Weighted Sum (z)] → [Activation Function] → Output (a)
```

---

## 🔢 Basic Formula

a = f(z)

Where:

* (z = \sum w_ix_i + b)
* (f) = activation function
* (a) = output

---

## 🔍 Types of Activation Functions

---

## 1. Sigmoid Function

### 📖 Formula

$$
\sigma(x) = \frac{1}{1 + e^{-x}}
$$

### 📊 Diagram (Shape)

```id="sigmoid"
     |
 1.0 |        ______
     |      /
     |    /
 0.5 |---/---------
     |  /
     | /
 0.0 |/____________
        -∞     +∞
```

### ⚙️ Properties

* Output range: (0,1)
* Used in binary classification

---

### ⚠️ Disadvantages

* Vanishing gradient problem
* Slow learning

---

## 2. ReLU (Rectified Linear Unit)

### 📖 Formula

$$
f(x) = \max(0, x)
$$

### 📊 Diagram

```id="relu"
     |
     |        /
     |       /
     |      /
 0.0 |_____/________
        0       +∞
```

### ⚙️ Properties

* Fast and efficient
* Most widely used

---

### ⚠️ Disadvantages

* Dead neuron problem

---

## 3. Tanh Function

### 📖 Formula

$$
tanh(x) = \frac{e^x - e^{-x}}{e^x + e^{-x}}
$$

### 📊 Diagram

```id="tanh"
     |
 1.0 |      ______
     |     /
 0.0 |----/------
     |   /
-1.0 |__/
        -∞   +∞
```

### ⚙️ Properties

* Output range: (-1,1)
* Zero-centered

---

## 4. Softmax Function

### 📖 Formula

$$
\text{Softmax}(x_i) = \frac{e^{x_i}}{\sum e^{x_j}}
$$

### 📊 Use

* Used in **multi-class classification**
* Converts outputs into probabilities

---

## 🔍 Comparison

| Function | Range  | Use Case                   |
| -------- | ------ | -------------------------- |
| Sigmoid  | (0,1)  | Binary classification      |
| ReLU     | [0,∞)  | Hidden layers              |
| Tanh     | (-1,1) | Better than sigmoid        |
| Softmax  | (0,1)  | Multi-class classification |

---

## ⚖️ Advantages

* Enables deep learning
* Improves model performance
* Helps learn complex patterns

---

## ⚠️ Disadvantages

* Some functions suffer from vanishing gradients
* Need careful selection

---

## 🧪 Applications

* Image recognition
* NLP
* Speech processing
* Deep learning models

---

## 📚 Conclusion

Activation functions are essential in neural networks as they introduce non-linearity and allow models to learn complex patterns effectively.

---

## 🔖 References

* Deep Learning Books
* TensorFlow Documentation
* Online Tutorials

---
