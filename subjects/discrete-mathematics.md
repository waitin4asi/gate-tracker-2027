# 🧮 Discrete Mathematics

> **Weightage:** ~9% | **Avg Questions:** 6–8 | **Importance:** ⭐⭐⭐⭐⭐

---

## 📊 Overview

Discrete Math is foundational for all CS theory. It bridges mathematics and CS — graph theory overlaps with DSA, logic with TOC, counting with algorithms. High weightage and very learnable patterns.

---

## ✅ Topic-wise Checklist

### 🔢 Set Theory
- [ ] Sets, subsets, power set, universal set
- [ ] Set operations: union, intersection, difference, complement, symmetric difference
- [ ] Cartesian product
- [ ] Venn diagrams and counting
- [ ] Infinite sets, countable vs. uncountable (overview)
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🔣 Mathematical Logic
- [ ] Propositions, logical connectives (∧, ∨, ¬, →, ↔)
- [ ] Truth tables
- [ ] Tautology, contradiction, contingency
- [ ] Logical equivalences (De Morgan's, distributive, etc.)
- [ ] Predicates and quantifiers (∀, ∃)
- [ ] Rules of inference: Modus Ponens, Modus Tollens, Hypothetical Syllogism
- [ ] Proof techniques: direct, indirect (contradiction), contrapositive
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🔗 Relations
- [ ] Binary relations: definition, representation (matrix, graph)
- [ ] Properties: reflexive, irreflexive, symmetric, antisymmetric, asymmetric, transitive
- [ ] Equivalence relations: reflexive + symmetric + transitive
- [ ] Equivalence classes, partition
- [ ] Partial orders (POSET): reflexive + antisymmetric + transitive
- [ ] Hasse diagrams
- [ ] Total order (linear order)
- [ ] Transitive closure (Warshall's algorithm)
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🗺️ Functions
- [ ] One-to-one (injective), onto (surjective), bijective functions
- [ ] Composition of functions
- [ ] Inverse functions
- [ ] Floor, ceiling functions
- [ ] Pigeonhole principle
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🕸️ Graph Theory
- [ ] Graph definitions: vertices, edges, degree
- [ ] Types: directed, undirected, weighted, multigraph
- [ ] Degree sequence: Handshaking lemma
- [ ] Paths, walks, trails, cycles
- [ ] Connected graphs, strongly/weakly connected (directed)
- [ ] Eulerian path and circuit conditions
- [ ] Hamiltonian path and circuit
- [ ] Trees: definition, properties (n-1 edges, unique path)
- [ ] Spanning trees, minimum spanning tree
- [ ] Planar graphs: Euler's formula (V - E + F = 2)
- [ ] Graph coloring: chromatic number
- [ ] Bipartite graphs
- [ ] Isomorphic graphs
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🔢 Combinatorics & Counting
- [ ] Basic counting: addition rule, multiplication rule
- [ ] Permutations: P(n,r) = n!/(n-r)!
- [ ] Combinations: C(n,r) = n!/(r!(n-r)!)
- [ ] Binomial theorem: (x+y)ⁿ = Σ C(n,k) xᵏ yⁿ⁻ᵏ
- [ ] Inclusion-Exclusion principle
- [ ] Pigeonhole principle (extended)
- [ ] Derangements
- [ ] Catalan numbers
- [ ] Stirling numbers (overview)
- [ ] Recurrence relations: linear, homogeneous
- [ ] Generating functions (overview)
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🔢 Number Theory
- [ ] Divisibility, GCD, LCM
- [ ] Euclidean algorithm
- [ ] Modular arithmetic, congruences
- [ ] Fermat's little theorem: aᵖ⁻¹ ≡ 1 (mod p), p prime
- [ ] Euler's totient function φ(n)
- [ ] Chinese Remainder Theorem
- [ ] Prime numbers, fundamental theorem of arithmetic
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

---

## 📋 Key Formulas

### Counting
```
P(n,r) = n! / (n-r)!       [ordered selection, no repetition]
C(n,r) = n! / (r!(n-r)!)   [unordered selection, no repetition]
nrⁿ                          [ordered selection, with repetition]
C(n+r-1, r)                  [unordered selection, with repetition]

Inclusion-Exclusion: |A∪B| = |A| + |B| - |A∩B|
                    |A∪B∪C| = |A|+|B|+|C| - |A∩B| - |B∩C| - |A∩C| + |A∩B∩C|
```

### Graphs
```
Handshaking Lemma: Σ deg(v) = 2|E|
Euler Circuit: exists iff connected and all vertices have even degree
Euler Path: exists iff connected and exactly 2 vertices have odd degree
Tree with n vertices: has exactly n-1 edges
Complete graph Kₙ: n(n-1)/2 edges
Planar graph (Euler): V - E + F = 2  (connected planar)
Bipartite Kₘ,ₙ: m×n edges
Chromatic number: χ(G) ≥ max clique size; χ(bipartite) ≤ 2
```

### Number Theory
```
gcd(a,b) × lcm(a,b) = a × b
Fermat's little theorem: aᵖ⁻¹ ≡ 1 (mod p) for prime p, gcd(a,p)=1
Euler's theorem: aᵠ⁽ⁿ⁾ ≡ 1 (mod n) where gcd(a,n)=1
φ(pᵏ) = pᵏ - pᵏ⁻¹
φ(mn) = φ(m)φ(n) when gcd(m,n)=1
```

### Recurrences
```
Homogeneous: aₙ = c₁aₙ₋₁ + c₂aₙ₋₂ + ...
Characteristic equation: rⁿ = c₁rⁿ⁻¹ + c₂rⁿ⁻²
```

---

## ⚠️ Common Mistakes

1. **Partial order vs. total order:** POSET doesn't require all pairs to be comparable
2. **Euler vs. Hamiltonian:** Euler visits all edges; Hamiltonian visits all vertices
3. **Chromatic number:** χ(tree) = 2; χ(odd cycle) = 3; χ(complete graph Kₙ) = n
4. **C(n,r) vs. P(n,r):** Combination when order doesn't matter; Permutation when it does
5. **Inclusion-Exclusion sign:** Alternating +/- signs; pairs subtract, triples add
6. **Reflexive closure:** Add self-loops to all vertices; don't confuse with symmetric closure
7. **Pigeonhole:** N+1 objects in N bins → at least one bin has 2 objects
8. **Equivalence class:** Must be reflexive, symmetric AND transitive — all three required

---

## 📚 Resources

- **Primary:** Discrete Mathematics — Kenneth Rosen
- **Video:** Ravindrababu Ravula Discrete Math (YouTube)
- **Practice:** GATE Overflow Discrete Math tag

---

## 📅 PYQ Progress Tracker

- [ ] PYQs 2020–2026 solved
- [ ] PYQs 2015–2019 solved
- [ ] PYQs 2010–2014 solved

---

*Updated: ___ | Revision Count: ___*
