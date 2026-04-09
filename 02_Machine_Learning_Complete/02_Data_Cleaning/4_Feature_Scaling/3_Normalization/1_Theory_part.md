# Normalization
It is a sacaling technique in which values are dshifted and rescaled so that they end up ranging between 0 and 1. It is also known as Min-Max scaling.

$$
X_{new} = \frac{X_i - min(X)}{max(x) - min(X)}
$$

#### 📌 Where:
- 𝑋 = original value
- $x_{𝑚𝑖𝑛}$ = minimum value
- $𝑋_{𝑚𝑎𝑥}$ = maximum value


## 🧠 Why Do We Need Normalization?

Consider:
```python
Age = 20–60  
Salary = 20,000–1,00,000
```
👉 Salary dominates Age ❌  
👉 Model becomes biased  

✔ Normalization fixes this by bringing all values to the same range

## ⚡ Implementation in Python

Using MinMaxScaler
```python
from sklearn.preprocessing import MinMaxScaler
import pandas as pd

data = pd.DataFrame({
    "Age": [20, 30, 40, 50]
})

scaler = MinMaxScaler()

scaled = scaler.fit_transform(data)

print(scaled)
```

## 🔑 Properties of Normalization
✔ Values range between 0 and 1  
✔ Preserves relative differences  
✔ Sensitive to outliers  

## ⚠️ When to Use Normalization?
✅ Use When:  
✔ Data has different scales  
✔ Using distance-based models like:  
- KNN
- SVM

❌ Avoid When:  
✔ Data has many outliers  
👉 Use Standardization instead  

## 🔥 Normalization vs Standardization
Feature	| Normalization	| Standardization
--------|---------------|----------------
Range	  | 0 to 1	      | No fixed range
Formula	| Min-Max	      | Z-score
Outliers|	Sensitive ❌	| Handles better ✅
Use case	Neural Networks	General ML
