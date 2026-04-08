# 📌 What is Ordinal Encoding?
Ordinal Encoding is a technique used to convert categorical data into numerical values based on a meaningful order (ranking).

👉 Example:

    Education Level
    High School < Graduate < Postgraduate

👉 Encoding:

    High School   → 0
    Graduate      → 1
    Postgraduate  → 2
✔ Here, numbers represent order, not just labels

## 🧠 Why Use Ordinal Encoding?
Some machine learning models need numeric input, and when data has natural order, ordinal encoding preserves that relationship.

Used in models like:
- Linear Regression
- Logistic Regression

## ⚙️ How It Works
1. Identify categories with order
2. Assign numbers according to ranking
3. Replace original values with numbers

## 🧩 Example
Original Data:
```pyhton
Size = ["Small", "Medium", "Large", "Medium"]
```
Encoding:

    Small  → 0
    Medium → 1
    Large  → 2
👉 Final:

    [0, 1, 2, 1]

##⚡ Implementation in Python
Using OrdinalEncoder
```python
from sklearn.preprocessing import OrdinalEncoder
import pandas as pd

df = pd.DataFrame({
    "Size": ["Small", "Medium", "Large", "Medium"]
})

encoder = OrdinalEncoder(categories=[["Small", "Medium", "Large"]])

df["Size_encoded"] = encoder.fit_transform(df[["Size"]])

print(df)
```

## 🔑 Important Parameter
✔ categories  
Defines the correct order:
```python
categories=[["Low", "Medium", "High"]]
```
👉 Without this, encoder may assign wrong order automatically

## ⚠️ Key Difference from Label Encoding
Feature	        | Label Encoding	| Ordinal Encoding
----------------|-----------------|--------------------
Order awareness	| ❌ No	        | ✅ Yes
Control over order|	❌ No        |	✅ Yes
Use case	      | Any data (risky) |	Ordered data only


## 🚨 When to Use Ordinal Encoding
✅ Use When:  
✔ Data has natural order

Examples:
- Education level
- Size (S, M, L)
- Ratings (Bad < Average < Good)

## ❌ Do NOT Use When:
✔ Data has no order

Examples:
- Gender
- City
- Country
👉 Use One-Hot Encoding instead

## ⚠️ Common Mistakes
### ❌ Wrong Order Assignment
```python
rdinalEncoder(categories=[["Large", "Small", "Medium"]])
```
👉 This creates incorrect ranking → bad model performance

### ❌ Using Without Specifying Order
```python
OrdinalEncoder()
```
👉 May assign order alphabetically ❌

## 🔄 Handling Unknown Values
```python
encoder = OrdinalEncoder(handle_unknown="use_encoded_value", unknown_value=-1)
```
👉 New category → encoded as -1

## 🧾 Advantages
✔ Keeps order information  
✔ Uses only one column  
✔ Efficient for ordinal data  

## ❌ Disadvantages
❌ Wrong order = wrong results  
❌ Not suitable for nominal data  
❌ Can mislead some models  
