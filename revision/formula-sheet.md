# ⚡ Formula Sheet — Quick Reference

> The most important formulas for GATE 2027. Review this every week.

---

## 🔢 Discrete Mathematics

### Set Theory
```
|A ∪ B| = |A| + |B| − |A ∩ B|
|A ∪ B ∪ C| = |A|+|B|+|C| − |A∩B| − |B∩C| − |A∩C| + |A∩B∩C|
|P(A)| = 2^|A|   (power set size)
De Morgan: (A∪B)' = A'∩B' ;  (A∩B)' = A'∪B'
```

### Combinatorics
```
P(n,r) = n!/(n-r)!
C(n,r) = n!/(r!(n-r)!)   =   C(n,n-r)
Stars and Bars: C(n+r-1, r)  [r items into n bins, repetition allowed]
Derangements: D(n) ≈ n!/e   (exact: n! × Σ (-1)^k/k! for k=0..n)
Binomial: (x+y)^n = Σ C(n,k) x^(n-k) y^k
```

### Graph Theory
```
Handshaking: Σ deg(v) = 2|E|
Euler circuit: connected + all even degrees
Euler path: connected + exactly 2 odd degree vertices
Planar graph: V − E + F = 2  (Euler's formula)
Non-planar condition: K₅ or K₃,₃ as subdivision (Kuratowski's theorem)
Tree: |E| = |V|−1, connected, acyclic
Cayley's formula: n^(n-2) spanning trees for complete graph Kₙ
```

---

## 📐 Linear Algebra

```
det(AB) = det(A)·det(B)
det(A^T) = det(A)
det(kA) = k^n·det(A)   [n = matrix dimension]
Trace(A) = Σ eigenvalues
det(A) = Π eigenvalues
Rank-Nullity: rank(A) + nullity(A) = #columns
EigenvaluesOf A^n = λⁿ
EigenvaluesOf A^(-1) = 1/λ
Cayley-Hamilton: every matrix satisfies its characteristic polynomial
```

---

## 🎲 Probability

### Key Rules
```
P(A∪B) = P(A)+P(B)−P(A∩B)
P(A|B) = P(A∩B)/P(B)
Independent: P(A∩B) = P(A)·P(B)
Bayes: P(A|B) = P(B|A)·P(A) / P(B)
Total probability: P(B) = Σᵢ P(B|Aᵢ)·P(Aᵢ)
```

### Distributions
```
Binomial B(n,p):  Mean=np,  Var=np(1-p)
Poisson(λ):       Mean=λ,   Var=λ
Geometric(p):     Mean=1/p, Var=(1-p)/p²
Normal N(μ,σ²):   Mean=μ,   Var=σ²
Exponential(λ):   Mean=1/λ, Var=1/λ²
Uniform(a,b):     Mean=(a+b)/2, Var=(b-a)²/12
```

### Statistics
```
E[aX+b] = aE[X]+b
Var(aX+b) = a²·Var(X)
Var(X) = E[X²]−(E[X])²
Cov(X,Y) = E[XY]−E[X]·E[Y]
ρ = Cov(X,Y)/(σ_X·σ_Y)
CLT: X̄ ~ N(μ, σ²/n) for large n
```

---

## 💻 Operating Systems

### CPU Scheduling
```
Turnaround Time = Completion − Arrival
Waiting Time    = Turnaround − Burst
Response Time   = First CPU − Arrival
```

### Memory — Effective Access Time
```
EAT (TLB) = h·(t_TLB + t_mem) + (1-h)·(t_TLB + 2·t_mem)
EAT (Page Fault) = (1-p)·t_mem + p·t_fault
```

### Page Replacement
```
FIFO: suffers Belady's anomaly (more frames → more faults possible)
LRU: optimal in practice, no Belady's anomaly
OPT: theoretical optimal, no Belady's anomaly
```

---

## 🌐 Computer Networks

### Sliding Window
```
a = propagation delay / transmission time

Stop & Wait efficiency: η = 1/(1+2a)

Go-Back-N:   Window ≤ 2^n − 1
Selective Repeat: Window ≤ 2^(n-1)

Efficiency: W/(1+2a)  if W < (1+2a)
            1          if W ≥ (1+2a)
```

### Key Formulas
```
Transmission time  = Frame size / Bandwidth
Propagation delay  = Distance / Speed
Bandwidth-Delay Product = Bandwidth × Propagation delay

Shannon capacity: C = B·log₂(1+S/N)
Nyquist: C = 2B·log₂(M)  [M = signal levels, noiseless]
```

