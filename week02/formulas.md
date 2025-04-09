# Week 2 – Formulas and Assumptions

## 1. Classical (Pooled) OLS Model
Y_it = β₀ + β₁X₁_it + ... + β_kX_k_it + u_it

### Assumptions:
- E(X_it' u_it) = 0
- rank(X'X) = k
- E(u_it u_it') = σ²I

## 2. First Difference Model
ΔY_it = βΔX_it + Δu_it

FD transformation removes μᵢ:
Δν_it = u_it - u_it−1

### Assumptions:
- E(ΔX_it Δu_it) = 0
- rank(ΔX'ΔX) = k
- E(Δu_it Δu_it') = σ²I