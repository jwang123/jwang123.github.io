---
layout: post
title: Eigen-decomposition
---

## A brief introduction to eigen-decomposition

Eigen-decomposition of a matrix is simply the eigenvectors and eigenvalues of that matrix. A types of matrices used often in statistics are called **positive semi-definite**. These matrices always have eigen-decomposition in a convenient form. Formally, a matrix $A$ is positive semi-definite if it can be obtained as

<p align="center">
$A = XX^{T}$
</p>

In particular, correlation matrices, covariance, and cross-product matrices are all *positive semi-definite matrices*

For our purpose, these type of matrices have several important properties:

- they have real Eigenvalues
- they have orthogonal eigenvectors
- eigenvectors are comprised of real values

Keeping these properties in mind, we now try to understand how eigen-decomposition can be used in finding the linear combination of the variables that yields the largest variance. Given your original data which is presented in a basis, we want to look at the same data from a different points of view. Mathematically, we can do this by a change of basis. For now, I will put the mathematical procedure here, but will add the formalism at a later stage.

Given a $M \times N$ data table denoted $B$, where there are $M$ individuals and $N$ variables,

1. center and standardize (if variables have different units) each variable column so the $i^{th}$ column has $\mu_{i} = 0$ and $\sigma_{i} = 1$
2. find the covaraince matrix $S$ (which will be $M \times M$)
<p align = "center">
$S= \frac{1}{n-1}BB^{T}$
</p>
3. the covariance matrix has the property that the $i$th entry on the diagonal, namely $S_{ii}$ is the variance of the ith variable, and the $ij$th entry of $S$, namely $S_{ij}$, with $i≠j$, is the covariance between the $i$th and $j$th variables
4. there is a theorem in linear algebra that states that any symmetric matrix can be orthogonally diagonalized. Remember that this diagonalization does not change your data, it is simply transforming the data into a new set of coordinate axes so that the output matrix has a canonical form.
5. the output diagonal matrix has column vectors corresponding to orthonormal eigenvectors, and the diagonal values are eigenvalues of each eigenvector
6. simply multiple the loading matrix by the $B$ to get the factor scores, or new coordinates (note: this is only the case because the loading matrix is an **orthogonal matrix**)

### Active vs supplementary

- *active observations* are observations used to compute the PCA
- *supplementary observations* are observations added later using the calculated components
