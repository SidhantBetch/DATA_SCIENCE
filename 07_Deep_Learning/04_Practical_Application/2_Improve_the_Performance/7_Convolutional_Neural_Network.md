#  🐦‍🔥 Convolutional Neural Network (CNN)

A **Convolutional Neural Network (CNN)** is a type of **deep learning model** mainly used for **image processing and computer vision tasks**.

👉 It can automatically detect important features like:

* Edges
* Shapes
* Textures

---

## 🧠 Key Idea

* Uses **convolution operations** instead of fully connected layers
* Learns **spatial features** from images
* Reduces number of parameters

---

## 🧩 Basic Architecture

```id="cnn1"
Input Image → Convolution → Activation → Pooling → Flatten → Fully Connected → Output
```

---

## 🔍 Key Components

---

### 🔹 1. Convolution Layer

* Applies filters (kernels) to input
* Extracts features

[
\text{Feature Map} = \text{Input} * \text{Kernel}
]

---

### 🔹 2. Activation Function

* Introduces non-linearity
* Common: ReLU

---

### 🔹 3. Pooling Layer

* Reduces spatial size
* Keeps important features

Types:

* Max Pooling
* Average Pooling

---

### 🔹 4. Flatten Layer

* Converts 2D feature maps → 1D vector

---

### 🔹 5. Fully Connected Layer

* Final classification

---

## 📊 Example Flow

```id="cnn2"
Image (28x28)
   ↓
Conv Layer → Feature Map
   ↓
Pooling → Reduced Size
   ↓
Flatten → Vector
   ↓
Dense Layer → Output
```

---

## ⚙️ Advantages

* Automatic feature extraction
* High accuracy in image tasks
* Fewer parameters than ANN

---

## ⚠️ Disadvantages

* Requires large data
* Computationally expensive
* Needs GPU for faster training

---

## 🛠️ Python Example (Keras)

```python id="cnn3"
from tensorflow.keras.models import Sequential
from tensorflow.keras.layers import Conv2D, MaxPooling2D, Flatten, Dense

model = Sequential()

model.add(Conv2D(32, (3,3), activation='relu', input_shape=(28,28,1)))
model.add(MaxPooling2D(pool_size=(2,2)))

model.add(Flatten())

model.add(Dense(128, activation='relu'))
model.add(Dense(1, activation='sigmoid'))

model.compile(optimizer='adam', loss='binary_crossentropy', metrics=['accuracy'])
```

---

## 🧪 Applications

* Image classification
* Object detection
* Face recognition
* Medical imaging
* Self-driving cars

---

## 🔍 CNN vs ANN

| Feature            | ANN     | CNN       |
| ------------------ | ------- | --------- |
| Data Type          | Tabular | Image     |
| Feature Extraction | Manual  | Automatic |
| Parameters         | High    | Lower     |

---
