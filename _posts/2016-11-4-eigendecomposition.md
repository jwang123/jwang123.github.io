---
layout: post
title: Eigen-decomposition
---

## A brief introduction to eigen-decomposition

Eigen-decomposition of a matrix is simply the eigenvectors and eigenvalues of that matrix. A types of matrices used often in statistics are called **positive semi-definite**. These matrices always have eigen-decomposition in a convenient form. Formally, a matrix a is positive semi-definite if it can be obtained as

<p align="center">
$A = XX^{T}$
</p>

In particular, correlation matrices, covariance, and cross-product matrices are all *positive semi-definite matrices*

For our purpose, these type of matrices have several important properties:

- they have real Eigenvalues
- they have orthogonal eigenvectors
- eigenvectors are comprised of real values

Keeping these properties in mind, we know try to understand how eigen-decomposition can be used in finding the linear combination of the variables that yields the largest variance.
