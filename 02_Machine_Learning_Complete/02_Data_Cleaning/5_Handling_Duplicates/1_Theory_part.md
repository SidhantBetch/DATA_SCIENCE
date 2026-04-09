# 🔥 Handling Duplicates in Data Science

---

## 📌 What are Duplicates?

Duplicates are rows in a dataset that are **exactly the same or repeated**.

### Example:
Name | Age | City  
-----|-----|------
Ram  | 20  | Delhi  
Shyam| 22  | Mumbai  
Ram  | 20  | Delhi  ← Duplicate  

---

## 🧠 Why Handle Duplicates?

- Creates bias in analysis  
- Increases dataset size unnecessarily  
- Reduces model accuracy  

---

## 🔍 How to Find Duplicates (Pandas)

### 1️⃣ Check Duplicate Rows
```python
dataset.duplicated()
```

### 2️⃣ Count Duplicates
```python
dataset.duplicated().sum()
```

### 3️⃣ View Duplicate Rows
```python
dataset[dataset.duplicated()]
```

### 4️⃣ Check Duplicates Based on Columns
```python
dataset.duplicated(subset=["Name", "Age"])
```

### 5️⃣ Keep Last Occurrence
```python
dataset.duplicated(keep="last")
```

## ⚙️ How to Handle Duplicates

### ✅ 1️⃣ Remove Duplicates
```python
dataset.drop_duplicates(inplace=True)
```

### ✅ 2️⃣ Remove Based on Specific Columns
```python
dataset.drop_duplicates(subset=["Name"], inplace=True)
```

### ✅ 3️⃣ Keep Last Occurrence
```python
dataset.drop_duplicates(keep="last", inplace=True)
```

### ✅ 4️⃣ Remove All Duplicates
```python
dataset.drop_duplicates(keep=False, inplace=True)
```

### ✅ 5️⃣ Reset Index
```python
dataset.reset_index(drop=True, inplace=True)
```

## 🔁 Real Example
```python
import pandas as pd

data = {
    "Name": ["Ram", "Shyam", "Ram"],
    "Age": [20, 22, 20]
}

df = pd.DataFrame(data)

df = df.drop_duplicates()

print(df)
```
