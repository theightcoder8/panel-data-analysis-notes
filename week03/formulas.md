# Week 3 – Fixed Effects Formulas and Assumptions

## Fixed Effects Model:
Y_it = βX_it + μᵢ + u_it

Within transformation:
Y_it - Ȳ_i = β(X_it - X̄_i) + (u_it - ū_i)

Estimator:
β̂ = (ΣΣ(x_it - x̄_i)'(x_it - x̄_i))⁻¹ × (ΣΣ(x_it - x̄_i)'(y_it - ȳ_i))

---

## LSDV Specification:
Y_it = βX_it + D_i + u_it

Where D_i are dummy variables for each unit (except reference group)

---

## Assumptions:
- SE1: E(μᵢ | X_it) ≠ 0 (fixed effects are correlated with regressors)
- SE2: Full rank of X after transformation
- SE3: Error term u_it is i.i.d. with zero mean and constant variance