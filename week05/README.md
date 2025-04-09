# 📘 Week 5 – Model Selection and Estimation Method Preferences

This week explores how to choose between various panel data estimation methods depending on the structure of the data and assumptions regarding individual effects. We review the theoretical trade-offs between:
- Pooled OLS (HEKK), GLS (GEKK), and Maximum Likelihood Estimation (MLE)
- Fixed Effects (FE), Random Effects (RE), First Differences (FD)
- LSDV and Within Estimator (GIT)
- Model selection under correlated vs uncorrelated individual effects

---

## 📊 Key Questions
- Is the individual effect correlated with regressors?
- Do we want to estimate time-invariant variables?
- How large are N (units) and T (time periods)?

---

## 🧮 Summary of Comparisons

### 1. HEKK vs. GEKK
- If no autocorrelation or heteroskedasticity: same coefficients.
- If present → GEKK is more efficient.
- HEKK is easier to apply.

### 2. GIT vs. GDEKK
- Both provide same results in coefficients.
- GDEKK loses degrees of freedom if N is large.
- GDEKK’s R² may be misleading.

### 3. GIT vs. FD
- When T = 2 → GIT = FD.
- T > 2 and no autocorrelation → GIT preferred.
- If residuals follow random walk → FD is more efficient.

### 4. HEKK vs. GEKK when μᵢ uncorrelated with X_it
- HEKK is unbiased but less efficient than GEKK.
- As ρ → 1, the difference increases.

### 5. GEKK vs. MLE
- Similar results, but MLE maximizes likelihood under normality.
- As sample size increases, both converge.

---

## 🧠 Fixed vs. Random Effects

| Situation | Preferred Model |
|----------|------------------|
| μᵢ correlated with X_it | Fixed Effects or FD |
| μᵢ uncorrelated with X_it | Random Effects |
| Time-invariant variables important | Random Effects |

---

## 📂 Files Included
- `formulas.md`: Summary of model assumptions and conditions