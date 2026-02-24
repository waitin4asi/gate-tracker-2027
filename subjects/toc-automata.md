# 🤖 Theory of Computation (TOC) / Automata Theory

> **Weightage:** ~8% | **Avg Questions:** 5–7 | **Importance:** ⭐⭐⭐⭐⭐

---

## 📊 Overview

TOC is one of the most unique and scoring subjects if understood correctly. It's mostly theoretical with some calculation (DFA construction, minimization). Once the logic clicks, questions become very systematic.

**Scoring Pattern:**
- 2 questions on FA (DFA/NFA/regular expressions)
- 1–2 questions on CFG / PDA
- 1 question on Turing Machines / decidability
- 1 question on Complexity (P, NP, NP-complete)

---

## ✅ Topic-wise Checklist

### 🔤 Finite Automata (FA)
- [ ] DFA: definition, states, transitions, acceptance
- [ ] DFA construction from language descriptions
- [ ] NFA: non-deterministic transitions, epsilon transitions
- [ ] NFA to DFA conversion (subset construction)
- [ ] epsilon-NFA to NFA conversion (epsilon closure)
- [ ] Minimization of DFA (table filling / equivalence class method)
- [ ] Language recognized by DFA/NFA
- [ ] Complement, union, intersection of regular languages using FA
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 📋 Regular Expressions
- [ ] Basic operators: concatenation, union (|), Kleene star (*), plus (+)
- [ ] RE to NFA (Thompson's construction)
- [ ] NFA/DFA to RE (state elimination method)
- [ ] Regular expression equivalences
- [ ] Describing language patterns using RE
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🚫 Pumping Lemma (Regular)
- [ ] Statement of pumping lemma for regular languages
- [ ] Using pumping lemma to prove a language is NOT regular
- [ ] Common non-regular languages: {aⁿbⁿ}, {aⁿbⁿcⁿ}, palindromes
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🌲 Context-Free Grammars (CFG)
- [ ] Productions, derivations (leftmost, rightmost)
- [ ] Parse trees, ambiguity
- [ ] Inherently ambiguous grammars
- [ ] Chomsky Normal Form (CNF) conversion
- [ ] Greibach Normal Form (GNF) conversion
- [ ] CYK parsing algorithm
- [ ] Pumping lemma for CFL
- [ ] Closure properties of CFL
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 📥 Pushdown Automata (PDA)
- [ ] PDA: states, input, stack, transitions
- [ ] Acceptance: by empty stack vs. by final state
- [ ] PDA for balanced parentheses, {aⁿbⁿ}, palindromes
- [ ] CFG to PDA conversion
- [ ] Deterministic PDA (DPDA) vs. non-deterministic PDA
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🖥️ Turing Machines
- [ ] TM definition: states, tape, head, transitions
- [ ] TM as acceptor and decider
- [ ] Multi-tape TM, Non-deterministic TM (equivalence)
- [ ] Church-Turing Thesis
- [ ] Recursive (decidable) languages
- [ ] Recursively Enumerable (RE) languages
- [ ] Universal Turing Machine (UTM)
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### ❓ Decidability
- [ ] Decidable problems: membership for DFA, CFL
- [ ] Undecidable problems: Halting problem, Post Correspondence Problem (PCP)
- [ ] Reduction: proving undecidability
- [ ] Rice's Theorem: all non-trivial semantic properties of TM are undecidable
- [ ] Semi-decidable (RE but not recursive) languages
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### ⏱️ Computational Complexity
- [ ] Time complexity classes: P, NP
- [ ] P ⊆ NP (P = NP? open problem)
- [ ] NP-Complete: definition, Cook's theorem (SAT is NP-complete)
- [ ] NP-Hard: at least as hard as NP-complete problems
- [ ] Polynomial-time reductions
- [ ] Common NP-complete problems: 3-SAT, Clique, Vertex Cover, Hamiltonian Path
- [ ] PSPACE, EXPTIME (overview)
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

---

## 📋 Key Concepts & Rules

### Language Hierarchy (Chomsky)
```
Type 0 (Unrestricted)  ⊃  Type 1 (CSL)  ⊃  Type 2 (CFL)  ⊃  Type 3 (Regular)
Recognized by: TM           LBA             PDA              FA
```

### Closure Properties

| Operation | Regular | CFL |
|-----------|---------|-----|
| Union | ✅ | ✅ |
| Intersection | ✅ | ❌ |
| Complement | ✅ | ❌ |
| Concatenation | ✅ | ✅ |
| Kleene Star | ✅ | ✅ |
| Reversal | ✅ | ✅ |
| Intersection with Regular | ✅ | ✅ |

### NFA to DFA Subset Construction
```
Start state of DFA = epsilon-closure({start state of NFA})
For each DFA state S and each input symbol a:
  delta(S, a) = epsilon-closure(union of delta(q, a) for all q in S)
Mark as final any DFA state containing an NFA final state
```

### Pumping Lemma (Regular)
```
If L is regular, there exists p (pumping length) such that:
For any string w ∈ L with |w| ≥ p:
  w = xyz where |y| ≥ 1, |xy| ≤ p, and ∀k ≥ 0: xy^k z ∈ L
To prove non-regular: find a string where no valid pumping exists
```

### DFA Minimization
```
1. Remove unreachable states
2. Mark distinguishable pairs:
   - Any (final, non-final) pair is distinguishable
   - If (p,q) → (r,s) and (r,s) distinguishable, then (p,q) distinguishable
3. Merge equivalent (indistinguishable) states
```

---

## ⚠️ Common Mistakes

1. **Epsilon-NFA to DFA:** Always compute epsilon closure before and after each transition
2. **Pumping lemma misuse:** Pumping lemma can only prove non-regularity, NOT regularity
3. **Ambiguity definition:** A CFG is ambiguous if one string has two different parse trees (not derivations)
4. **PDA acceptance:** Empty stack acceptance ≠ final state acceptance (but equivalent power)
5. **NP-Hard vs NP-Complete:** NP-Complete = NP-Hard ∩ NP. Halting problem is NP-Hard but NOT NP-Complete
6. **P vs NP:** P problems have polynomial-time algorithms; NP problems have polynomial-time VERIFIERS
7. **Recursive vs RE:** Recursive = decidable (TM always halts); RE = TM halts on accepted strings only
8. **Rice's Theorem:** Applies to non-trivial semantic properties — NOT syntactic ones

---

## 📈 PYQ Frequency Analysis

| Topic | Frequency |
|-------|-----------|
| DFA/NFA construction & minimization | Every year |
| Regular expressions | Every year |
| CFL properties & PDA | Most years |
| Decidability | Most years |
| Complexity (P, NP) | Most years |
| Pumping lemma | Some years |

---

## 📚 Resources

- **Primary:** Introduction to Automata Theory — Hopcroft & Ullman
- **Alternate:** Introduction to Theory of Computation — Sipser (more readable)
- **Video:** Ravindrababu Ravula TOC playlist (YouTube) — best for GATE
- **Practice:** GATE Overflow TOC tag

---

## 📅 PYQ Progress Tracker

- [ ] PYQs 2020–2026 solved
- [ ] PYQs 2015–2019 solved
- [ ] PYQs 2010–2014 solved

---

*Updated: ___ | Revision Count: ___*
