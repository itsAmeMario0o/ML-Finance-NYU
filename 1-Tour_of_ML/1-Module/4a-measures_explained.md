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

\[
\text{Error rate} = \frac{\text{Number of incorrect predictions}}{\text{Total number of predictions}}
\]

- If 20 out of 100 predictions are wrong, the error rate is 20%.
- The complement is **accuracy**:

\[
\text{Accuracy} = \frac{\text{Number of correct predictions}}{\text{Total predictions}} = 1 - \text{Error rate}
\]

### 📌 0-1 Loss

This loss assigns:
- `0` for a correct prediction
- `1` for an incorrect prediction

\[
\text{Expected 0-1 loss} = \text{Average error rate}
\]

### ❗ Problem with 0-1 Loss

- It is **not differentiable**, making it unsuitable for optimization algorithms like gradient descent.
- Instead, we often use differentiable alternatives like **log-loss** or **cross-entropy** in probabilistic models.

---

## 3. Regression Tasks

Regression is about predicting continuous numerical values.

We evaluate how close the predicted value \( \hat{Y}_i \) is to the true value \( Y_i \).

### 📌 Mean Squared Loss (MSE)

\[
L = \frac{1}{N} \sum_{i=1}^{N} \left( \frac{Y_i - \hat{Y}_i}{Y_i} \right)^2
\]

- Squares the difference to emphasize larger errors.
- Smooth and differentiable—good for training.

### 📌 L1 Loss (Mean Absolute Error)

\[
L = \frac{1}{N} \sum_{i=1}^{N} \left| \frac{Y_i - \hat{Y}_i}{Y_i} \right|
\]

- Takes the absolute value of the difference.
- More robust to outliers compared to squared loss.

> 🔍 Both formulas use **relative error**, dividing by \( Y_i \), to account for the scale of the true value.

---

## 4. Summary Table

| Task           | Measure    | Formula                                                                 | Why It Matters |
|----------------|------------|-------------------------------------------------------------------------|----------------|
| Classification | Error Rate | \( \frac{N_{\text{wrong}}}{N} \)                                        | Simple, intuitive metric for classification success |
| Classification | 0-1 Loss   | 0 if correct, 1 if wrong                                                | Theoretical foundation for accuracy; not usable for gradient-based training |
| Regression     | MSE        | \( \frac{1}{N} \sum \left( \frac{Y - \hat{Y}}{Y} \right)^2 \)            | Penalizes larger errors more; smooth for optimization |
| Regression     | L1 Loss    | \( \frac{1}{N} \sum \left| \frac{Y - \hat{Y}}{Y} \right| \)              | Robust to outliers; gives a clearer view of typical error |
