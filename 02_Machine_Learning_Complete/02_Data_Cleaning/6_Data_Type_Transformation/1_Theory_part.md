# 🔥 Data Type Transformation in Data Science

---

## 📌 What is Data Type Transformation?

Data Type Transformation is the process of **converting data from one type to another** to make it suitable for analysis, visualization, and machine learning.

### Examples:
- String → Integer  
- Object → Datetime  
- Float → Integer  

---

## 🧠 Why is it Important?

- Ensures correct calculations  
- Prevents errors in analysis  
- Improves model performance  
- Required for machine learning algorithms  

---

## 🔍 Common Data Types

- **int** → Integer values  
- **float** → Decimal values  
- **object** → String/Text  
- **bool** → True/False  
- **datetime** → Date & Time  

---

## 🔎 Check Data Types

```python
dataset.dtypes
```

## ⚙️ Methods for Data Type Transformation
### 1️⃣ Using astype()
Convert column data type:
```python
dataset["Age"] = dataset["Age"].astype(int)
Convert Multiple Columns
dataset = dataset.astype({
    "Age": "int",
    "Salary": "float"
})
```
 ---

### 2️⃣ Convert String to Numeric
```python
dataset["Salary"] = pd.to_numeric(dataset["Salary"])
Handle Errors
dataset["Salary"] = pd.to_numeric(dataset["Salary"], errors="coerce")
```
👉 Invalid values become NaN

---

### 3️⃣ Convert to Datetime
```python
dataset["Date"] = pd.to_datetime(dataset["Date"])
With Format
dataset["Date"] = pd.to_datetime(dataset["Date"], format="%Y-%m-%d")
```
---

### 4️⃣ Convert to String
```python
dataset["Age"] = dataset["Age"].astype(str)
```
---

### 5️⃣ Convert to Category
```python
dataset["Gender"] = dataset["Gender"].astype("category")
```
👉 Helps reduce memory usage
---

## 🔁 Example
```python
import pandas as pd

data 
= {
    "Age": ["20", "30", "40"],
    "Salary": ["20000", "30000", "40000"]
}

df = pd.DataFrame(data)

df["Age"] = df["Age"].astype(int)
df["Salary"] = pd.to_numeric(df["Salary"])

print(df.dtypes)
```
---

## ⚠️ Common Issues
### ❌ Invalid Data
"abc" → cannot convert to int

#### ✔ Solution:
```python
pd.to_numeric(dataset["col"], errors="coerce")
```
---

### ❌ Missing Values
Conversion may fail if NaN exists

#### ✔ Handle missing values before conversion
---

### ❌ Wrong Date Format
"12-31-2024" vs "2024-12-31"

#### ✔ Use format parameter in to_datetime()
---

## 🧾 Advantages
- Ensures correct data usage
- Improves performance
- Reduces memory usage
---

## ❌ Disadvantages
- Risk of data loss
- Requires careful error handling
