# 📘 Week 2 – Pooled OLS and First Differences in Panel Data

This week's content focuses on the classical Pooled OLS Estimator and the First Difference Estimator (FD) within the context of panel data. We use the **Grunfeld Investment Dataset (1935–1954)**, which contains investment, market value, and capital stock data for 10 major U.S. firms.

---

## 📊 Topics Covered
- Classical (Pooled) OLS Estimation and its assumptions
- First Difference transformation
- Unobserved effects (unit and time effects)
- Problems with ignoring heterogeneity in panel data
- STATA implementation using the `grunfeld` dataset

---

## 🧮 Models

### 1. Pooled OLS (HEKK)
```math
Y_it = β₀ + β₁X₁_it + β₂X₂_it + u_it
```

STATA command:
```stata
. reg invest mvalue kstock
```

---

### 2. First Difference Estimator (FD)
To eliminate individual fixed effects (μᵢ):
```math
ΔY_it = βΔX_it + Δu_it
```

STATA command:
```stata
. gen D.invest = invest - L.invest
. gen D.mvalue = mvalue - L.mvalue
. gen D.kstock = kstock - L.kstock
. reg D.invest D.mvalue D.kstock, noconstant
```

---

## 📂 Files Included
- `formulas.md`: Theoretical formulas and assumptions
- `outputs/stata_output.pdf`: STATA regression results (FD and Pooled OLS)