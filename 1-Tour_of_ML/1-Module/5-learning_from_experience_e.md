# Learning from Experience E

## Core Principle
The performance measure **P** improves with Experience **E** as a result of learning

## Types of Learning from Experience E

```
                           Experience
                               │
        ┌──────────────────────┼──────────────────────┐
        │                     │                      │
        ▼                     ▼                      ▼
┌─────────────┐       ┌─────────────┐       ┌─────────────────┐
│ Supervised  │       │Unsupervised │       │ Reinforcement   │
│             │       │             │       │   Learning      │
└─────────────┘       └─────────────┘       └─────────────────┘
        ▲                     ▲                      ▲
        │                     │                      │
┌─────────────────┐   ┌─────────────────┐   ┌─────────────────┐
│ A "teacher"     │   │ No "teacher":   │   │ There is a      │
│ provides a      │   │ only a dataset  │   │ teacher, but    │
│ training set of │   │ of features     │   │ it gives only   │
│ features/label  │   │ vectors (X_i)   │   │ a partial       │
│ pairs (X_i,C_i) │   │ is provided     │   │ feedback        │
│                 │   │                 │   │ (a reward)      │
└─────────────────┘   └─────────────────┘   └─────────────────┘
```

## Learning Types Summary

| Learning Type | Teacher | Data Provided | Feedback |
|---------------|---------|---------------|----------|
| **Supervised** | Yes | Feature/label pairs (X_i, C_i) | Complete labels |
| **Unsupervised** | No | Feature vectors (X_i) only | No feedback |
| **Reinforcement** | Partial | Experience through interaction | Partial feedback (rewards) |