### Subnetting
```
/n prefix → 2^(32-n) addresses per subnet
Usable hosts = 2^(32-n) − 2  (subtract network + broadcast)
```

---

## 🖥️ Computer Organization & Architecture

### Performance
```
CPU Time = IC × CPI × Clock Period = IC × CPI / Clock Rate
MIPS = Clock Rate / (CPI × 10⁶)
Speedup (Amdahl's) = 1 / [(1-f) + f/S]
```

### Cache
```
AMAT = Hit time + Miss rate × Miss penalty
     = h·T_L1 + (1-h)·(T_L1 + T_L2)   [two-level]

Hit ratio h → AMAT improves as h → 1
```

### Pipeline
```
Ideal CPI = 1
Actual CPI = 1 + stalls per instruction
Speedup = k·T_np / (T_np + (n-1)·T_stage)   [n = instructions, k = stages]

For large n: Speedup ≈ k
```

### IEEE 754 (Single Precision, 32-bit)
```
1 sign | 8 exponent (biased +127) | 23 mantissa
Value = (-1)^s × 1.M × 2^(E-127)
Special: E=0, M=0 → ±0 ; E=255, M=0 → ±∞ ; E=255, M≠0 → NaN
```

---

## 🗄️ DBMS

### Normalization
```
1NF: Atomic values, no repeating groups
2NF: 1NF + No partial dependency (non-prime → part of PK)
3NF: 2NF + No transitive dependency (non-prime → non-prime)
BCNF: Every determinant is a super key
4NF: BCNF + No non-trivial multivalued dependencies
```

### Armstrong's Axioms
```
Reflexivity:   β ⊆ α → α → β
Augmentation:  α → β → αγ → βγ
Transitivity:  α → β, β → γ → α → γ
```

### Transactions
```
Conflict serializable ↔ Precedence graph is acyclic
2PL: Phase 1 acquire all locks; Phase 2 only release
ACID: Atomicity, Consistency, Isolation, Durability
```

---

## 🤖 Theory of Computation

### Chomsky Hierarchy
```
Type 3 (Regular)     → DFA/NFA
Type 2 (CFL)         → PDA
Type 1 (CSL)         → LBA (Linear Bounded Automaton)
Type 0 (RE)          → Turing Machine
```

### Closure Properties
```
Regular  : ∪, ∩, ', concat, *, reversal, homomorphism ✅
CFL      : ∪, concat, *, reversal ✅ | ∩, ' ❌
```

### Pumping Lemma (Regular)
```
|s| ≥ p → s = xyz, |xy| ≤ p, |y| ≥ 1, ∀i≥0: xy^i z ∈ L
```

### Complexity
```
P ⊆ NP (open whether P = NP)
NP-complete = NP ∩ NP-hard
SAT is NP-complete (Cook-Levin Theorem)
```

---

## 🔀 DSA — Algorithm Complexities

| Algorithm | Time (Best/Avg/Worst) | Space |
|---|---|:---:|
| Merge Sort | O(n log n) all cases | O(n) |
| Quick Sort | O(n log n) avg / O(n²) worst | O(log n) |
| Heap Sort | O(n log n) all cases | O(1) |
| Binary Search | O(log n) | O(1) |
| BFS / DFS | O(V+E) | O(V) |
| Dijkstra (heap) | O((V+E) log V) | O(V) |
| Bellman-Ford | O(VE) | O(V) |
| Floyd-Warshall | O(V³) | O(V²) |
| Kruskal's | O(E log E) | O(V) |
| Prim's (heap) | O(E log V) | O(V) |

### Master Theorem
```
T(n) = aT(n/b) + f(n)
Case 1: f(n) = O(n^{log_b a - ε}) → T(n) = Θ(n^{log_b a})
Case 2: f(n) = Θ(n^{log_b a})    → T(n) = Θ(n^{log_b a} log n)
Case 3: f(n) = Ω(n^{log_b a + ε}) → T(n) = Θ(f(n))
```

---

## ⚙️ Compiler Design

```
FIRST(A):  terminals that start strings derived from A
FOLLOW(A): terminals that follow A in any sentential form

LL(1) condition: FIRST(α) ∩ FIRST(β) = ∅ for A→α | β
                 If ε ∈ FIRST(α): FIRST(α) ∩ FOLLOW(A) = ∅

Parsing power: LR(0) ⊆ SLR(1) ⊆ LALR(1) ⊆ CLR(1)

Left recursion: A → Aα | β → A → βA', A' → αA' | ε
```
