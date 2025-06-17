
# 📘 Generalization Error in Regression – Study Notes

This guide explains how machine learning models handle **regression problems** and how we evaluate their performance using the concept of **generalization error**.

---

## 🧠 What is Regression?

**Regression** is when we try to predict a **number** based on input data.  
Examples:
- Predicting a house price from its size and location
- Predicting a stock price based on its history

---

## 🧪 The Regression Model

We assume that:

```
y = f(x) + ε
```

Where:
- `x` = input features
- `f(x)` = the true function (unknown to us)
- `ε` = random noise (real-world randomness)

---

## 📊 Noise Assumptions

```
E[ε] = 0
E[ε²] = σ²
```

- The noise has **zero average** (no bias)
- The **variance** (spread) of the noise is `σ²`

This leads to:

```
E[y] = f(x)
Var(y) = σ²
```

---

## 🎯 Goal: Learn an Approximation of f(x)

Since we don’t know the true function `f(x)`, we try to learn an approximation, `ƒ̂(x)`, using a machine learning model.

### Our Objective:
Minimize the **generalization error**:

```
E[(y - ƒ̂(x))²]
```

This is the **expected squared error** over both training and unseen data.

---

## 🔍 Error Decomposition

The generalization error can be expanded as:

```
E[(y - ƒ̂(x))²] = E[y²] + E[ƒ̂²] - 2E[y ƒ̂]
```

This helps us break the error into parts we can analyze.

---

## 💡 Summary

| Term                      | Meaning                                           |
|---------------------------|---------------------------------------------------|
| `f(x)`                    | The real function generating `y`                 |
| `ƒ̂(x)`                    | The model’s approximation of `f(x)`              |
| `ε`                       | Random noise                                      |
| Generalization Error      | Average prediction error across all data         |
| Goal of Learning          | **Generalize** – perform well on **unseen** data |

---

## 🧠 What is the Bias-Variance Decomposition?

When we train a model to predict a number (e.g., house price), we measure how far off the model is using:

```
E[(y - ƒ̂(x))²]
```

This is the **average squared error** between the true value `y` and our model’s prediction `ƒ̂(x)`.

---

## 🧪 Total Error Breakdown

This total error can be broken down into three parts:

```
Error = (bias)² + variance + noise
```

---

## 🔍 Components Explained

### 🎯 Bias²
**Bias** is how far, on average, your model's predictions are from the truth.

- High bias means the model is too simple and **underfits** the data.
- Example: Using a straight line to fit curved data.

---

### 🌊 Variance
**Variance** measures how much the model’s predictions change depending on the training data.

- High variance means the model is too sensitive and **overfits** the training data.
- Example: A model that memorizes training data but fails on new data.

---

### 🔊 Noise (σ²)
**Noise** is the random variation in the data that **cannot be explained** — it's built into the world.

- Even a perfect model can't eliminate noise.
- Noise is **unavoidable** and **not your model’s fault**.

---

## 🧾 Summary Table

| Component   | What it Means                                                | Can We Reduce It?           |
|-------------|--------------------------------------------------------------|------------------------------|
| Bias        | Systematic error due to overly simple models (underfitting)  | ✅ Yes — use better models   |
| Variance    | Error from overly complex models reacting too much           | ✅ Yes — use regularization  |
| Noise       | Randomness in real-world data                                | ❌ No — it's out of our control |

---

## ⚖️ Why This Matters

- A model that is **too simple** has high bias.
- A model that is **too complex** has high variance.
- The best model **balances both** — a sweet spot where total error is minimized.

---

