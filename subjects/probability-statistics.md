# 🎲 Probability & Statistics

![Weightage](https://img.shields.io/badge/Weightage-3–4%20marks-yellow)
![Priority](https://img.shields.io/badge/Priority-Medium-yellow)

---

## 📋 Topic Checklist

### 🔷 Basic Probability
- [ ] Sample space, events, probability axioms (Kolmogorov)
- [ ] Classical probability — equally likely outcomes
- [ ] Mutually exclusive vs independent events
- [ ] Addition rule: P(A∪B) = P(A) + P(B) − P(A∩B)
- [ ] Multiplication rule: P(A∩B) = P(A) × P(B|A)
- [ ] Complement rule: P(A') = 1 − P(A)
- [ ] Conditional probability: P(A|B) = P(A∩B)/P(B)
- [ ] Bayes' Theorem and Law of Total Probability
- [ ] Independence: P(A∩B) = P(A) × P(B)

### 🔷 Random Variables
- [ ] Discrete random variables — PMF (Probability Mass Function)
- [ ] Continuous random variables — PDF (Probability Density Function)
- [ ] CDF (Cumulative Distribution Function)
- [ ] Expected value (mean): E[X]
- [ ] Variance: Var(X) = E[X²] − (E[X])²
- [ ] Standard deviation: σ = √Var(X)
- [ ] Moments and moment generating functions (MGF)
- [ ] Joint probability distributions (discrete)
- [ ] Marginal and conditional distributions
- [ ] Covariance and correlation coefficient

### 🔷 Discrete Probability Distributions
- [ ] Bernoulli distribution — single trial
- [ ] Binomial distribution B(n,p) — n independent trials
- [ ] Geometric distribution — trials until first success
- [ ] Negative binomial distribution
- [ ] Poisson distribution — events in fixed interval
- [ ] Hypergeometric distribution — without replacement

### 🔷 Continuous Probability Distributions
- [ ] Uniform distribution U(a,b)
- [ ] Normal (Gaussian) distribution N(μ,σ²)
- [ ] Standard normal distribution Z = (X−μ)/σ
- [ ] Exponential distribution — memoryless property
- [ ] Gamma distribution
- [ ] Chi-squared distribution (basics)

### 🔷 Statistics
- [ ] Descriptive statistics: mean, median, mode, range
- [ ] Measures of spread: variance, standard deviation, IQR
- [ ] Population vs sample statistics
- [ ] Sampling distributions
- [ ] Central Limit Theorem (CLT)
- [ ] Point estimation — properties: unbiased, consistent, efficient
- [ ] Confidence intervals
- [ ] Hypothesis testing — Type I and Type II errors
- [ ] p-value and significance level
- [ ] t-test, chi-squared test (conceptual)

### 🔷 Random Processes (Basics)
- [ ] Markov chains — transition matrix, steady-state distribution
- [ ] Stationary distribution

---

## ⚡ Key Formulas

### Probability Rules
```
P(A∪B) = P(A) + P(B) − P(A∩B)
P(A|B) = P(A∩B) / P(B)
Bayes: P(A|B) = P(B|A)·P(A) / P(B)
Total probability: P(B) = Σ P(B|Aᵢ)·P(Aᵢ)
```

### Expected Value and Variance
```
E[X] = Σ x·P(X=x)          (discrete)
E[X] = ∫ x·f(x) dx         (continuous)
E[aX+b] = aE[X]+b
Var(X) = E[X²] − (E[X])²
Var(aX+b) = a²·Var(X)
Cov(X,Y) = E[XY] − E[X]·E[Y]
Correlation: ρ = Cov(X,Y) / (σ_X · σ_Y)
```

### Key Distributions
| Distribution | PMF / PDF | Mean | Variance |
|---|---|:---:|:---:|
| Bernoulli(p) | P(X=1)=p, P(X=0)=1-p | p | p(1-p) |
| Binomial(n,p) | C(n,k)p^k(1-p)^(n-k) | np | np(1-p) |
| Geometric(p) | (1-p)^(k-1)p | 1/p | (1-p)/p² |
| Poisson(λ) | e^(-λ)λ^k/k! | λ | λ |
| Uniform(a,b) | 1/(b-a) | (a+b)/2 | (b-a)²/12 |
| Exponential(λ) | λe^(-λx) | 1/λ | 1/λ² |
| Normal(μ,σ²) | (1/σ√2π)e^(-(x-μ)²/2σ²) | μ | σ² |

### Normal Distribution
```
Z = (X − μ) / σ  — standard normal transformation
68-95-99.7 rule:
  P(μ-σ ≤ X ≤ μ+σ) ≈ 0.68
  P(μ-2σ ≤ X ≤ μ+2σ) ≈ 0.95
  P(μ-3σ ≤ X ≤ μ+3σ) ≈ 0.997
```

### Central Limit Theorem
```
For large n, X̄ ~ N(μ, σ²/n) regardless of population distribution
Standard error = σ/√n
```

---

## ❌ Common Mistakes

| Mistake | Correct Understanding |
|---|---|
| Independent ↔ mutually exclusive | Independent: P(A∩B)=P(A)P(B); Mutually exclusive: P(A∩B)=0 |
| Mean of binomial = np² | Mean = np; Variance = np(1-p) |
| Poisson: mean ≠ variance | For Poisson: Mean = Variance = λ |
| Exponential memoryless | P(X > s+t | X > s) = P(X > t) — this is the memoryless property |
| Var(X+Y) = Var(X)+Var(Y) always | Only when X and Y are independent |

---

## 📊 PYQ Frequency Analysis (2015–2024)

| Topic | Frequency | Marks Range |
|---|:---:|:---:|
| Bayes' Theorem | Very High | 1–2 |
| Probability distributions | High | 1–2 |
| Expected value & variance | High | 1 |
| Conditional probability | High | 1 |
| Normal distribution | Medium | 1 |
| Markov chains | Medium | 1 |

---

## 🎯 Confidence Tracker

| Topic | Confidence | Last Revised |
|---|:---:|---|
| Basic Probability | ☐ Low / ☐ Med / ☐ High | |
| Bayes' Theorem | ☐ Low / ☐ Med / ☐ High | |
| Random Variables | ☐ Low / ☐ Med / ☐ High | |
| Distributions | ☐ Low / ☐ Med / ☐ High | |
| Statistics | ☐ Low / ☐ Med / ☐ High | |
