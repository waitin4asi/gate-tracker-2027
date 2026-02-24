# 🔌 Digital Logic

> **Weightage:** ~6% | **Avg Questions:** 4–5 | **Importance:** ⭐⭐⭐⭐

---

## 📊 Overview

Digital Logic is very scoring once you master Boolean algebra and K-maps. Sequential circuits (flip-flops, counters, shift registers) are common in GATE. Minimization questions are very predictable.

---

## ✅ Topic-wise Checklist

### 🔣 Boolean Algebra
- [ ] Boolean identities and theorems
- [ ] De Morgan's laws
- [ ] Duality principle
- [ ] Complement, dual forms
- [ ] Canonical forms: SOP (Sum of Products), POS (Product of Sums)
- [ ] Minterm, maxterm notation
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🔲 Logic Gates
- [ ] Basic gates: AND, OR, NOT
- [ ] Derived gates: NAND, NOR, XOR, XNOR
- [ ] Universal gates: NAND and NOR can implement any function
- [ ] Gate equivalences and conversions
- [ ] Positive and negative logic
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 📊 Karnaugh Maps (K-maps)
- [ ] 2-variable, 3-variable, 4-variable K-maps
- [ ] Grouping rules (groups must be powers of 2, rectangular/square)
- [ ] Essential prime implicants, prime implicants
- [ ] Don't care conditions
- [ ] Minimization to SOP and POS forms
- [ ] 5-variable K-maps (overview)
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🔧 Combinational Circuits
- [ ] Adders: half adder, full adder, ripple carry, carry look-ahead
- [ ] Subtractors: half, full
- [ ] Multiplexer (MUX): 2:1, 4:1, 8:1; implementing functions using MUX
- [ ] Demultiplexer (DEMUX)
- [ ] Encoder, Decoder (priority encoder)
- [ ] Comparators
- [ ] ROM, PLA, PAL implementations
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### ⏱️ Sequential Circuits
- [ ] SR latch, gated SR latch, D latch
- [ ] Flip-flops: SR, D, JK, T
- [ ] Excitation tables for each flip-flop
- [ ] Characteristic equations for each flip-flop
- [ ] Conversion between flip-flops
- [ ] Master-slave flip-flops
- [ ] Registers: parallel load, shift register (SISO, SIPO, PISO, PIPO)
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🔢 Counters
- [ ] Ripple (asynchronous) counter
- [ ] Synchronous counter
- [ ] Mod-N counter design
- [ ] Ring counter, Johnson counter
- [ ] Up/down counter
- [ ] Binary, BCD counters
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🧪 Finite State Machines (FSM)
- [ ] Moore machine: output depends on state only
- [ ] Mealy machine: output depends on state and input
- [ ] State diagrams, state tables
- [ ] State minimization (merging equivalent states)
- [ ] FSM design procedure
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

---

## 📋 Key Formulas & Laws

### Boolean Laws
```
Identity:      A + 0 = A;  A · 1 = A
Null:          A + 1 = 1;  A · 0 = 0
Idempotent:    A + A = A;  A · A = A
Complement:    A + A' = 1; A · A' = 0
Double complement: (A')' = A
Commutative:   A + B = B + A; A · B = B · A
Associative:   (A+B)+C = A+(B+C)
Distributive:  A(B+C) = AB + AC; A+BC = (A+B)(A+C)
Absorption:    A + AB = A; A(A+B) = A
De Morgan's:   (A+B)' = A'B'; (AB)' = A'+B'
```

### Flip-Flop Characteristic Equations
```
SR FF: Q(t+1) = S + R'Q  [SR = 0 undefined]
D FF:  Q(t+1) = D
JK FF: Q(t+1) = JQ' + K'Q
T FF:  Q(t+1) = T⊕Q = TQ' + T'Q
```

### Excitation Tables

| Q(t) | Q(t+1) | D | T | S | R | J | K |
|------|--------|---|---|---|---|---|---|
| 0 | 0 | 0 | 0 | 0 | X | 0 | X |
| 0 | 1 | 1 | 1 | 1 | 0 | 1 | X |
| 1 | 0 | 0 | 1 | 0 | 1 | X | 1 |
| 1 | 1 | 1 | 0 | X | 0 | X | 0 |

---

## ⚠️ Common Mistakes

1. **K-map grouping:** Groups must be rectangular, powers of 2, and as large as possible
2. **Prime implicant vs. essential PI:** A prime implicant is essential if it's the only one covering a minterm
3. **Flip-flop excitation vs. characteristic:** Excitation: given Q(t) and Q(t+1), find inputs; Characteristic: given inputs, find Q(t+1)
4. **MUX as function generator:** With n data select lines, you can implement any function of n+1 variables
5. **SR latch forbidden state:** S=R=1 is forbidden; undefined/invalid
6. **Synchronous vs. asynchronous counter:** Synchronous: all FFs clock simultaneously; Async: ripple effect
7. **Moore vs. Mealy:** Moore is more predictable; Mealy can have fewer states for same function
8. **Don't care in K-map:** Can be treated as either 0 or 1 to maximize grouping

---

## 📈 PYQ Frequency Analysis

| Topic | Frequency |
|-------|-----------|
| K-map minimization | Every year |
| Flip-flops and excitation | Most years |
| Combinational circuit design | Most years |
| Counter design | Some years |
| Boolean simplification | Most years |

---

## 📚 Resources

- **Primary:** Digital Design — Morris Mano
- **Video:** Neso Academy Digital Electronics (YouTube)
- **Practice:** GATE Overflow Digital Logic tag

---

## 📅 PYQ Progress Tracker

- [ ] PYQs 2020–2026 solved
- [ ] PYQs 2015–2019 solved
- [ ] PYQs 2010–2014 solved

---

*Updated: ___ | Revision Count: ___*
