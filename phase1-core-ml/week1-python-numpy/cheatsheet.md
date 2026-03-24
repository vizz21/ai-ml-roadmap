# Phase 1 Cheat Sheet

## NumPy
- Mean: `np.sum(arr) / len(arr)`
- Variance: `sum((x - mean)²) / (n-1)`
- Std: `sqrt(variance)`
- Covariance: `sum((x - mean_x)(y - mean_y)) / (n-1)`
- Correlation: `cov(x,y) / (std_x * std_y)`
- Linear Regression slope: `cov(x,y) / var(x)`
- Linear Regression intercept: `mean(y) - m * mean(x)`

## Key NumPy operations
- Slicing last column: `a[:, -1]`
- Boolean mask: `a[a > 10]`
- Broadcasting: (3,) treated as (1,3)
- Normalisation: `(a - mean) / std`

## Python
- Generator: `yield` keyword
- Context manager: `__enter__`, `__exit__`
- Decorator pattern: `wrapper(*args, **kwargs)`