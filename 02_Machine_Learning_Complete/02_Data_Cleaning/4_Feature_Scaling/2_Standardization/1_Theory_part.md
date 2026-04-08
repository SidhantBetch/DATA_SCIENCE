# 🔹 Standardization (Feature Scaling)
Standardization is a technique used to transform data so that it has:
- Mean = 0
- Standard Deviation = 1

It is also called Z-score normalization.

### 📌 Formula
$$
𝑧=\frac{𝑥−𝜇}{𝜎}
$$

Where:
- x = original value
- μ (mu) = mean of data
- σ (sigma) = standard deviation

## 🔹 Why Standardization is Important?
- Ensures all features are on the same scale
- Improves performance of algorithms like:
  - Logistic Regression
  - KNN
  - SVM
  - Gradient Descent
- Prevents features with large values from dominating

### 🔹 Example
Suppose:
- Marks = 80
- Mean = 70
- Std Dev = 10
Then:
$$
𝑧=\frac{80−70}{10}=1
$$
👉 So, the standardized value = 1

## 🔹 In Python (Using sklearn)
```pyhton
from sklearn.preprocessing import StandardScaler

data = [[10], [20], [30], [40]]

scaler = StandardScaler()
scaled_data = scaler.fit_transform(data)

print(scaled_data)
```
