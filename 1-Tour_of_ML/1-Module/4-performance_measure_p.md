# Performance Measure P

## General Principle
Typically, performance measure **P** is specific to the task **T**

## Classification Tasks

### One possible choice for classification tasks

**Error rate** = N_incorrectly_classified / N_total ⟺ **Accuracy** = N_correctly_classified / N_total = 1 - Error rate

**Error rate = expected 0-1 loss**

### Problem with 0-1 Loss
The main problem with the 0-1 loss is that it is not differentiable. A smooth version is available for probabilistic model: the **log-probability** given by the model to training examples

## Regression Tasks

### Possible choices for regression tasks:

**Mean square loss:**
```
L = (1/N) × Σ(i=1 to N) [(Yi - Ŷi)/Yi]²
```

**L1-loss:**
```
L = (1/N) × Σ(i=1 to N) |Yi - Ŷi|/Yi
```

Where:
- Yi = actual value
- Ŷi = predicted value
- N = total number of examples