# 🎲 Probability & Statistics

> **Weightage:** ~5% | **Avg Questions:** 3–4 | **Importance:** ⭐⭐⭐⭐

---

## 📊 Overview

Probability is very formula-driven. Bayes' theorem, distributions (Binomial, Poisson, Normal), and expectation/variance questions appear consistently. The DA paper has heavier Statistics weight.

---

## ✅ Topic-wise Checklist

### 🎯 Probability Theory
- [ ] Sample space, events, outcomes
- [ ] Classical, empirical, and axiomatic probability
- [ ] Addition rule: P(A∪B) = P(A) + P(B) - P(A∩B)
- [ ] Multiplication rule: P(A∩B) = P(A) × P(B|A)
- [ ] Independent events: P(A∩B) = P(A) × P(B)
- [ ] Mutually exclusive events: P(A∩B) = 0
- [ ] Conditional probability: P(A|B) = P(A∩B) / P(B)
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🔄 Bayes' Theorem
- [ ] Statement: P(A|B) = P(B|A)P(A) / P(B)
- [ ] Total probability theorem
- [ ] Applications: medical testing, spam filtering
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 📊 Random Variables
- [ ] Discrete vs. continuous random variables
- [ ] Probability Mass Function (PMF)
- [ ] Probability Density Function (PDF)
- [ ] Cumulative Distribution Function (CDF)
- [ ] Expected value (mean): E[X] = Σ x·P(X=x) or ∫ x·f(x)dx
- [ ] Variance: Var(X) = E[X²] - (E[X])²
- [ ] Standard deviation: σ = √Var(X)
- [ ] Joint distributions, marginal distributions
- [ ] Covariance and correlation
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 📈 Common Distributions

**Discrete:**
- [ ] Bernoulli: single trial, success probability p
- [ ] Binomial B(n,p): n trials, P(X=k) = C(n,k)pᵏ(1-p)ⁿ⁻ᵏ
- [ ] Poisson P(λ): rare events, P(X=k) = e⁻λ λᵏ/k!
- [ ] Geometric: trials until first success
- [ ] Negative Binomial (overview)

**Continuous:**
- [ ] Uniform: f(x) = 1/(b-a) on [a,b]
- [ ] Normal (Gaussian): bell curve, N(μ,σ²)
- [ ] Standard Normal: N(0,1), Z-table usage
- [ ] Exponential: memoryless property, f(x) = λe⁻λˣ
- [ ] Chi-squared, t-distribution, F-distribution (overview)
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 📐 Statistics
- [ ] Descriptive statistics: mean, median, mode, range
- [ ] Measures of spread: variance, standard deviation, IQR
- [ ] Sampling and sampling distributions
- [ ] Central Limit Theorem (CLT): sample mean → Normal for large n
- [ ] Confidence intervals (overview)
- [ ] Hypothesis testing: null hypothesis, p-value, Type I/II errors
- [ ] Simple linear regression: least squares
- [ ] Correlation coefficient
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

---

## 📋 Key Formulas

### Probability
```
P(A∪B) = P(A) + P(B) - P(A∩B)
P(A|B) = P(A∩B) / P(B)
Bayes: P(A|B) = P(B|A)·P(A) / P(B) = P(B|A)·P(A) / Σₙ P(B|Aₙ)·P(Aₙ)
```

### Expected Value and Variance
```
E[aX + b] = aE[X] + b
Var(aX + b) = a²Var(X)
Var(X) = E[X²] - (E[X])²
For independent X, Y: Var(X+Y) = Var(X) + Var(Y)
                      E[XY] = E[X]·E[Y]
Covariance: Cov(X,Y) = E[XY] - E[X]E[Y]
Correlation: ρ = Cov(X,Y) / (σₓ σᵧ)
```

### Distributions Summary

| Distribution | Mean | Variance |
|-------------|------|---------|
| Bernoulli(p) | p | p(1-p) |
| Binomial(n,p) | np | np(1-p) |
| Poisson(λ) | λ | λ |
| Geometric(p) | 1/p | (1-p)/p² |
| Uniform(a,b) | (a+b)/2 | (b-a)²/12 |
| Exponential(λ) | 1/λ | 1/λ² |
| Normal(μ,σ²) | μ | σ² |

### Normal Distribution
```
Z = (X - μ) / σ  [standardization]
P(Z < z) from Z-table
68-95-99.7 rule: μ±σ: 68%, μ±2σ: 95%, μ±3σ: 99.7%
```

---

## ⚠️ Common Mistakes

1. **P(A|B) vs. P(B|A):** These are different! Always identify which is given and which to find
2. **Independent vs. mutually exclusive:** Independent: P(A∩B)=P(A)P(B); ME: P(A∩B)=0. Nonzero independent events can't be ME!
3. **Variance of sum:** Var(X+Y) = Var(X)+Var(Y) ONLY for independent X,Y
4. **Conditional ≠ restricted:** P(A|B) is probability of A in the restricted sample space where B occurred
5. **Poisson assumption:** Events must be independent and rate must be constant
6. **E[X²] ≠ (E[X])²:** This confusion leads to wrong variance calculations
7. **Exponential memoryless:** P(X > s+t | X > s) = P(X > t)
8. **Normal standardization:** Always convert to Z before using table

---

## 📚 Resources

- **Primary:** A First Course in Probability — Sheldon Ross
- **Video:** StatQuest with Josh Starmer (YouTube) — intuitive probability/stats
- **Video:** Khan Academy Statistics — basic to intermediate
- **Practice:** GATE Math PYQs + GATE DA PYQs

---

## 📅 PYQ Progress Tracker

- [ ] PYQs 2020–2026 solved
- [ ] PYQs 2015–2019 solved
- [ ] PYQs 2010–2014 solved

---

*Updated: ___ | Revision Count: ___*
