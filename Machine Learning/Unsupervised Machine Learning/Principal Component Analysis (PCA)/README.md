# Principal Component Analysis (PCA)

Principal Component Analysis is a dimentionality reduction technique used in machine learning and data science. It simplify the complex datasets while preserving the much of orignal information(variance) as much as possible.

PCA (Principal Component Analysis) falls under the category of unsupervised machine learning.

## Why Use PCA?
- To **reduce the number of features** while keeping important patterns.
- To **visualize high-dimensional data** in 2D or 3D.
- To **remove noise and multicollinearity**.
- To **speed up model training** by reducing input features.

## How PCA Works
1. Standardize the data: Center it around mean 0 and scale it.
2. Compute the covariance matrix to understand how features vary with each other.
3. Calculate eigenvectors and eigenvalues of the covariance matrix.
4. Select top 'k' principal components based on highest eigenvalues.
5. Transform the data to the new lower-dimensional space using these components.

## Limitations:
- PCA is **linear** – it can't capture complex non-linear relationships.
- Principal components are **hard to interpret**  because they are combinations of features, not original features themselves.