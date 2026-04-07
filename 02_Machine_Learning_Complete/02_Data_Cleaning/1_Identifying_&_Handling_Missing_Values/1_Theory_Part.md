# Data Cleaning
Data cleaning is the process of preparing data for analysis / ML(machine Learning) / DL(Deep Learning) by removing or modifying data that is incorrect, incomplete, irrelevant, duplicated, or improperly formatted.  

## Steps to Data Cleaning
- Handling Missing Data
- Outlier Detection and Handling
- Data Scaling and Transformation
- Encoding Categorical Variables
- Handling Duplicates
- Dealing with Inconsistent Data

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# 🔍 What is a Missing Value?
A missing value in data science is a data point that is not stored or recorded in a dataset. In Python (especially with Pandas), missing values are usually represented as:
- NaN (Not a Number)
- None
- NaT (for datetime)

#### 👉 Example:
```python
Name     Age     Gender
Ram      20      Male
Shyam    NaN     Male
Rita     22      None
```

Here, Age and Gender have missing values.

## 🧠 Why Missing Values Matter?
- Can reduce model accuracy
- Cause errors in calculations
- Bias results if not handled properly

## 🔎 How to Find Missing Values (All Methods)
### 1️⃣ isnull() Method  
Checks where values are missing.
```python
dataset.isnull()
```
👉 Output: True where value is missing

### 2️⃣ isnull().sum() (Most Used ✅)  
Counts missing values column-wise.
```python
dataset.isnull().sum()
```
#### 👉 Example Output:
```
Name      0
Age       2
Gender    1
```

### 3️⃣ notnull() Method
Opposite of isnull() (finds non-missing values)
```python
dataset.notnull()
```

### 4️⃣ isna() Method
Same as isnull() (just another name)
```python
dataset.isna().sum()
```

### 5️⃣ info() Method (Quick Overview ⚡)
Gives summary including non-null counts
```pyhton
dataset.info()
```

👉 Shows:
- Total entries
- Non-null values
- Data types
  
### 6️⃣ Check Missing in Specific Column
```python
dataset["Gender"].isnull().sum()
```

### 7️⃣ Check Rows with Missing Values
```pyhton
dataset[dataset.isnull().any(axis=1)]
```
👉 Shows rows where any column has missing values

### 8️⃣ Check Total Missing Values in Dataset
```python
dataset.isnull().sum().sum()
```
👉 Gives total missing values

### 9️⃣ Percentage of Missing Values
```python
(dataset.isnull().sum() / len(dataset)) * 100
```
👉 Helps understand how serious the issue is

### 🔟 Using Heatmap (Visualization 📊)
With Seaborn:
```python
import seaborn as sns
sns.heatmap(dataset.isnull())
```
👉 Missing values will be highlighted visually

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# ⚙️ Handle Missing Values

## ✔️ Fill with Mean
```python
dataset["Age"].fillna(dataset["Age"].mean(), inplace=True)
```
## ✔️ Fill with Mode (Categorical)
```python
dataset["Gender"].fillna(dataset["Gender"].mode()[0], inplace=True)
```
## ✔️ Drop Missing Values
```python
dataset.dropna(inplace=True)
```
