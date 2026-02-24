# 💡 Digital Logic

![Weightage](https://img.shields.io/badge/Weightage-4–6%20marks-yellow)
![Priority](https://img.shields.io/badge/Priority-Medium-yellow)

---

## 📋 Topic Checklist

### 🔷 Number Systems
- [ ] Binary, Octal, Decimal, Hexadecimal — conversions
- [ ] Binary arithmetic: addition, subtraction, multiplication, division
- [ ] 1's complement and 2's complement arithmetic
- [ ] Overflow detection in 2's complement
- [ ] BCD (8421 code), Excess-3 code, Gray code
- [ ] Gray code to binary and binary to Gray code

### 🔷 Boolean Algebra
- [ ] Basic postulates: identity, null, idempotent, complement
- [ ] Boolean theorems: absorption, De Morgan's, consensus
- [ ] SOP (Sum of Products) canonical form — minterms
- [ ] POS (Product of Sums) canonical form — maxterms
- [ ] Minterm ↔ Maxterm duality: mᵢ = Mᵢ (complement)
- [ ] Duality principle

### 🔷 Logic Gates
- [ ] Basic gates: NOT, AND, OR, NAND, NOR, XOR, XNOR
- [ ] Universal gates: NAND and NOR can implement any gate
- [ ] Implementing basic gates using NAND only
- [ ] Implementing basic gates using NOR only
- [ ] Timing diagrams

### 🔷 Karnaugh Maps (K-Maps)
- [ ] 2-variable, 3-variable, 4-variable K-maps
- [ ] Grouping: pairs (2¹), quads (2²), octets (2³)
- [ ] Essential prime implicants
- [ ] Don't-care conditions
- [ ] Minimization using K-maps (SOP and POS forms)
- [ ] 5-variable K-maps (conceptual)

### 🔷 Combinational Circuits
- [ ] Half adder: S = A⊕B, C = AB
- [ ] Full adder: S = A⊕B⊕Cin, Cout = AB + BCin + ACin
- [ ] Ripple Carry Adder — propagation delay
- [ ] Carry Lookahead Adder — faster, uses generate and propagate
- [ ] Half subtractor and full subtractor
- [ ] BCD adder
- [ ] 4-to-1 MUX: truth table and circuit
- [ ] 8-to-1 MUX, 2-to-1 MUX
- [ ] Using MUX to implement any function
- [ ] Demultiplexer (DEMUX / Decoder)
- [ ] Encoder, Priority encoder
- [ ] 7-segment display decoder

### 🔷 Sequential Circuits
- [ ] Latches:
  - [ ] SR latch (NOR-based, NAND-based)
  - [ ] Gated SR latch
  - [ ] D latch
- [ ] Flip-flops:
  - [ ] SR flip-flop (clocked)
  - [ ] D flip-flop (data flip-flop)
  - [ ] JK flip-flop — no undefined state
  - [ ] T flip-flop (toggle)
- [ ] Characteristic equations:
  - [ ] D FF: Q(t+1) = D
  - [ ] T FF: Q(t+1) = T⊕Q
  - [ ] JK FF: Q(t+1) = JQ' + K'Q
  - [ ] SR FF: Q(t+1) = S + K'Q (when S·R=0)
- [ ] Flip-flop conversions (D to JK, JK to D, etc.)
- [ ] Master-slave flip-flop

### 🔷 Registers & Counters
- [ ] Shift registers: SISO, SIPO, PISO, PIPO
- [ ] Bidirectional shift register
- [ ] Ring counter and Johnson (twisted ring) counter
- [ ] Asynchronous (ripple) counter
- [ ] Synchronous counter
- [ ] Modulo-N counter design
- [ ] Up/down counter

### 🔷 Finite State Machines
- [ ] Moore machine — output depends on state
- [ ] Mealy machine — output depends on state and input
- [ ] State diagram and state table
- [ ] State minimization
- [ ] Converting Mealy to Moore and vice versa

---

## ⚡ Key Formulas & Quick Reference

### Boolean Identities
```
Absorption:  A + AB = A,    A(A+B) = A
De Morgan's: (A+B)' = A'B', (AB)' = A'+B'
XOR:         A⊕B = AB' + A'B = (A+B)(A'+B')
XNOR:        A⊙B = AB + A'B' = (A⊕B)'
```

### Minterm / Maxterm
```
For n variables, there are 2ⁿ minterms and 2ⁿ maxterms

Sum of Minterms (SOM) = Product of Maxterms (POM) complement
f(A,B,C) = Σm(0,1,3) = ΠM(2,4,5,6,7)
```

### Full Adder
```
Sum  = A ⊕ B ⊕ Cin
Cout = AB + Cin(A ⊕ B)
```

### JK Flip-Flop
```
Q(t+1) = JQ' + K'Q

J=0, K=0 → Hold  (Q → Q)
J=0, K=1 → Reset (Q → 0)
J=1, K=0 → Set   (Q → 1)
J=1, K=1 → Toggle (Q → Q')
```

### Moore vs Mealy
```
Moore: output = f(current state only) → output changes on clock edge
Mealy: output = f(current state, input) → output can change asynchronously
Moore needs more states than Mealy for same behavior
```

---

## ❌ Common Mistakes

| Mistake | Correct Understanding |
|---|---|
| NAND of inputs = NOR | NAND(A,B) = A'+B'; NOR(A,B) = A'·B' — different |
| Groups in K-map can be any size | Groups MUST be powers of 2: 1, 2, 4, 8, 16 |
| Ripple counter is faster | Ripple counter is SLOWER due to propagation; synchronous is faster |
| JK FF: J=K=0 toggles | J=K=0 holds; J=K=1 toggles |
| D latch = D flip-flop | Latch is level-triggered; flip-flop is edge-triggered |
| Don't-care = 0 always | Don't-cares can be treated as 0 or 1 for minimization |

---

## 📊 PYQ Frequency Analysis (2015–2024)

| Topic | Frequency | Marks Range |
|---|:---:|:---:|
| K-map minimization | High (every year) | 1–2 |
| Flip-flop conversions | High | 1–2 |
| Counter design | High | 1–2 |
| MUX / DEMUX implementation | Medium | 1 |
| Boolean algebra simplification | Medium | 1 |
| Sequential circuit design | Medium | 1–2 |

---

## 🎯 Confidence Tracker

| Topic | Confidence | Last Revised |
|---|:---:|---|
| Boolean Algebra | ☐ Low / ☐ Med / ☐ High | |
| K-maps | ☐ Low / ☐ Med / ☐ High | |
| Flip-flops | ☐ Low / ☐ Med / ☐ High | |
| Combinational Circuits | ☐ Low / ☐ Med / ☐ High | |
| Counters / Registers | ☐ Low / ☐ Med / ☐ High | |
