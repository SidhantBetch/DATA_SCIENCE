# 🐦‍🔥 Optimizers in Machine Learning & Deep Learning

An **Optimizer** is an algorithm used to **update model parameters (weights & bias)** to minimize the loss function.

👉 It helps the model learn by finding the **best parameters** that reduce error.

---

## 🔄 Basic Concept (Gradient Descent)

$$
w = w - \eta \frac{\partial L}{\partial w}
$$

Where:

* (w) = weight
* (\eta) = learning rate
* (L) = loss function

---

## 🔍 Types of Optimizers

---

## 1. Gradient Descent

### 📖 Definition

Updates weights using the **entire dataset**

### ⚙️ Types:

* Batch Gradient Descent
* Stochastic Gradient Descent (SGD)
* Mini-batch Gradient Descent

---

## 2. Stochastic Gradient Descent (SGD)

### 📖 Definition

Updates weights using **one data point at a time**

### ⚙️ Advantage

* Faster updates

### ⚠️ Disadvantage

* Noisy convergence

---

## 3. Momentum

### 📖 Idea

Uses **previous gradients** to smooth updates

### Benefit

* Faster convergence
* Reduces oscillation

---

## 4. AdaGrad

### 📖 Idea

Adapts learning rate for each parameter

### Benefit

* Good for sparse data

---

## 5. RMSProp

### 📖 Idea

Fixes AdaGrad’s learning rate decay issue

### Benefit

* Works well for non-stationary problems

---

## 6. Adam (Adaptive Moment Estimation)

### 📖 Idea

Combines **Momentum + RMSProp**

### Benefit

* Fast and efficient
* Most widely used optimizer

---

## ⚖️ Comparison

| Optimizer | Speed   | Stability | Use Case      |
| --------- | ------- | --------- | ------------- |
| GD        | Slow    | Stable    | Small data    |
| SGD       | Fast    | Noisy     | Large data    |
| Momentum  | Faster  | Stable    | Deep learning |
| Adam      | Fastest | Stable    | Most tasks    |

---

## ⚙️ Learning Rate ((\eta))

* Controls step size
* Too high → Overshooting
* Too low → Slow learning

---

## 🛠️ Python Example (Keras)

```python id="opt1"
from tensorflow.keras.models import Sequential
from tensorflow.keras.layers import Dense
from tensorflow.keras.optimizers import Adam

model = Sequential()
model.add(Dense(10, input_dim=4, activation='relu'))
model.add(Dense(1, activation='sigmoid'))

model.compile(
    optimizer=Adam(learning_rate=0.001),
    loss='binary_crossentropy',
    metrics=['accuracy']
)

model.fit(X_train, y_train, epochs=50)
```

---

## 🧪 Applications

* Neural network training
* Deep learning models
* Computer vision
* NLP

---
