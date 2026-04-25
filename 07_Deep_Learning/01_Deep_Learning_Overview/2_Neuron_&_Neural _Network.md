# 📌 Neuron and Neural Network

A **Neuron** is the basic building block of a neural network, and a **Neural Network** is a collection of interconnected neurons used to solve complex problems.

👉 Inspired by the **human brain**, these concepts form the foundation of **Deep Learning**.

---

## 🧠 Artificial Neuron

### 📖 Definition

An artificial neuron is a mathematical function that:

* Takes inputs
* Applies weights and bias
* Produces an output

---

## 🔢 Mathematical Representation

$$
y = f\left(\sum_{i=1}^{n} w_i x_i + b\right)
$$

Where:

* ( x_i ) = Input features
* ( w_i ) = Weights
* ( b ) = Bias
* ( f ) = Activation function
* ( y ) = Output

---

## ⚙️ Components of a Neuron

### 1. Inputs

* Feature values

---

### 2. Weights

* Importance of each input

---

### 3. Bias

* Adjusts output

---

### 4. Activation Function

* Adds non-linearity

Examples:

* ReLU
* Sigmoid
* Tanh

---

## 🏗️ Neural Network

### 📖 Definition

A Neural Network is a collection of multiple neurons organized into layers to perform learning tasks.

---

## 🧩 Structure of Neural Network

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

## 🔄 How Neural Network Works

1. Input data is passed to input layer
2. Each neuron computes weighted sum
3. Activation function is applied
4. Output flows through layers
5. Final prediction is generated

---

## 🔁 Training Process

* Forward Propagation → Compute output
* Loss Calculation → Measure error
* Backpropagation → Update weights

---

## 📊 Example

Input:

* Age, Salary

Output:

* Loan Approval (Yes/No)

👉 Neural network learns relationship automatically

---

## ⚖️ Advantages

* Can model complex relationships
* Works well with large datasets
* Automatic feature learning

---

## ⚠️ Disadvantages

* Requires large data
* Computationally expensive
* Hard to interpret

---

## 🛠️ Simple Python Example (Keras)

```python id="nn1"
from tensorflow.keras.models import Sequential
from tensorflow.keras.layers import Dense

model = Sequential()

model.add(Dense(5, input_dim=3, activation='relu'))
model.add(Dense(1, activation='sigmoid'))

model.compile(loss='binary_crossentropy', optimizer='adam')

model.fit(X_train, y_train, epochs=50)
```

---
