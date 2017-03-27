---
title: basic math for deep learning
date: 2017-03-22 18:53:27
tags:
---

## Calculus

## Linear Algebra
- scalar
- vector
  - row vector
  - column vector
- matrix

$$\begin{bmatrix}1 & 0 & 1 \\ 0 & 1 & 0 \\ 1 & 1 & 0 \\ \end{bmatrix}$$

## Probability and Statistics

## Information theory

### KL-divergence(or relative entropy) ###
> Kullback-Leibler divergence, a.k.a. relative entropy

For discrete probability distribution $P$ and $Q$, the Kullback-Leibler divergence from $Q$ to $p$ is defined to be
$$D_{KL}(P \parallel Q) = \sum_{i}P(i)\log\frac{P(i)}{Q(i)}$$ 

For distributions $P$ and $Q$ of a continuous random variable, the Kullback-Leibler divergence is defined to be the integral:
$$D_{KL}(P\parallel Q) = \int_{-\infty}^{\infty}p(x)\log\frac{p(x)}{q(x)}dx$$

The above form of KL-divergence can also be called as entropy of $P$ relative to $Q$.

### Cross entropy ###
The cross entropy for distribution $p$ and $q$ over a given set is defined as follows
$$H(p, q) = E_q[-\log q] = H(p) + D_{KL}(p \parallel q)$$
Note that often we denote $q$ as the true distribution and $p$ as an "unnatural" probability distribution.
