# 📌 Forward and Backward Propagation

Forward and Backward Propagation are the **core processes** used to train neural networks.

👉 They help the model:

* Make predictions (Forward Propagation)
* Learn from errors (Backward Propagation)

---

## 🔄 1. Forward Propagation

### 📖 Definition

Forward propagation is the process of passing input data through the neural network to generate an output.

---

## 🧠 How It Works

1. Input features are fed into the network
2. Each neuron computes weighted sum
3. Activation function is applied
4. Output is passed to next layer
5. Final prediction is generated

---

## 🔢 Mathematical Representation

$$
z = \sum_{i=1}^{n} w_i x_i + b
$$

$a = f(z)$

Where:

* (z) = weighted sum
* (a) = activated output
* (f) = activation function

---

## 📊 Example

Input:

* x = [2, 3]
  Weights:
* w = [0.5, 0.2]
  Bias:
* b = 0.1

$$
z = (2×0.5) + (3×0.2) + 0.1 = 1.7
$$

Apply activation → Output

---

## 🔁 2. Backward Propagation

### 📖 Definition

Backward propagation is the process of **updating weights** by propagating the error backward through the network.

---

## 🧠 Key Idea

* Compare predicted output with actual output
* Calculate error (loss)
* Adjust weights to reduce error

---

## 🔄 Steps in Backpropagation

1. Compute loss (error)
2. Calculate gradient (derivative)
3. Propagate error backward
4. Update weights using gradient descent

---

## 🔢 Weight Update Rule

$$
w = w - \eta \frac{\partial L}{\partial w}
$$

Where:

* (w) = weight
* (\eta) = learning rate
* (L) = loss function

---

## 🔍 Why Backpropagation?

* Minimizes loss
* Improves model accuracy
* Enables deep learning

---

## ⚖️ Forward vs Backward Propagation

| Feature   | Forward Propagation | Backward Propagation |
| --------- | ------------------- | -------------------- |
| Direction | Input → Output      | Output → Input       |
| Purpose   | Prediction          | Learning             |
| Output    | Predicted value     | Updated weights      |

---

## ⚙️ Simple Flow

```
Input → Hidden Layers → Output → Loss → Backpropagation → Update Weights
```

---

## ⚠️ Challenges

* Vanishing gradient problem
* Exploding gradients
* Requires proper learning rate

---

## 🧪 Applications

* Deep learning models
* Image recognition
* NLP
* Speech processing

---
