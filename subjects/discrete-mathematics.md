# 🔢 Discrete Mathematics

![Weightage](https://img.shields.io/badge/Weightage-6–8%20marks-orange)
![Priority](https://img.shields.io/badge/Priority-High-orange)

---

## 📋 Topic Checklist

### 🔷 Set Theory
- [ ] Sets — definition, roster and set builder forms
- [ ] Subsets, power sets, universal set
- [ ] Set operations: union, intersection, complement, difference
- [ ] De Morgan's laws for sets
- [ ] Cartesian product
- [ ] Venn diagrams
- [ ] Principle of Inclusion-Exclusion (PIE)
- [ ] Infinite sets — countable and uncountable

### 🔷 Relations
- [ ] Binary relations — definition, representation (matrix, digraph)
- [ ] Properties: reflexive, irreflexive, symmetric, antisymmetric, transitive
- [ ] Equivalence relation (reflexive + symmetric + transitive)
- [ ] Equivalence classes and partitions
- [ ] Partial order relation — POSET
- [ ] Total order (linear order)
- [ ] Hasse diagrams
- [ ] Lattice — meet and join operations
- [ ] Transitive closure — Warshall's algorithm
- [ ] Composition of relations

### 🔷 Functions
- [ ] Function definition — domain, codomain, range
- [ ] Types: injective (one-to-one), surjective (onto), bijective
- [ ] Inverse functions
- [ ] Composition of functions
- [ ] Floor and ceiling functions
- [ ] Pigeonhole principle
- [ ] Counting functions between finite sets

### 🔷 Mathematical Logic / Propositional Logic
- [ ] Propositions, truth values, logical connectives
- [ ] Negation, conjunction (∧), disjunction (∨), implication (→), biconditional (↔)
- [ ] Precedence of operators: ¬, ∧, ∨, →, ↔
- [ ] Truth tables
- [ ] Logical equivalences: De Morgan's, contrapositive, double negation
- [ ] Tautology, contradiction, contingency
- [ ] Satisfiability

### 🔷 Predicate Logic (First-Order Logic)
- [ ] Predicates and quantifiers: ∀ (universal), ∃ (existential)
- [ ] Nested quantifiers
- [ ] Negating quantified statements
- [ ] Arguments and rules of inference:
  - [ ] Modus Ponens, Modus Tollens
  - [ ] Hypothetical Syllogism, Disjunctive Syllogism
  - [ ] Universal Instantiation/Generalization

### 🔷 Proof Techniques
- [ ] Direct proof
- [ ] Proof by contradiction (indirect proof)
- [ ] Proof by contrapositive
- [ ] Proof by induction (weak and strong)
- [ ] Proof by cases

### 🔷 Combinatorics
- [ ] Basic counting: multiplication and addition rules
- [ ] Permutations: P(n,r) = n!/(n-r)!
- [ ] Combinations: C(n,r) = n! / (r!(n-r)!)
- [ ] Permutations with repetition
- [ ] Combinations with repetition (stars and bars)
- [ ] Binomial theorem and binomial coefficients
- [ ] Pascal's triangle and identities
- [ ] Principle of Inclusion-Exclusion (PIE) for counting
- [ ] Pigeonhole principle
- [ ] Recurrence relations:
  - [ ] Setting up recurrences
  - [ ] Solving linear recurrences (homogeneous and non-homogeneous)
  - [ ] Characteristic equation method
- [ ] Generating functions (basics)

### 🔷 Graph Theory
- [ ] Graphs — definition, types (undirected, directed, weighted, simple, multi)
- [ ] Degree of vertex — handshaking lemma: Σdeg(v) = 2|E|
- [ ] Paths, cycles, trails, walks
- [ ] Connected components
- [ ] Eulerian path and circuit — conditions
- [ ] Hamiltonian path and circuit — NP-complete problem
- [ ] Bipartite graphs — 2-colorable, no odd cycles
- [ ] Planar graphs — Euler's formula: V − E + F = 2
- [ ] Graph coloring — chromatic number
- [ ] Trees — definition, properties (n-1 edges, connected, acyclic)
- [ ] Spanning trees — number = Cayley's formula (nⁿ⁻²)
- [ ] Minimum spanning trees (see DSA)
- [ ] Isomorphism of graphs

---

## ⚡ Key Formulas

### Counting Formulas
```
P(n,r) = n! / (n-r)!                 — ordered, no repetition
C(n,r) = n! / (r!(n-r)!)             — unordered, no repetition
Permutations with repetition = n^r   — ordered, with repetition
Stars and Bars = C(n+r-1, r)         — unordered, with repetition

Derangements: D(n) = n! × Σ((-1)^k / k!) for k=0 to n
             ≈ n! / e
```

### Binomial Theorem
```
(x+y)^n = Σ C(n,k) x^(n-k) y^k  for k=0 to n
Sum of binomial coefficients: Σ C(n,k) = 2^n
```

### Inclusion-Exclusion Principle
```
|A ∪ B| = |A| + |B| − |A ∩ B|
|A ∪ B ∪ C| = |A| + |B| + |C| − |A∩B| − |B∩C| − |A∩C| + |A∩B∩C|
```

### Graph Theory
```
Euler's formula (planar): V − E + F = 2
Handshaking lemma: Σdeg(v) = 2|E|  (so sum of degrees is always even)
Eulerian circuit: exists iff connected and all vertices have even degree
Eulerian path: exists iff exactly 0 or 2 vertices have odd degree
Bipartite: iff no odd-length cycles
Trees: |E| = |V| − 1, exactly one path between any two nodes
```

### Recurrence Relations
```
Homogeneous: aₙ = c₁aₙ₋₁ + c₂aₙ₋₂
Characteristic equation: r² = c₁r + c₂
Distinct roots r₁, r₂: aₙ = A·r₁ⁿ + B·r₂ⁿ
Repeated root r: aₙ = (A + Bn)·rⁿ
```

---

## ❌ Common Mistakes

| Mistake | Correct Understanding |
|---|---|
| Antisymmetric = not symmetric | Antisymmetric allows aRa; symmetric and antisymmetric can coexist |
| Euler circuit needs all even degree | Yes, AND graph must be connected |
| Tree has no cycles → disconnected OK | Tree must be connected with no cycles |
| PIE for 3 sets misses triple intersection | |A∪B∪C| = |A|+|B|+|C|-|A∩B|-|B∩C|-|A∩C|+|A∩B∩C| |
| C(n,r) = P(n,r) | C(n,r) = P(n,r)/r! |
| Planar graph = no crossings in any drawing | Planar = can be drawn without crossings |

---

## 📊 PYQ Frequency Analysis (2015–2024)

| Topic | Frequency | Marks Range |
|---|:---:|:---:|
| Graph Theory (Euler, trees, coloring) | Very High | 2–3 |
| Combinatorics (counting, PIE) | High | 1–2 |
| Relations and their properties | High | 1–2 |
| Logic (propositional, predicate) | High | 1–2 |
| Recurrence relations | Medium | 1–2 |
| Set theory | Medium | 1 |

---

## 🎯 Confidence Tracker

| Topic | Confidence | Last Revised |
|---|:---:|---|
| Set Theory | ☐ Low / ☐ Med / ☐ High | |
| Logic | ☐ Low / ☐ Med / ☐ High | |
| Relations & Functions | ☐ Low / ☐ Med / ☐ High | |
| Combinatorics | ☐ Low / ☐ Med / ☐ High | |
| Graph Theory | ☐ Low / ☐ Med / ☐ High | |
