# 🔢 Linear Algebra

![Weightage](https://img.shields.io/badge/Weightage-3–4%20marks-yellow)
![Priority](https://img.shields.io/badge/Priority-Medium-yellow)

---

## 📋 Topic Checklist

### 🔷 Matrices
- [ ] Matrix types: square, rectangular, symmetric, skew-symmetric, diagonal, identity, null
- [ ] Matrix operations: addition, subtraction, multiplication
- [ ] Transpose of a matrix — properties
- [ ] Trace of a matrix (sum of diagonal elements)
- [ ] Determinant — definition, cofactor expansion, properties
- [ ] Matrix inversion — adjugate method, Gaussian elimination
- [ ] Rank of a matrix — definition, computation using row reduction
- [ ] Row echelon form (REF) and reduced row echelon form (RREF)

### 🔷 Systems of Linear Equations
- [ ] Homogeneous and non-homogeneous systems
- [ ] Consistency conditions using rank:
  - [ ] Consistent iff rank(A) = rank(A|b)
  - [ ] Unique solution iff rank = n (number of unknowns)
  - [ ] Infinite solutions iff rank < n
- [ ] Gaussian elimination and back substitution
- [ ] Cramer's rule (for small systems)
- [ ] Solution space of homogeneous systems (null space)

### 🔷 Vector Spaces
- [ ] Vector space definition and axioms
- [ ] Subspaces
- [ ] Linear independence and dependence
- [ ] Span and basis
- [ ] Dimension of a vector space
- [ ] Null space (kernel) and column space (image/range)
- [ ] Rank-Nullity theorem: rank(A) + nullity(A) = n

### 🔷 Eigenvalues & Eigenvectors
- [ ] Definition: Av = λv
- [ ] Characteristic polynomial: det(A − λI) = 0
- [ ] Computing eigenvalues and eigenvectors
- [ ] Algebraic multiplicity vs geometric multiplicity
- [ ] Diagonalization: A = PDP⁻¹
- [ ] Conditions for diagonalizability
- [ ] Properties of eigenvalues:
  - [ ] Trace = sum of eigenvalues
  - [ ] Determinant = product of eigenvalues
  - [ ] Eigenvalues of Aⁿ are λⁿ
  - [ ] Eigenvalues of A⁻¹ are 1/λ

### 🔷 Special Matrices
- [ ] Symmetric matrices — real eigenvalues, orthogonal eigenvectors
- [ ] Orthogonal matrix: A^T = A⁻¹
- [ ] Positive definite matrix — all eigenvalues positive
- [ ] Singular vs non-singular matrix
- [ ] Idempotent matrix: A² = A

### 🔷 Inner Products & Orthogonality
- [ ] Dot product (inner product in Rⁿ)
- [ ] Norm / length of a vector
- [ ] Orthogonal and orthonormal vectors
- [ ] Gram-Schmidt orthogonalization process
- [ ] Orthogonal projection

### 🔷 Linear Transformations
- [ ] Definition and properties
- [ ] Matrix representation of linear transformation
- [ ] Kernel and image of a linear transformation
- [ ] Isomorphism

---

## ⚡ Key Formulas

### Determinant Properties
```
det(AB) = det(A) × det(B)
det(A^T) = det(A)
det(A⁻¹) = 1/det(A)
det(kA) = kⁿ × det(A)  (n = size of matrix)
det(A) = product of eigenvalues
```

### Rank Properties
```
rank(AB) ≤ min(rank(A), rank(B))
rank(A + B) ≤ rank(A) + rank(B)
rank(A^T A) = rank(A)

Rank-Nullity: rank(A) + nullity(A) = number of columns
```

### Eigenvalue Properties
```
Characteristic equation: det(A − λI) = 0

Sum of eigenvalues = Trace(A) = sum of diagonal elements
Product of eigenvalues = det(A)

If A has eigenvalue λ:
  A^n has eigenvalue λⁿ
  A⁻¹ has eigenvalue 1/λ
  (A − kI) has eigenvalue (λ − k)
  A^T has same eigenvalues as A
```

### Cayley-Hamilton Theorem
```
Every matrix satisfies its own characteristic equation.
If p(λ) = 0 is the characteristic polynomial, then p(A) = 0

Useful for computing A⁻¹, A^n without direct computation
```

---

## ❌ Common Mistakes

| Mistake | Correct Understanding |
|---|---|
| AB = BA always | Matrix multiplication is NOT commutative in general |
| rank = number of rows | rank ≤ min(rows, columns); row reduce to find actual rank |
| det(A+B) = det(A) + det(B) | WRONG — det is NOT linear over matrix addition |
| Zero eigenvalue means singular | Correct — det(A) = product of eigenvalues, so 0 ∈ eigenvalues → det = 0 |
| All symmetric matrices are diagonal | Symmetric means A = A^T, not necessarily diagonal |
| Diagonalizable = distinct eigenvalues | Sufficient but not necessary; geometric multiplicity matters |

---

## 📊 PYQ Frequency Analysis (2015–2024)

| Topic | Frequency | Marks Range |
|---|:---:|:---:|
| Eigenvalues & Eigenvectors | Very High (every year) | 1–2 |
| Rank & Linear Systems | High | 1 |
| Determinants | High | 1 |
| Cayley-Hamilton | Medium | 1 |
| Orthogonality | Low–Medium | 1 |

---

## 🎯 Confidence Tracker

| Topic | Confidence | Last Revised |
|---|:---:|---|
| Matrices & Determinants | ☐ Low / ☐ Med / ☐ High | |
| Eigenvalues / Eigenvectors | ☐ Low / ☐ Med / ☐ High | |
| Rank & Systems of Equations | ☐ Low / ☐ Med / ☐ High | |
| Vector Spaces | ☐ Low / ☐ Med / ☐ High | |
| Diagonalization | ☐ Low / ☐ Med / ☐ High | |
