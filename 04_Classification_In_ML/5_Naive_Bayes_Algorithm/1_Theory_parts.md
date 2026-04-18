# Naive Bayes Algorithm

## 📌 Introduction

Naive Bayes is a **probabilistic machine learning algorithm** based on **Bayes' Theorem**.
It is mainly used for **classification tasks**, especially in:

* Spam detection
* Sentiment analysis
* Text classification
* Recommendation systems

It is called **"naive"** because it assumes that all features are **independent** of each other.

---

## 📖 Bayes' Theorem

The core of Naive Bayes is Bayes' Theorem:

$$
P(A|B) = \frac{P(B|A) \cdot P(A)}{P(B)}
$$

Where:

* ( P(A|B) ) = Posterior probability
* ( P(B|A) ) = Likelihood
* ( P(A) ) = Prior probability
* ( P(B) ) = Evidence

---

## 🧠 How Naive Bayes Works

Naive Bayes calculates the probability of a class given the input features and selects the class with the highest probability.

$$
P(C|X) = P(x_1|C) \cdot P(x_2|C) \cdot ... \cdot P(x_n|C) \cdot P(C)
$$

### Steps:

1. Calculate prior probabilities for each class
2. Calculate likelihood for each feature
3. Multiply all probabilities
4. Choose the class with the highest result

---

## 🧩 Types of Naive Bayes

### 1. Gaussian Naive Bayes

* Used for **continuous data**
* Assumes data follows a **normal distribution**

### 2. Multinomial Naive Bayes

* Used for **text classification**
* Works with **word counts or frequency**

### 3. Bernoulli Naive Bayes

* Used for **binary features**
* Example: word present (1) or not (0)

---

## 📊 Example

Suppose we want to classify whether an email is **Spam or Not Spam**.

Features:

* Contains "offer"
* Contains "free"

Naive Bayes calculates probability for both classes:

$$
P(Spam|Features) \quad vs \quad P(Not\ Spam|Features)
$$

Whichever is higher → Final prediction.

---

## ⚙️ Advantages

* Simple and easy to implement
* Works well with **large datasets**
* Fast and efficient
* Performs well in **text classification**

---

## ⚠️ Disadvantages

* Assumes feature independence (not always true)
* Zero probability problem (handled by **Laplace smoothing**)
* Less accurate compared to complex models

---

## 🛠️ Python Implementation (Scikit-learn)

```python
from sklearn.model_selection import train_test_split
from sklearn.naive_bayes import GaussianNB
from sklearn.metrics import accuracy_score

# Sample data
X = [[1, 0], [1, 1], [0, 1], [0, 0]]
y = [1, 1, 0, 0]

# Split data
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2)

# Model
model = GaussianNB()
model.fit(X_train, y_train)

# Prediction
y_pred = model.predict(X_test)

# Accuracy
print("Accuracy:", accuracy_score(y_test, y_pred))
```

---

## 🧪 Applications

* Email spam filtering
* Document classification
* Medical diagnosis
* Recommendation systems

---

## 📚 Conclusion

Naive Bayes is a **powerful baseline algorithm** for classification tasks.
Despite its simplicity and assumptions, it performs **surprisingly well** in many real-world applications, especially in **text-related problems**.

---

## 🔖 References

* Scikit-learn Documentation
* Machine Learning Textbooks
* Online Tutorials

---
