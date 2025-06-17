# Understanding the Math Behind Performance Measures 


## 🔷 1. Error Rate (Classification)

**Formula:**

```
Error rate = Number of incorrect predictions / Total number of predictions
```

### 🧠 What does it mean?

You're dividing:
- The number of wrong answers your model gave,
- by the total number of questions it was asked.

This gives you a **proportion** (or percentage) of how often the model makes mistakes.

### 🧮 Why this makes sense:

This is like taking a test and figuring out how many questions you got wrong out of the total.  
If you got 2 wrong out of 10, your error rate is 2 ÷ 10 = 0.2 or 20%.

---

## ✅ 2. Accuracy

**Formula:**

```
Accuracy = 1 - Error rate
```

Or:

```
Accuracy = Number of correct predictions / Total number of predictions
```

### 🧠 What does it mean?

This is the flip side of error rate.  
If the model is wrong 20% of the time, then it’s right 80% of the time.

---

## 🎯 3. 0-1 Loss (Classification)

**Idea:**

- If prediction is correct → loss = 0
- If prediction is wrong → loss = 1

Average these losses to get the **expected 0-1 loss**.

### 🧠 Why this works:

This is like keeping score where every mistake costs 1 point and correct guesses cost 0.

---

## 📈 4. Mean Squared Error (MSE) – Regression

**Formula:**

```
MSE = (1 / N) * Σ [ (Yᵢ - Ŷᵢ) / Yᵢ ]²
```

Where:
- Yᵢ = the actual value
- Ŷᵢ = the predicted value
- N = number of examples

### 🧠 What does it mean?

For each prediction:
1. Find the error (Yᵢ - Ŷᵢ)
2. Scale it by dividing by Yᵢ
3. Square the result (to remove negatives and highlight big mistakes)
4. Average all squared values

### 🧮 Why square?

- Makes negative and positive errors both count
- **Big mistakes** hurt more (e.g. 10² = 100, but 2² = 4)

---

## 📏 5. L1 Loss (Mean Absolute Error)

**Formula:**

```
L1 Loss = (1 / N) * Σ |(Yᵢ - Ŷᵢ) / Yᵢ|
```

### 🧠 What does it mean?

Instead of squaring, we just take the **absolute value** (how far off we are).

1. Find the error (Yᵢ - Ŷᵢ)
2. Make it positive (absolute value)
3. Scale it
4. Average all the results

### 🧮 Why use absolute values?

- Treats all errors fairly, big or small
- **More resistant to outliers** (huge errors won’t explode the result)

---

## 🧠 Summary in Real Talk

- **Error rate**: How often are we wrong?
- **Accuracy**: How often are we right?
- **0-1 loss**: A simple way to score classification (1 point for every wrong guess).
- **MSE**: Think of it like yelling at your model for big mistakes — it makes them hurt more.
- **L1 Loss**: More chill — just tells the model how far off it is on average.
