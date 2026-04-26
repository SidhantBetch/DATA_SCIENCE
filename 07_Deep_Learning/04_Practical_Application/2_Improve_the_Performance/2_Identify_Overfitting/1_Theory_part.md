# 📌 Identifying Overfitting in Neural Networks

**Overfitting** occurs when a neural network learns the training data too well, including noise and patterns that do not generalize to new data.

👉 Result:

* High accuracy on training data
* Poor performance on test/validation data

---

## 🔍 Signs of Overfitting

### 1. Training vs Validation Accuracy

* Training accuracy → very high
* Validation accuracy → low

👉 Large gap indicates overfitting

---

### 2. Training vs Validation Loss

* Training loss → very low
* Validation loss → high or increasing

---

### 3. Learning Curve Pattern

```id="overfit1"
Epoch →
Training Loss     ↓↓↓↓↓
Validation Loss   ↓ then ↑ (starts increasing)
```

👉 Validation loss increases after some epochs

---

### 4. Performance on New Data

* Works well on training set
* Performs poorly on unseen/test data

---

## 📊 Example

| Metric              | Value |
| ------------------- | ----- |
| Training Accuracy   | 95%   |
| Validation Accuracy | 70%   |

👉 Clear sign of overfitting

---

## 🛠️ How to Check in Code (Keras)

```python id="overfit2"
history = model.fit(
    X_train, y_train,
    validation_split=0.2,
    epochs=50
)

import matplotlib.pyplot as plt

# Plot accuracy
plt.plot(history.history['accuracy'], label='train')
plt.plot(history.history['val_accuracy'], label='validation')
plt.legend()
plt.show()
```

---

## ⚠️ Common Causes

* Too complex model
* Too many layers/neurons
* Small dataset
* Too many training epochs

---

## ✅ How to Confirm Overfitting

✔ Compare:

* Train vs Validation accuracy
* Train vs Validation loss

✔ Check:

* Learning curves
* Test performance

---

## 🔧 Quick Fixes

* Add Dropout
* Use regularization (L1/L2)
* Early stopping
* More data
* Reduce model complexity

---
