# 📘 Week 4 – Random Effects, GEKK and MLE Estimators

This week introduces the **Random Effects (RE) Model** in panel data. Unlike Fixed Effects, the RE model assumes the individual-specific effect (μᵢ) is random and uncorrelated with explanatory variables. We also cover the Generalized Least Squares (GLS) method and Maximum Likelihood Estimation (MLE) for RE models.

---

## 🧠 Key Topics
- Random Effects model structure
- Theta (θ) transformation logic
- GLS estimation with error component model
- Maximum Likelihood Estimation (MLE)
- STATA implementation: `xtreg, re theta` and `xtreg, mle`

---

## 🔢 Core Equations

### Random Effects Model
```
Y_it = βX_it + μᵢ + u_it
```
where:  
- μᵢ ~ N(0, σ²_μ)  
- u_it ~ N(0, σ²_u)

---

### GLS Transformation (Theta):
```
θ = 1 - [σ²_u / (T * σ²_μ + σ²_u)]^0.5
```

Transformed equation:
```
(Y_it - θ·Ȳ_i) = β(X_it - θ·X̄_i) + (ν_it - θ·ν̄_i)
```

---

### Maximum Likelihood Estimation (MLE)

When μᵢ and u_it are both normally distributed, the log-likelihood function can be derived and optimized to estimate β, σ²_μ, and σ²_u.

---

## 📂 Included Files
- `formulas.md`: Key RE assumptions and math
- `outputs/stata_output.pdf`: STATA results for RE (GLS and MLE)