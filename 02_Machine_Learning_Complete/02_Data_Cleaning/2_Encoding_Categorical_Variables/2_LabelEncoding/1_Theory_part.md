# 📌 What is Label Encoding?
Label Encoding is a technique used to convert categorical (text) data into numerical values by assigning each unique category a unique integer.

### 👉 Example:
```
Gender
Male
Female
Male
```
👉 After Label Encoding:
```
Male   → 1
Female → 0
```

## 🧠 Why Do We Use Label Encoding?
Machine learning algorithms like:
- Decision Tree
- Random Forest
👉 require numerical input, not text.

## ⚙️ How Label Encoding Works
1. Identify unique categories
2. Assign integer values starting from 0
3. Replace categories with numbers

### 🧩 Example
Original Data:
```python
Color = ["Red", "Green", "Blue", "Green"]
```
Encoded:

    Red   → 2
    Green → 1
    Blue  → 0
👉 Final:

    [2, 1, 0, 1]

---------------------------------------------------------------------------------------------------------------------------
  
# ⚡ Implementation in Python
Using LabelEncoder
```pyhton
from sklearn.preprocessing import LabelEncoder

le = LabelEncoder()

data = ["Male", "Female", "Male"]

encoded = le.fit_transform(data)

print(encoded)
```

## 🔄 Reverse Transformation (Important ⭐)
```python
original = le.inverse_transform(encoded)
```
👉 Converts numbers back to original labels

## 🧠 Key Characteristics
✔ Converts categories → integers
✔ No increase in number of columns
✔ Simple and fast
✔ Works well with tree-based models

---------------------------------------------------------------------------------------------------------------------------

# ⚠️ Major Problem (Very Important 🚨)
## ❌ Creates False Order
    Low = 0
    Medium = 1
    High = 2
👉 Model assumes:

    High > Medium > Low  ❌ (not always true)
👉 This is called ordinal relationship problem

## 📊 When to Use Label Encoding?
### ✅ Use When:
✔ Data is ordinal (has order)
Examples:
- Education level (High School < Graduate < Postgraduate)
- Size (Small < Medium < Large)

## ❌ Do NOT Use When:
✔ Data is nominal (no order)
Examples:
- Gender
- City
- Country
👉 Use One-Hot Encoding instead

------------------------------------------------------------------------------------------------------------------------------------

# 🔥 Label Encoding vs One-Hot Encoding
Feature	|Label Encoding	|One-Hot Encoding
--------|---------------|------------------
Output	| Single        | column	Multiple columns
Order created |	Yes ❌	| No ✅
Memory	| Low           |	High
Best for|	Ordinal data  |	Nominal data

## ⚠️ Handling New Data (Test Data Problem)
If new category appears:
```python
le.transform(["Unknown"])
```

## 👉 ❌ Error occurs
✔ Solution:
- Use consistent training data
- Or use encoding methods that handle unknowns

## 🧾 Advantages
✔ Simple to implement
✔ Memory efficient
✔ Fast computation

## ❌ Disadvantages
❌ Creates misleading order
❌ Not suitable for nominal data
❌ Cannot handle unseen categories easily

--------------------------------------------------------------------------------------------------------------------------

# 🧾 Real Example (Your Project Style)
```python
from sklearn.preprocessing import LabelEncoder
import pandas as pd

df = pd.DataFrame({
    "Education": ["High School", "Graduate", "Postgraduate"]
})

le = LabelEncoder()

df["Education_encoded"] = le.fit_transform(df["Education"])

print(df)
```
