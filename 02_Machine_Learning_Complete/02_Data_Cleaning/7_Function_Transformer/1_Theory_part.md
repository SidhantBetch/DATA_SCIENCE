# 🔥 Function Transformer in Machine Learning

---

## 📌 What is Function Transformer?

**Function Transformer** is a utility from **scikit-learn** that allows you to apply **custom functions** to your data during preprocessing.

👉 It is mainly used when built-in transformers are not enough.

---

## 🧠 Why Use Function Transformer?

- Apply custom transformations (log, sqrt, etc.)
- Integrate custom logic into ML pipelines
- Keep preprocessing consistent
- Works well with `Pipeline` and `ColumnTransformer`

---

## 📦 Import Library

```python
from sklearn.preprocessing import FunctionTransformer
```

---

## ⚙️ Basic Syntax
```python
transformer = FunctionTransformer(func, validate=True)
```
Parameters:
- func → Function to apply
- validate → Checks input shape (True/False)

---

### 🔢 Example 1: Log Transformation
```python
import numpy as np
from sklearn.preprocessing import FunctionTransformer

log_transformer = FunctionTransformer(np.log1p)

data_log = log_transformer.fit_transform(data)
```
👉 log1p(x) = log(1 + x) (handles zero values safely)

---

### 🔢 Example 2: Square Root Transformation
```python
sqrt_transformer = FunctionTransformer(np.sqrt)

data_sqrt = sqrt_transformer.fit_transform(data)
```

---

### 🔢 Example 3: Custom Function
```python
def custom_func(x):
    return x * 10

custom_transformer = FunctionTransformer(custom_func)

data_new = custom_transformer.fit_transform(data)
```

---

### 🔄 Example with Pandas DataFrame
```python
import pandas as pd
import numpy as np

df = pd.DataFrame({
    "Income": [1000, 2000, 3000]
})

transformer = FunctionTransformer(np.log1p)

df["Income_log"] = transformer.fit_transform(df[["Income"]])
```

---

## 🔗 Use in Pipeline
```python
from sklearn.pipeline import Pipeline
from sklearn.linear_model import LinearRegression

pipeline = Pipeline([
    ("log_transform", FunctionTransformer(np.log1p)),
    ("model", LinearRegression())
])
```

---
