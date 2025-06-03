# Understanding Performance Measures in Machine Learning

This guide introduces performance metrics for evaluating machine learning models, especially for **classification** and **regression** tasks. It includes the key equations, their reasoning, and why they are important.

---

## 1. General Principle

The choice of a **performance measure (P)** depends on the type of **task (T)**.

- For **classification**, we assess how well the model predicts categories.
- For **regression**, we evaluate how close the predicted values are to actual values.

---

## 2. Classification Tasks

Classification involves predicting discrete labels (e.g., spam vs. not spam).

### 📌 Error Rate

**Error rate** = Number of incorrect predictions / Total number of predictions

If 20 out of 100 predictions are wrong, the error rate is 0.20 (or 20%).

**Accuracy** = Number of correct predictions / Total number of predictions

Or equivalently:

**Accuracy** = 1 - Error rate

### 📌 0-1 Loss

This loss assigns:
- 0 for a correct prediction
- 1 for an incorrect prediction

**Expected 0-1 loss** is simply the average error rate over all predictions.

### ❗ Problem with 0-1 Loss

0-1 loss is **not differentiable**, so it's not usable with gradient-based optimization (like gradient descent).  
Instead, we often use **log-loss** or **cross-entropy** when working with probabilistic models.

---

## 3. Regression Tasks

Regression is about predicting continuous numerical values.

We compare the predicted value (Ŷᵢ) to the actual value (Yᵢ) using loss functions.

### 📌 Mean Squared Loss (MSE)

**MSE** = (1 / N) * Σ [ (Yᵢ - Ŷᵢ) / Yᵢ ]²

- N is the total number of examples.
- Squares the error to penalize larger deviations more heavily.
- Smooth and differentiable, so it's useful for optimization.

### 📌 L1 Loss (Mean Absolute Error)

**L1 Loss** = (1 / N) * Σ |(Yᵢ - Ŷᵢ) / Yᵢ|

- Uses absolute differences instead of squared differences.
- More robust to outliers than MSE.

Note: Both use **relative error** (dividing by Yᵢ) to normalize the scale of errors.

---

## 4. Summary Table

| Task           | Measure    | Formula (Plain Text)                                              | Why It Matters                                      |
|----------------|------------|--------------------------------------------------------------------|-----------------------------------------------------|
| Classification | Error Rate | Error rate = Incorrect predictions / Total predictions            | Simple, intuitive metric for classification success |
| Classification | 0-1 Loss   | 0 if prediction is correct; 1 if incorrect                         | Theoretical foundation; not usable for training     |
| Regression     | MSE        | (1 / N) * Σ [ (Yᵢ - Ŷᵢ) / Yᵢ ]²                                    | Penalizes large errors; smooth for optimization     |
| Regression     | L1 Loss    | (1 / N) * Σ |(Yᵢ - Ŷᵢ) / Yᵢ|                                      | Robust to outliers; better sense of typical error   |
