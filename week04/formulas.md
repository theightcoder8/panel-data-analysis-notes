# Week 4 – Random Effects Model: Formulas and Assumptions

## Random Effects (RE) Model:
Y_it = βX_it + μᵢ + u_it
ν_it = μᵢ + u_it

Assumes μᵢ is uncorrelated with X_it

---

## GLS (Generalized Least Squares) Transformation:
θ = 1 - sqrt[σ²_u / (T * σ²_μ + σ²_u)]

Transformation:
(Y_it - θ·Ȳ_i) = β(X_it - θ·X̄_i) + (ν_it - θ·ν̄_i)

---

## RE Assumptions:
- E(μᵢ) = 0
- E(u_it) = 0
- E(μᵢ | X_it) = 0
- E(u_it | μᵢ, X_it) = 0
- Homoskedasticity: Var(u_it) = σ²_u, Var(μᵢ) = σ²_μ

---

## MLE (Maximum Likelihood Estimation):
Based on the joint normality of μᵢ and u_it.  
Log-likelihood is maximized with respect to β, σ²_μ, and σ²_u.

Useful in software such as STATA with:
```stata
xtreg invest mvalue kstock, re mle
```