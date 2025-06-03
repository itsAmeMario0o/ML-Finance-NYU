# 📚 Machine Learning Landscape 

## 🧠 What is Machine Learning?

**Machine Learning (ML)** is about teaching computers to **learn from data**.  
Instead of writing every rule by hand, we show examples, and the machine figures out patterns or rules.

---

## 🗺️ Types of Machine Learning

The image breaks ML into **three main categories**:

1. **Supervised Learning**
2. **Unsupervised Learning**
3. **Reinforcement Learning**

---

## 1. 🧭 Supervised Learning – "Learn from labeled data"

You give the machine both **inputs and the correct outputs** (like questions and answers).

### 🔹 Regression

- Predicts a **number** (e.g., temperature, price).
- Function: `f: Rⁿ → R`
- Input: Multiple values (Rⁿ), Output: One number (R)
- Example: Predict a house price from its size and location.

### 🔹 Classification

- Predicts a **category or label** (e.g., spam or not spam).
- Function: `f: Rⁿ → {1, ..., k}`
- k = number of possible classes
- Example: Is this email spam?

---

## 2. 🧩 Unsupervised Learning – "Find patterns with no labels"

You give the machine only the inputs — no correct answers.  
It finds structure or patterns on its own.

### 🔹 Clustering

- Goal: Group similar things together.
- Function: `f: Rⁿ → {1, ..., k}`
- Example: Group customers based on shopping behavior.

### 🔹 Representation Learning

- Goal: Transform raw data into simpler, more useful features.
- Function: `f: Rⁿ → Rᵏ`
- Example: Compress images or reduce dimensions of text.

---

## 3. 🎮 Reinforcement Learning – "Learn from rewards and actions"

The machine **interacts with an environment**, takes actions, and learns from the results.

### 🔹 Policy Learning

- Learns **which actions** to take to maximize reward.
- Function: `f: Rⁿ → Rᵃ` (outputs actions)
- Given: Tuples like (state, action, next state, reward)
- Example: Learn to play a game by trying different moves.

### 🔹 Inverse Reinforcement Learning (IRL)

- Learns **what the reward function is**, by observing behavior.
- Goal: Explain why someone behaves a certain way.
- Example: Learn to drive by watching how a human drives.

---

## ✍️ Summary Table

| Learning Type           | What You Provide         | What It Learns                      | Real-Life Analogy                   |
|-------------------------|--------------------------|-------------------------------------|-------------------------------------|
| Supervised Learning     | Inputs + Correct Outputs | Predict numbers or categories       | Studying with an answer key         |
| Unsupervised Learning   | Inputs only              | Find structure or useful features   | Grouping photos by similarity       |
| Reinforcement Learning  | Inputs + Feedback        | Learn actions from rewards          | Training a dog with treats          |
