# 📌 What is Regularization?

Regularization is a technique used to **reduce overfitting** by adding a **penalty term** to the cost function.

👉 It discourages the model from learning overly complex patterns.

---

## 🧠 Why Do We Need Regularization?

- Prevents overfitting  
- Improves model generalization  
- Controls model complexity  
- Handles multicollinearity  

---

## 🎯 Objective

👉 Minimize: $Cost Function + Penalty Term$

---

## 📊 Types of Regularization

---

### 🔹 1️⃣ L1 Regularization (Lasso Regression)

---

#### 📌 Formula
$$
Cost = Loss + λ * Σ |w|
$$

Where:
- **λ (lambda)** → Regularization parameter  
- **w** → Model coefficients  

---

#### 🧠 Key Idea

👉 Adds **absolute value of coefficients**

---

#### 🔍 Effect on Model

- Shrinks coefficients  
- Some coefficients become **zero**  
👉 Performs **feature selection**

---

#### ✔ Advantages

- Removes irrelevant features  
- Creates sparse model  
- Useful for high-dimensional data  

---

#### ❌ Disadvantages

- Can remove important features  
- Less stable when features are highly correlated  

---

---

### 🔹 2️⃣ L2 Regularization (Ridge Regression)

---

#### 📌 Formula
$$
Cost = Loss + λ * Σ (w²)
$$

---

#### 🧠 Key Idea

👉 Adds **square of coefficients**

---

#### 🔍 Effect on Model

- Shrinks coefficients smoothly  
- No coefficient becomes zero  

---

#### ✔ Advantages

- Reduces overfitting  
- Works well with multicollinearity  
- More stable than L1  

---

#### ❌ Disadvantages

- Does not perform feature selection  
- Keeps all features  

---

---

### ⚖️ L1 vs L2 Comparison

| Feature | L1 (Lasso) | L2 (Ridge) |
|--------|------------|-----------|
| Penalty | Absolute | Squared |
| Feature Selection | Yes | No |
| Coefficients | Can become 0 | Never 0 |
| Model Type | Sparse | Dense |
| Stability | Less stable | More stable |

---

## 📊 Graph Intuition

- L1 → Diamond shape constraint → sharp corners → zero coefficients  
- L2 → Circular constraint → smooth shrinkage  

---

## ⚙️ Choosing Lambda (λ)

- Small λ → less regularization  
- Large λ → more regularization  

👉 Tune using:
- Cross-validation  

---

## ⚡ Implementation in Python

---

### ✔ Lasso (L1)

```python
from sklearn.linear_model import Lasso

model = Lasso(alpha=0.1)
model.fit(X_train, y_train)
```

### ✔ Ridge (L2)
```python
from sklearn.linear_model import Ridge

model = Ridge(alpha=0.1)
model.fit(X_train, y_train)
```
