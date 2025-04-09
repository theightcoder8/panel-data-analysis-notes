# 📘 Week 3 – Fixed Effects Model

This week, we focus on the **Fixed Effects (FE) Model**, a key method used when unobserved unit-specific effects (μᵢ) are correlated with explanatory variables. We introduce two main estimation techniques:
- The **Within Estimator** (Grup İçi Tahminci)
- The **Least Squares Dummy Variable (LSDV)** Estimator

The **Grunfeld Investment Dataset** is used for implementation.

---

## 🧮 Theoretical Model

### Fixed Effects (One-way) Panel Model
```
Y_it = βX_it + μᵢ + u_it
```
- μᵢ: Unobserved time-invariant individual effect
- u_it: Idiosyncratic error term

---

### 1. Within Estimator (Grup İçi Tahminci)
Removes μᵢ by transforming variables using time-demeaning:
```
Y_it - Ȳ_i = β(X_it - X̄_i) + (u_it - ū_i)
```

STATA:
```stata
xtreg invest mvalue kstock, fe
```

---

### 2. LSDV – Least Squares Dummy Variable
Adds (N-1) dummies to capture unit-specific intercepts:
```
Y_it = βX_it + D_i + u_it
```

STATA:
```stata
reg invest mvalue kstock i.company
```

---

## 📂 Files Included
- `formulas.md`: Assumptions and matrix form of FE
- `outputs/stata_output.pdf`: STATA results for within and LSDV estimators
