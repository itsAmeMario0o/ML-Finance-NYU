# Mitchell's Definition of Machine Learning

## Quote
> "A computer program is said to learn from experience E with respect to some class of tasks T and performance measure P, if its performance at tasks in T, as measured by P, improves with experience E." (Mitchell, 1997)

## Machine Learning Framework

```
                           ML Algorithm
                               |
        ┌──────────────────────┼──────────────────────┐
        │                      │                      │
        ▼                      ▼                      ▼
   ┌─────────┐         ┌─────────────┐        ┌──────────────┐
   │ Task T  │◄────────┤ Experience E│────────┤ Performance  │
   │         │         │             │        │ Measure P    │
   └─────────┘         └─────────────┘        └──────────────┘
        │                     ▲                      ▲
        │                     │                      │
        └─────────────────────┼──────────────────────┘
                              │
                    ┌─────────────────┐
                    │   Environment   │
                    │  (or Dataset)   │
                    └─────────────────┘
```

## Key Components

| Component | Description |
|-----------|-------------|
| **Task T** | The class of tasks the program needs to perform |
| **Experience E** | The data/examples the program learns from |
| **Performance Measure P** | The metric used to evaluate how well the program performs |
| **ML Algorithm** | The method that connects T, E, and P to enable learning |
| **Environment/Dataset** | The source of experience and performance feedback |

## Learning Process
The ML algorithm uses **Experience E** to improve performance on **Task T** as measured by **Performance Measure P**. The environment provides both the experience data and the feedback for measuring performance.