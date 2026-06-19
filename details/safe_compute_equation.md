# The Safe Compute Equation

Standard scaling laws must incorporate safety alignment penalties to accurately model compute-optimal frontiers.

## Formulas
Standard loss targets parameters ($N$) and data tokens ($D$):
$$L(N, D) = \frac{A}{N^\alpha} + \frac{B}{D^\beta} + E$$

Aligned scaling adds a penalty $T_{align}$ for safety and alignment:
$$L_{safe}(N, D) = L(N, D) + T_{align}(N, D)$$

## System Diagram
```mermaid
graph TD
    A[Compute Budget C] --> B[Optimal N & D Selection]
    B --> C{Scaling Model}
    C -->|Un-aligned Model| D[Loss L]
    C -->|Aligned Model| E[Loss L + T_align]
    E --> F[Shifted Compute-Optimal Frontier]
```

## Compute Tax
Shifted Scaling Frontiers. Aligned scaling introduces a penalty parameter that forces models to allocate more resources to parameters or data to maintain capabilities.

[Back to README](../README.md)
