# Stratification Monte Carlo

This repository contains a project developed by Alban Géron, Arnaud Barrat, Camille Legrée-Hagbarth, and Tristan Fabre. The goal is to approximate the multidimensional integral $\int_{[0, 1]^d} f(u) du$ where $f(u) = \cos\left(2\pi \left(\frac{1}{d} \sum_{i = 1}^d u_i - \frac{1}{2} \right)\right)$, using several numerical integration techniques.

This study could easily be extended to any function of the form $f(u) = \varphi\left(\frac{1}{d} \sum_{i = 1}^d u_i\right)$, where $\varphi : [0, 1] \to \mathbb{R}$ is a continuous function. The integral of such a function arise in many contexts, for instance in physics, machine learning, finance, and numerical analysis.

## Implemented Methods

- **Naive Monte Carlo**: Basic implementation of uniform random sampling over $[0,1]^d$.
- **Quasi-Monte Carlo**: Using randomized permutations to generate low-discrepancy sequences.
- **Haber Estimators (Order 1 and 2)**: Based on the stratification techniques described in [this paper](https://arxiv.org/abs/2210.01554).
- **Importance Sampling**: Using a Gaussian approximation of the integrand based on the Central Limit Theorem (CLT).

## Repository Contents

- `notebook_stratification.ipynb`: A Jupyter notebook demonstrating and comparing the different integration methods.
- `slides.tex`: The LaTeX source code of our presentation slides summarizing the project and our results.
