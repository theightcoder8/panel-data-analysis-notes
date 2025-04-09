# Week 5 – Model Selection: Formulas and Assumptions

## 1. Pooled OLS (HEKK)
Y_it = βX_it + u_it  
Assumes no individual effect μᵢ or assumes it's part of u_it

## 2. GEKK (GLS)
- Deals with heteroskedasticity and serial correlation
- Efficient when classical assumptions are violated

## 3. Maximum Likelihood (MLE)
- Estimates based on likelihood function
- Consistent and efficient under normality

## 4. Fixed Effects (FE)
Y_it = βX_it + μᵢ + u_it  
μᵢ is correlated with X_it → use Within transformation or LSDV

## 5. Random Effects (RE)
Y_it = βX_it + μᵢ + u_it  
μᵢ is uncorrelated with X_it → use GLS transformation with theta

## 6. First Difference (FD)
ΔY_it = βΔX_it + Δu_it  
Removes μᵢ through differencing

## 7. LSDV (Least Squares Dummy Variable)
Y_it = βX_it + dummies + u_it  
Can estimate μᵢ directly but loses degrees of freedom