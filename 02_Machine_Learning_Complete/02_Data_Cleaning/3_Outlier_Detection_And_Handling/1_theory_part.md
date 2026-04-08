# 📌 What is an Outlier?
An outlier is a data point that is very different from other values in the dataset.

👉 Example:

    10, 12, 11, 13, 12, 500
➡️ 500 is an outlier

## 🧠 Why Outliers Matter?
Outliers can:
- Distort mean & standard deviation
- Reduce model accuracy
- Mislead analysis
Models like:
- Linear Regression
  are highly sensitive to outliers

-------------------------------------------------------------------------------------------------------------------------
  
## 🔎 Types of Outliers
1. Global Outliers → Extreme compared to whole dataset
2. Contextual Outliers → Abnormal in specific context
3. Collective Outliers → Group behaving abnormally

-------------------------------------------------------------------------------------------------------------------------
  
## 🔍 Methods to Detect Outliers
### 1️⃣ Z-Score Method (Statistical ⚡)
Uses standard deviation

$$
𝑍=\frac{𝑋−𝜇}{𝜎}
$$

### 3️⃣ Box Plot (Visualization 📊)
Using Seaborn
```python
import seaborn as sns
sns.boxplot(x=dataset["Age"])
```
👉 Points outside whiskers = outliers

### 4️⃣ Scatter Plot
```python
import matplotlib.pyplot as plt
plt.scatter(dataset.index, dataset["Age"])
```

### 5️⃣ Percentile Method
```python
lower = dataset["Age"].quantile(0.01)
upper = dataset["Age"].quantile(0.99)
```

-------------------------------------------------------------------------------------------------------------------------
  
## ⚙️ How to Handle Outliers
### 1️⃣ Remove Outliers ❌
```python
dataset = dataset[(dataset["Age"] >= lower) & (dataset["Age"] <= upper)]
```
👉 Use when:
- Data is large
- Outliers are errors

### 2️⃣ Capping (Winsorization) 🔒
Replace extreme values:
```python
dataset["Age"] = np.where(dataset["Age"] > upper, upper, dataset["Age"])
dataset["Age"] = np.where(dataset["Age"] < lower, lower, dataset["Age"])
```

### 3️⃣ Transformation 🔄
Reduce skewness:
```python
import numpy as np
dataset["Age"] = np.log(dataset["Age"])
```

### 4️⃣ Replace with Mean/Median
```python
dataset["Age"] = np.where(
    dataset["Age"] > upper,
    dataset["Age"].median(),
    dataset["Age"]
)
```

### 5️⃣ Use Robust Models 🤖
Some models handle outliers well:
- Decision Tree
- Random Forest


-------------------------------------------------------------------------------------------------------------------------
  
## ⚠️ When NOT to Remove Outliers
### 👉 Important cases:
- Fraud detection
- Medical anomalies
- Rare events
➡️ Outliers may be valuable insights

### 🧾 Advantages of Handling Outliers
✔ Improves model accuracy
✔ Better statistical results
✔ Reduces noise

### ❌ Disadvantages
❌ Risk of losing important data
❌ May remove real-world rare cases
