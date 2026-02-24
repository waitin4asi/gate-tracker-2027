# 🤖 Theory of Computation / Automata

![Weightage](https://img.shields.io/badge/Weightage-6–8%20marks-orange)
![Priority](https://img.shields.io/badge/Priority-High-orange)

---

## 📋 Topic Checklist

### 🔷 Finite Automata
- [ ] DFA — definition, 5-tuple, transition function, language accepted
- [ ] NFA — definition, 5-tuple, ε-transitions
- [ ] NFA to DFA conversion (subset construction)
- [ ] ε-NFA to DFA conversion
- [ ] DFA minimization (Myhill-Nerode / table-filling algorithm)
- [ ] Regular languages — closure properties
- [ ] Proving non-regularity using Pumping Lemma for Regular Languages

### 🔷 Regular Expressions & Regular Languages
- [ ] Basic regular operations: union, concatenation, Kleene star
- [ ] RE to NFA (Thompson's construction)
- [ ] DFA to RE conversion (state elimination)
- [ ] Equivalence of DFA, NFA, ε-NFA, RE
- [ ] Closure properties of regular languages:
  - [ ] Union, concatenation, Kleene star, complement, intersection, difference, reversal, homomorphism

### 🔷 Context-Free Grammars (CFG)
- [ ] Grammar definition: terminals, non-terminals, production rules, start symbol
- [ ] Derivations — leftmost, rightmost
- [ ] Parse trees and ambiguity
- [ ] Ambiguous vs unambiguous grammars
- [ ] Inherently ambiguous languages
- [ ] Simplification of CFG:
  - [ ] Removal of useless symbols
  - [ ] Removal of ε-productions
  - [ ] Removal of unit productions
- [ ] Chomsky Normal Form (CNF)
- [ ] Greibach Normal Form (GNF)
- [ ] CYK Algorithm for membership testing

### 🔷 Pushdown Automata (PDA)
- [ ] PDA — definition, 7-tuple
- [ ] Acceptance by final state vs empty stack
- [ ] Equivalence of PDA and CFG
- [ ] Deterministic PDA (DPDA) — less powerful than NPDA
- [ ] Context-free language closure properties
- [ ] Pumping Lemma for CFLs — proving non-context-free

### 🔷 Turing Machines
- [ ] TM — definition, 7-tuple
- [ ] TM configurations and computation
- [ ] TM variants: multi-tape, non-deterministic, enumerator (all equivalent)
- [ ] Recursive languages and recursively enumerable languages
- [ ] Church-Turing Thesis

### 🔷 Decidability
- [ ] Decidable problems — have a TM that always halts
- [ ] Undecidable problems:
  - [ ] Halting problem — undecidable (proven by diagonalization)
  - [ ] Acceptance problem for TMs
  - [ ] Post Correspondence Problem (PCP)
- [ ] Reduction — if A reduces to B, and B is decidable, then A is decidable
- [ ] Rice's Theorem — any non-trivial property of TM language is undecidable

### 🔷 Complexity Theory
- [ ] P — problems solvable in polynomial time
- [ ] NP — problems verifiable in polynomial time
- [ ] P ⊆ NP (P = NP is open problem)
- [ ] NP-complete — hardest problems in NP (NP + NP-hard)
- [ ] NP-hard — at least as hard as NP-complete
- [ ] Cook-Levin Theorem — SAT is NP-complete
- [ ] Polynomial-time reductions
- [ ] Common NP-complete problems: 3-SAT, Hamiltonian Cycle, Vertex Cover, Clique, Subset Sum

---

## ⚡ Key Concepts & Rules

### Language Hierarchy (Chomsky)
```
Type 0 (Recursively Enumerable) ⊃ Type 1 (Context-Sensitive) ⊃
Type 2 (Context-Free) ⊃ Type 3 (Regular)

Recognized by:
Type 3 → Finite Automaton (DFA/NFA)
Type 2 → Pushdown Automaton (PDA)
Type 1 → Linear Bounded Automaton (LBA)
Type 0 → Turing Machine (TM)
```

### Pumping Lemma for Regular Languages
```
For regular language L, ∃ pumping length p such that:
For all s ∈ L with |s| ≥ p,
  ∃ x, y, z: s = xyz where
    |xy| ≤ p
    |y| ≥ 1
    For all i ≥ 0: xy^i z ∈ L

Use to PROVE a language is NOT regular (find a string that can't be pumped)
```

### Pumping Lemma for CFLs
```
For CFL L, ∃ pumping length p such that:
For all s ∈ L with |s| ≥ p,
  ∃ u, v, w, x, y: s = uvwxy where
    |vx| ≥ 1
    |vwx| ≤ p
    For all i ≥ 0: uv^i wx^i y ∈ L
```

### Closure Properties Summary
| Property | Regular | CFL | CSL | RE |
|---|:---:|:---:|:---:|:---:|
| Union | ✅ | ✅ | ✅ | ✅ |
| Concatenation | ✅ | ✅ | ✅ | ✅ |
| Kleene Star | ✅ | ✅ | ✅ | ✅ |
| Intersection | ✅ | ❌ | ✅ | ✅ |
| Complement | ✅ | ❌ | ✅ | ❌ |
| Difference | ✅ | ❌ | ✅ | ❌ |
| Problem | Decidable? |
|---|:---:|
| DFA equivalence | ✅ Yes |
| DFA emptiness | ✅ Yes |
| CFG emptiness | ✅ Yes |
| CFG ambiguity | ❌ No |
| TM halting | ❌ No |
| CFL ∩ CFL = ? (CFL?) | ❌ No |

---

## ❌ Common Mistakes

| Mistake | Correct Understanding |
|---|---|
| All NFA have fewer states than DFA | NFA-to-DFA can exponentially increase states |
| DPDA = NPDA | DPDA ⊂ NPDA; DPDA accepts only deterministic CFLs |
| RE closed under intersection | RE NOT closed under intersection (closure properties differ from CFL) |
| Halting is semi-decidable | Halting is RE but not recursive (semi-decidable = recognizable) |
| NP-complete = NP-hard | NP-complete = NP ∩ NP-hard |
| All undecidable problems are RE | Some problems are not even RE (e.g., complement of halting) |

---

## 📊 PYQ Frequency Analysis (2015–2024)

| Topic | Frequency | Marks Range |
|---|:---:|:---:|
| DFA/NFA construction & minimization | Very High | 2–3 |
| Regular/Non-regular language proofs | High | 1–2 |
| CFG / CFL properties | High | 1–2 |
| Decidability & Undecidability | High | 1–2 |
| P, NP, NP-complete | Medium | 1–2 |
| Closure properties | High | 1 |

---

## 🎯 Confidence Tracker

| Topic | Confidence | Last Revised |
|---|:---:|---|
| DFA / NFA | ☐ Low / ☐ Med / ☐ High | |
| Regular Expressions | ☐ Low / ☐ Med / ☐ High | |
| CFG / PDA | ☐ Low / ☐ Med / ☐ High | |
| Turing Machines | ☐ Low / ☐ Med / ☐ High | |
| Decidability | ☐ Low / ☐ Med / ☐ High | |
| Complexity (P, NP) | ☐ Low / ☐ Med / ☐ High | |
