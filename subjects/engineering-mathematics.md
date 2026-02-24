# ∫ Engineering Mathematics

> **Weightage:** ~7% | **Avg Questions:** 4–6 | **Importance:** ⭐⭐⭐⭐

---

## 📊 Overview

Engineering Math in GATE CSE focuses on Calculus, Linear Algebra, Probability, and occasionally complex analysis. Questions are numerical and formula-based. Consistent practice makes this highly scoring.

---

## ✅ Topic-wise Checklist

### 📈 Calculus
- [ ] Limits: evaluation, L'Hôpital's rule
- [ ] Continuity: conditions, types of discontinuity
- [ ] Differentiability: relationship with continuity
- [ ] Derivatives: basic rules (product, quotient, chain)
- [ ] Maxima and minima: first and second derivative tests
- [ ] Taylor series and Maclaurin series
- [ ] Mean value theorem, Rolle's theorem
- [ ] Integration: definite, indefinite, techniques (substitution, parts)
- [ ] Applications: area, volume of revolution
- [ ] Improper integrals
- [ ] Partial derivatives, directional derivatives, gradient
- [ ] Double and triple integrals (overview)
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🔢 Sequences and Series
- [ ] Convergence of sequences
- [ ] Tests for convergence: ratio test, root test, comparison test
- [ ] Power series
- [ ] Taylor and Maclaurin series for standard functions
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 📐 Differential Equations
- [ ] First order ODE: separable, linear, exact, Bernoulli
- [ ] Integrating factor method
- [ ] Second order linear ODE with constant coefficients
- [ ] Homogeneous vs. non-homogeneous
- [ ] Method of undetermined coefficients
- [ ] Variation of parameters (overview)
- [ ] Initial value problems (IVP)
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🔢 Complex Analysis (if in syllabus)
- [ ] Complex numbers: Cartesian and polar forms
- [ ] Euler's formula: e^(iθ) = cos θ + i sin θ
- [ ] Analytic functions: Cauchy-Riemann equations
- [ ] Complex integration, Cauchy integral theorem
- [ ] Residue theorem (overview)
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🖥️ Numerical Methods
- [ ] Bisection method
- [ ] Newton-Raphson method
- [ ] Secant method
- [ ] Fixed-point iteration
- [ ] Numerical integration: Trapezoidal rule, Simpson's rule
- [ ] LU decomposition, Gaussian elimination
- [ ] Gauss-Seidel, Jacobi iteration (linear systems)
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

---

## 📋 Key Formulas

### Calculus
```
d/dx (xⁿ) = nxⁿ⁻¹          d/dx (eˣ) = eˣ
d/dx (ln x) = 1/x            d/dx (sin x) = cos x
d/dx (cos x) = -sin x        d/dx (tan x) = sec²x

Taylor series: f(x) = f(a) + f'(a)(x-a) + f''(a)(x-a)²/2! + ...
sin x = x - x³/3! + x⁵/5! - ...
cos x = 1 - x²/2! + x⁴/4! - ...
eˣ = 1 + x + x²/2! + x³/3! + ...
ln(1+x) = x - x²/2 + x³/3 - ...  |x| ≤ 1
```

### ODE
```
First order linear: dy/dx + P(x)y = Q(x)
Integrating factor: μ = e^(∫P dx)
Solution: y = (1/μ) ∫μQ dx

Second order: ay'' + by' + cy = 0
Characteristic equation: ar² + br + c = 0
If roots r₁ ≠ r₂ (real): y = C₁e^(r₁x) + C₂e^(r₂x)
If roots r₁ = r₂ (repeated): y = (C₁ + C₂x)e^(r₁x)
If roots α ± βi (complex): y = e^(αx)(C₁cos βx + C₂sin βx)
```

### Numerical Methods
```
Newton-Raphson: xₙ₊₁ = xₙ - f(xₙ)/f'(xₙ)
Bisection: xₘ = (a+b)/2; test sign of f(xₘ)
Trapezoidal rule: ∫f dx ≈ h/2 × (f₀ + 2f₁ + 2f₂ + ... + 2fₙ₋₁ + fₙ)
Simpson's 1/3 rule: h/3 × (f₀ + 4f₁ + 2f₂ + 4f₃ + ... + fₙ)  [n even]
```

---

## ⚠️ Common Mistakes

1. **L'Hôpital's rule:** Only applies for 0/0 or ∞/∞ forms
2. **Continuity ≠ differentiability:** Differentiable → continuous, but not vice versa
3. **Integration by parts:** Choose u and dv using LIATE (Log, Inverse, Algebraic, Trig, Exponential)
4. **Convergence tests:** Don't forget to check at endpoints for interval of convergence
5. **Complex roots of ODE:** Use e^(αx) cos/sin, not just cos/sin alone
6. **Newton-Raphson divergence:** Diverges if f'(xₙ) ≈ 0 near root
7. **Simpson's rule:** Requires even number of intervals (odd number of points)
8. **Partial derivatives:** ∂²f/∂x∂y ≠ ∂²f/∂y∂x in general (but equal if continuous second partials)

---

## 📚 Resources

- **Primary:** Higher Engineering Mathematics — B.S. Grewal
- **Video:** NPTEL Engineering Mathematics lectures
- **Calculus:** 3Blue1Brown "Essence of Calculus" for intuition
- **Practice:** GATE Math PYQs (all years)

---

## 📅 PYQ Progress Tracker

- [ ] PYQs 2020–2026 solved
- [ ] PYQs 2015–2019 solved
- [ ] PYQs 2010–2014 solved

---

*Updated: ___ | Revision Count: ___*
