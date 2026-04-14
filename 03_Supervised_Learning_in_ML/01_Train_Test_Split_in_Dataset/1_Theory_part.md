# 🔥 Train-Test Split in Data Science

---

## 📌 What is Train-Test Split?

Train-Test Split is a technique used to **divide a dataset into two parts**:

- **Training Data** → Used to train the model  
- **Testing Data** → Used to evaluate the model  

---

## 🧠 Why Do We Use Train-Test Split?

- To check how well a model performs on **unseen data**
- To avoid **overfitting**
- To measure **real-world performance**

---

## ⚙️ How It Works

👉 Dataset is divided into:

| Data Type | Purpose |
|----------|--------|
| Training Set | Learn patterns |
| Testing Set | Evaluate model |

---

## 📊 Common Split Ratios

- 70% Train / 30% Test  
- 80% Train / 20% Test ⭐ (Most common)  
- 90% Train / 10% Test  

---

## ⚡ Implementation in Python

**Example:**

```python
import pandas as pd
from sklearn.model_selection import train_test_split

# Sample dataset
X = dataset.drop("Target", axis=1)  # Features
y = dataset["Target"]               # Target variable

# Split data
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)

print(X_train.shape, X_test.shape)
```
