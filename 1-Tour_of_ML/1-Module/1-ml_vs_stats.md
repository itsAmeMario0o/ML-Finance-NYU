# Differences Between ML and Statistical Modeling

| Aspect | Statistical Modeling | Machine Learning |
|--------|---------------------|------------------|
| **Approach & Philosophy** | Parametric models that try to "explain" the world. The focus is on modeling causality. | Non-parametric models that try to "mimic" the world rather than "explain" it. Often uses correlations as proxies to causality |
| **Methodology** | Deduce relations for observed quantities by parameter estimation for a pre-specified model of the world. | Induce relations between observable quantities, main goal is predictive power. |
| **Data Scale** | Small data (1-100 attributes, 100-1000 examples). | Large data (10-100K attributes, 1K-100M examples). |
| **Scalability** | Scalability is typically not the major concern. | Scalability is often critical in applications. |
| **Mathematical Foundation** | Based on a probabilistic approach. | Some ML methods are not probabilistic (SVM, neural networks, clustering, etc.). |