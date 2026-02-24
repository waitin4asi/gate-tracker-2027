# 📐 Engineering Mathematics

![Weightage](https://img.shields.io/badge/Weightage-4–5%20marks-yellow)
![Priority](https://img.shields.io/badge/Priority-Medium-yellow)

---

## 📋 Topic Checklist

### 🔷 Calculus
- [ ] Limits — definition, L'Hôpital's rule, standard limits
- [ ] Continuity and differentiability
- [ ] Derivatives — chain rule, product rule, quotient rule
- [ ] Derivatives of standard functions
- [ ] Higher-order derivatives
- [ ] Maxima and minima — first/second derivative tests
- [ ] Mean Value Theorem (MVT) — Rolle's, Lagrange's, Cauchy's
- [ ] Taylor's series and Maclaurin's series
- [ ] Partial derivatives and total derivative
- [ ] Gradient, divergence, curl
- [ ] Integration — definite and indefinite
- [ ] Integration techniques: substitution, by parts, partial fractions
- [ ] Improper integrals
- [ ] Double and triple integrals
- [ ] Applications: area, volume, arc length

### 🔷 Differential Equations
- [ ] Ordinary differential equations (ODEs) — order and degree
- [ ] First-order ODEs:
  - [ ] Separable equations
  - [ ] Linear equations (integrating factor)
  - [ ] Exact equations
  - [ ] Bernoulli equations
- [ ] Second-order linear ODEs:
  - [ ] Homogeneous with constant coefficients
  - [ ] Non-homogeneous — method of undetermined coefficients
  - [ ] Variation of parameters
- [ ] Laplace transform and its applications (inverse Laplace)

### 🔷 Sequences and Series
- [ ] Convergence and divergence of sequences
- [ ] Series convergence tests:
  - [ ] nth term test (divergence test)
  - [ ] Comparison test
  - [ ] Integral test
  - [ ] Ratio test
  - [ ] Root test
  - [ ] Alternating series test (Leibniz)
- [ ] Power series and radius of convergence
- [ ] Taylor and Maclaurin series (common functions)
- [ ] Fourier series — basics

---

## ⚡ Key Formulas

### Important Limits
```
lim (x→0) sin(x)/x = 1
lim (x→0) (1-cos x)/x² = 1/2
lim (x→∞) (1 + 1/x)^x = e
lim (x→0) (1+x)^(1/x) = e
lim (x→0) (eˣ-1)/x = 1
lim (x→0) (aˣ-1)/x = ln a
```

### Derivatives
```
d/dx [xⁿ] = nxⁿ⁻¹
d/dx [eˣ] = eˣ
d/dx [aˣ] = aˣ ln a
d/dx [ln x] = 1/x
d/dx [sin x] = cos x
d/dx [cos x] = -sin x
d/dx [tan x] = sec²x
d/dx [sin⁻¹x] = 1/√(1-x²)
d/dx [tan⁻¹x] = 1/(1+x²)
```

### Taylor/Maclaurin Series
```
eˣ = 1 + x + x²/2! + x³/3! + ...
sin x = x - x³/3! + x⁵/5! - ...
cos x = 1 - x²/2! + x⁴/4! - ...
ln(1+x) = x - x²/2 + x³/3 - ...  (|x| ≤ 1)
(1+x)^n = 1 + nx + n(n-1)x²/2! + ...  (|x| < 1)
```

### Integration
```
∫ xⁿ dx = xⁿ⁺¹/(n+1) + C  (n ≠ -1)
∫ 1/x dx = ln|x| + C
∫ eˣ dx = eˣ + C
∫ sin x dx = -cos x + C
∫ cos x dx = sin x + C
∫ sec²x dx = tan x + C
Integration by parts: ∫u dv = uv - ∫v du
```

### First-Order ODE — Integrating Factor
```
dy/dx + P(x)y = Q(x)
Integrating factor: μ(x) = e^(∫P(x)dx)
Solution: y·μ = ∫Q(x)·μ dx
```

### Second-Order Homogeneous ODE
```
ay'' + by' + cy = 0
Characteristic equation: ar² + br + c = 0
  Distinct real roots r₁, r₂: y = C₁e^(r₁x) + C₂e^(r₂x)
  Repeated root r: y = (C₁ + C₂x)e^(rx)
  Complex roots α ± βi: y = e^(αx)[C₁cos(βx) + C₂sin(βx)]
```

### Laplace Transform
```
L{1} = 1/s
L{t^n} = n!/s^(n+1)
L{e^(at)} = 1/(s-a)
L{sin(at)} = a/(s²+a²)
L{cos(at)} = s/(s²+a²)
L{f'(t)} = sF(s) - f(0)
L{f''(t)} = s²F(s) - sf(0) - f'(0)
```

---

## ❌ Common Mistakes

| Mistake | Correct Understanding |
|---|---|
| L'Hôpital applies everywhere | Only applies to 0/0 or ∞/∞ indeterminate forms |
| Integration by parts ILATE rule | ILATE: Inverse trig, Logarithmic, Algebraic, Trig, Exponential |
| Ratio test: ratio = 1 → converges | Ratio = 1 is inconclusive; need another test |
| Partial derivative ignores other vars | Other variables treated as constants |
| All power series converge everywhere | Check radius of convergence R first |

---

## 📊 PYQ Frequency Analysis (2015–2024)

| Topic | Frequency | Marks Range |
|---|:---:|:---:|
| Integration (definite/indefinite) | High | 1–2 |
| Differential equations | High | 1–2 |
| Limits and continuity | Medium | 1 |
| Series convergence | Medium | 1 |
| Laplace transforms | Medium | 1 |

---

## 🎯 Confidence Tracker

| Topic | Confidence | Last Revised |
|---|:---:|---|
| Limits & Derivatives | ☐ Low / ☐ Med / ☐ High | |
| Integration | ☐ Low / ☐ Med / ☐ High | |
| Differential Equations | ☐ Low / ☐ Med / ☐ High | |
| Series | ☐ Low / ☐ Med / ☐ High | |
| Laplace Transforms | ☐ Low / ☐ Med / ☐ High | |
