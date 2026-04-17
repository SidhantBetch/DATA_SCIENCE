
# 🔥 Derived Metrics in Machine Learning

---

## 📌 What are Derived Metrics?

Derived Metrics are performance measures calculated using values from the **Confusion Matrix**:

- True Positive (TP)  
- True Negative (TN)  
- False Positive (FP)  
- False Negative (FN)  

👉 They help evaluate how well a classification model performs.

---

## 📊 Confusion Matrix Reminder

|                | Predicted Positive | Predicted Negative |
|----------------|-------------------|-------------------|
| Actual Positive | TP | FN |
| Actual Negative | FP | TN |

---

# 📈 Important Derived Metrics

---

## 🔹 1️⃣ Accuracy

### 📌 Definition:
Accuracy measures the **overall correctness** of the model.

$$
Accuracy = \frac{(TP + TN)}{(TP + TN + FP + FN)}
$$

---

### 🧠 Meaning:
👉 Out of all predictions, how many are correct  

---

## 🔹 2️⃣ Precision

### 📌 Definition:
Precision measures how many predicted positives are actually correct.

$$
Precision = \frac{TP}{(TP + FP)}
$$

### 🧠 Meaning:
👉 Out of predicted positive cases, how many are truly positive  

---

## 🔹 3️⃣ Recall (Sensitivity)

### 📌 Definition:
Recall measures how many actual positives are correctly predicted.

$$
Recall = \frac{TP}{(TP + FN)}
$$

### 🧠 Meaning:
👉 Out of actual positive cases, how many are detected  

---

## 🔹 4️⃣ Specificity

### 📌 Definition:
Specificity measures how many actual negatives are correctly predicted.

$$
Specificity = \frac{TN }{(TN + FP)}
$$

### 🧠 Meaning:
👉 Out of actual negative cases, how many are correctly identified  

---

## 🔹 5️⃣ F1 Score

### 📌 Definition:
F1 Score is the **harmonic mean of Precision and Recall**.


$$
F1 = \frac{2 * (Precision * Recall)}{(Precision + Recall)}
$$

### 🧠 Meaning:
👉 Balance between Precision and Recall  

---

## 🔹 6️⃣ False Positive Rate (FPR)

### 📌 Definition:
Measures how often negative cases are incorrectly predicted as positive.

$$
FPR = \frac{FP}{(FP + TN)}
$$

---

## 🔹 7️⃣ False Negative Rate (FNR)

### 📌 Definition:
Measures how often positive cases are missed.

$$
FNR = \frac{FN}{(FN + TP)}
$$


---

## 🔹 8️⃣ True Positive Rate (TPR)

### 📌 Definition:
Same as Recall (Sensitivity)

$$
TPR = \frac{TP}{(TP + FN)}
$$

---

## 🔹 9️⃣ True Negative Rate (TNR)

### 📌 Definition:
Same as Specificity

$$
TNR = \frac{TN}{(TN + FP)}
$$

---

# ⚖️ Summary Table

| Metric | Formula | Purpose |
|--------|--------|--------|
| Accuracy | (TP+TN)/(Total) | Overall performance |
| Precision | TP/(TP+FP) | Correct positive prediction |
| Recall | TP/(TP+FN) | Detect actual positives |
| Specificity | TN/(TN+FP) | Detect actual negatives |
| F1 Score | Harmonic mean | Balance precision & recall |
| FPR | FP/(FP+TN) | False alarms |
| FNR | FN/(FN+TP) | Missed cases |

---

## ⚙️ Implementation in Python

```python
from sklearn.metrics import confusion_matrix

cm = confusion_matrix(y_test, y_pred)
print(cm)
```
