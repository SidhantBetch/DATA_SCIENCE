# 📌 Deep Learning - Introduction

Deep Learning is a subset of **Machine Learning** that uses **artificial neural networks** with multiple layers to learn patterns from data.

👉 It is inspired by the **human brain** and is capable of handling complex tasks like image recognition, speech processing, and natural language understanding.

---

## 🧠 What is Deep Learning?

Deep Learning uses **Neural Networks** with many hidden layers (hence “deep”) to:

* Automatically extract features
* Learn complex relationships
* Improve performance with large data

---

## 🏗️ Basic Structure of Neural Network

A neural network consists of:

### 1. Input Layer

* Receives input data

---

### 2. Hidden Layers

* Perform computations
* Extract features

---

### 3. Output Layer

* Produces final result

---

## 🔄 How Deep Learning Works

1. Input data is fed into the network
2. Each layer processes data using weights and biases
3. Activation functions introduce non-linearity
4. Output is generated
5. Error is calculated
6. Weights are updated using backpropagation

---

## 🔑 Key Concepts

### 1. Neurons

Basic units that process input signals

---

### 2. Weights & Bias

Parameters that the model learns

---

### 3. Activation Functions

Add non-linearity

Examples:

* ReLU
* Sigmoid
* Tanh

---

### 4. Loss Function

Measures error between prediction and actual value

---

### 5. Backpropagation

Updates weights to minimize error

---

## 📊 Types of Neural Networks

| Type                               | Use Case         |
| ---------------------------------- | ---------------- |
| ANN (Artificial Neural Network)    | General tasks    |
| CNN (Convolutional Neural Network) | Image processing |
| RNN (Recurrent Neural Network)     | Sequential data  |
| LSTM                               | Time series, NLP |

---

## ⚙️ Advantages

* Handles complex data
* Automatic feature extraction
* High accuracy for large datasets

---

## ⚠️ Disadvantages

* Requires large data
* Computationally expensive
* Hard to interpret

---

## 🧪 Applications

* Image recognition
* Speech recognition
* Natural Language Processing (NLP)
* Self-driving cars
* Recommendation systems

---

## 🛠️ Simple Example (Keras)

```python id="dl1"
from tensorflow.keras.models import Sequential
from tensorflow.keras.layers import Dense

model = Sequential()

model.add(Dense(10, input_dim=4, activation='relu'))
model.add(Dense(8, activation='relu'))
model.add(Dense(1, activation='sigmoid'))

model.compile(loss='binary_crossentropy', optimizer='adam', metrics=['accuracy'])

model.fit(X_train, y_train, epochs=50)
```

---
