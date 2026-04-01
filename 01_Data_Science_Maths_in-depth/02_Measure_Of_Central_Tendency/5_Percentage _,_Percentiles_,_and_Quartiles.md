# 💥 Percentage
A percentage is a way of expressing a number as a fraction of 100.

$$
Percentage = \frac{part}{Total} X 100
$$

---------------------------------------------------------------------------------------------------------------------------------------------------------

# 💣 Percentiles
Percentiles are used in statistics to give you a number that describes the value that a given percent of the values are lower than.

$$
percentiles = \frac{(n - Range)}{n} X {100}
$$

---------------------------------------------------------------------------------------------------------------------------------------------------------

# ⛹️‍♂️ Quartukes
Quartiles are values that divide a dataset into 4 equal parts after sorting it.

## 🔢 The 3 Quartiles:
### Q1 (First Quartile)
- 25% of data lies below this
- Also called the lower quartile
### Q2 (Second Quartile)
- 50% of data lies below this
- This is the median
### Q3 (Third Quartile)
- 75% of data lies below this
- Also called the upper quartile
  
### 📈 Visual idea:

    Min —— Q1 —— Q2 —— Q3 —— Max
          25%   50%   75%

---------------------------------------------------------------------------------------------------------------------------------------------------------

# 📊 Outlier
An outlier is a data point that is significantly different from the rest of the values in a dataset.

### 🔍 Simple idea:
#### 👉 It is a value that is too high or too low compared to others.

#### 📌 Example:
Data: 10, 12, 13, 15, 200
##### 👉 200 is an outlier because it is far away from other values.

## 📊 IQR
IQR is a measure of how spread out the middle 50% of data is.

## 📌 Formula:

$$
IQR = 𝑄_3 − 𝑄_1
$$

- Q1 → 25th percentile
- Q3 → 75th percentile
  
## 🔍 Simple idea:
👉 It tells the range of the central data, ignoring extreme values (outliers).

### 📊 Example:
Data (sorted): 10, 12, 14, 16, 18, 20, 22
- Q1 = 12
- Q3 = 20

$$
IQR = 20 − 12 = 8
$$

### 📌 Why IQR is useful:
- Measures data spread (robust to outliers)
- Helps in detecting outliers
- Used in box plots

## 🔎 Outlier rule using IQR:

$Lower Bound = 𝑄_1 − 1.5 × 𝐼𝑄𝑅$  
$Upper Bound = 𝑄_3 + 1.5 × 𝐼𝑄𝑅$


