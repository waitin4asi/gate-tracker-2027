# 🔢 Linear Algebra

> **Weightage:** ~4% | **Avg Questions:** 2–3 | **Importance:** ⭐⭐⭐⭐

---

## 📊 Overview

Linear Algebra is one of the most learnable subjects — limited topics, high repeatability in GATE. Eigenvalues, matrix operations, and rank are almost guaranteed questions. Great ROI for time invested.

---

## ✅ Topic-wise Checklist

### 🔲 Matrices
- [ ] Matrix types: square, diagonal, identity, symmetric, skew-symmetric, orthogonal
- [ ] Matrix operations: addition, scalar multiplication, matrix multiplication
- [ ] Transpose: (AB)ᵀ = BᵀAᵀ
- [ ] Matrix inverse: conditions, computation using row operations
- [ ] Properties of inverse: (AB)⁻¹ = B⁻¹A⁻¹
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🔢 Determinants
- [ ] Determinant computation (cofactor expansion, row operations)
- [ ] Properties of determinants
- [ ] Cramer's rule
- [ ] Adjugate (adjoint) matrix
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 📐 Rank and Linear Systems
- [ ] Row echelon form, reduced row echelon form (RREF)
- [ ] Row operations, Gaussian elimination
- [ ] Rank of a matrix: number of non-zero rows in echelon form
- [ ] Null space (kernel), column space, row space
- [ ] Rank-Nullity theorem: rank(A) + nullity(A) = n (number of columns)
- [ ] System of linear equations: Ax = b
  - [ ] Consistent (unique solution, infinite solutions) vs. inconsistent
  - [ ] Conditions: rank(A) vs. rank([A|b]) vs. n
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🔑 Eigenvalues & Eigenvectors
- [ ] Definition: Av = λv
- [ ] Characteristic equation: det(A - λI) = 0
- [ ] Computing eigenvalues and eigenvectors
- [ ] Properties of eigenvalues
- [ ] Cayley-Hamilton theorem: A satisfies its own characteristic equation
- [ ] Diagonalization: A = PDP⁻¹
- [ ] Spectral theorem for symmetric matrices
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🏗️ Vector Spaces
- [ ] Vector space definition, axioms
- [ ] Subspaces: conditions (closed under + and scalar mult)
- [ ] Linear independence, span
- [ ] Basis: linearly independent spanning set
- [ ] Dimension of a vector space
- [ ] Coordinate vectors
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🔄 Linear Transformations
- [ ] Definition: T(au + bv) = aT(u) + bT(v)
- [ ] Matrix representation of linear transformation
- [ ] Kernel (null space) and image (range)
- [ ] One-to-one: kernel = {0}; Onto: image = codomain
- [ ] Isomorphism
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

---

## 📋 Key Formulas

### Eigenvalue Properties
```
Sum of eigenvalues = trace(A) = sum of diagonal elements
Product of eigenvalues = det(A)
If A has eigenvalue λ, then:
  A^n has eigenvalue λⁿ
  A⁻¹ has eigenvalue 1/λ  (if A invertible)
  kA has eigenvalue kλ
  (A - kI) has eigenvalue (λ - k)
```

### Rank-Nullity
```
rank(A) + nullity(A) = number of columns of A
```

### Solutions to Ax = b
```
Case 1: rank(A) = rank([A|b]) = n → Unique solution
Case 2: rank(A) = rank([A|b]) < n → Infinite solutions
Case 3: rank(A) < rank([A|b]) → No solution (inconsistent)

For homogeneous Ax = 0:
  Always has trivial solution x = 0
  Non-trivial solution exists iff rank(A) < n (i.e., det(A) = 0)
```

### Determinant Properties
```
det(AB) = det(A) · det(B)
det(Aᵀ) = det(A)
det(A⁻¹) = 1/det(A)
det(kA) = kⁿ det(A)  [n × n matrix]
If row/column all zeros → det = 0
Row swap → det changes sign
Row scaling by k → det multiplied by k
```

### Cayley-Hamilton
```
Every matrix satisfies its own characteristic polynomial.
If characteristic polynomial is p(λ) = λ² - 5λ + 6,
then p(A) = A² - 5A + 6I = 0
This can be used to find A⁻¹ and powers of A efficiently.
```

---

## ⚠️ Common Mistakes

1. **Trace ≠ determinant:** Trace = sum of diagonal = sum of eigenvalues; det = product of eigenvalues
2. **Rank vs. determinant:** det = 0 ↔ rank < n (singular matrix), not rank = 0
3. **Eigenvalue of A² ≠ (eigenvalue of A)²:** Actually it IS true: if Av = λv, then A²v = λ²v ✅
4. **Orthogonal matrix:** Aᵀ = A⁻¹, so det(A) = ±1, NOT det(A) = 1 always
5. **Linear independence vs. span:** Both needed for basis; neither alone is sufficient
6. **Inconsistent system:** rank(A) < rank([A|b]) — MORE rows in augmented system
7. **Diagonalization condition:** A is diagonalizable iff it has n linearly independent eigenvectors
8. **Complex eigenvalues:** Real symmetric matrices always have real eigenvalues

---

## 📈 PYQ Frequency Analysis

| Topic | Frequency |
|-------|-----------|
| Eigenvalues (properties, computation) | Every year |
| Rank and solutions to systems | Every year |
| Determinants | Most years |
| Vector spaces | Some years |

---

## 📚 Resources

- **Primary:** Linear Algebra and Its Applications — Gilbert Strang
- **Visual:** 3Blue1Brown "Essence of Linear Algebra" (YouTube) — build intuition
- **MIT OCW:** 18.06 Linear Algebra — Gilbert Strang lectures (free)
- **Practice:** GATE Math PYQs

---

## 📅 PYQ Progress Tracker

- [ ] PYQs 2020–2026 solved
- [ ] PYQs 2015–2019 solved
- [ ] PYQs 2010–2014 solved

---

*Updated: ___ | Revision Count: ___*
