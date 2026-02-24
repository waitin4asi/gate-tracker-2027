# 🖥️ Computer Organization & Architecture (COA)

> **Weightage:** ~8% | **Avg Questions:** 5–7 | **Importance:** ⭐⭐⭐⭐⭐

---

## 📊 Overview

COA is heavily numerical — cache calculations, pipeline hazards, and memory hierarchy dominate. Once you master the formulas and concepts, these become reliable scoring questions.

**Scoring Pattern:**
- 1–2 questions on Cache (hit rate, effective access time)
- 1–2 questions on Pipelining (speedup, hazards)
- 1 question on Number Systems / Arithmetic
- 1 question on Memory Organization
- 0–1 questions on I/O organization

---

## ✅ Topic-wise Checklist

### 🔢 Number Systems & Data Representation
- [ ] Binary, octal, hexadecimal conversions
- [ ] Signed representation: sign-magnitude, 1's complement, 2's complement
- [ ] BCD, Gray code
- [ ] Floating point representation (IEEE 754)
  - [ ] Single precision (32-bit): 1 sign + 8 exponent + 23 mantissa
  - [ ] Double precision (64-bit): 1 sign + 11 exponent + 52 mantissa
  - [ ] Biased exponent (127 for single), NaN, infinity
- [ ] Integer overflow detection
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🔣 Computer Arithmetic
- [ ] Addition and subtraction (2's complement)
- [ ] Multiplication: Booth's algorithm
- [ ] Division algorithms (restoring, non-restoring)
- [ ] Floating point addition/subtraction (alignment, rounding)
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### ⚡ ALU Design
- [ ] Half adder, full adder
- [ ] Ripple carry adder, carry look-ahead adder
- [ ] Subtractor using 2's complement
- [ ] Overflow detection in signed addition
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🧠 CPU Design
- [ ] CPU components: ALU, control unit, registers, buses
- [ ] Instruction cycle: fetch, decode, execute
- [ ] Instruction formats: zero, one, two, three address
- [ ] Addressing modes: immediate, direct, indirect, register, register indirect, autoincrement
- [ ] Instruction set architecture (ISA): RISC vs. CISC
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🏎️ Pipelining
- [ ] Pipeline stages (typically 5: IF, ID, EX, MEM, WB)
- [ ] Speedup formula: ideal and real
- [ ] Pipeline hazards:
  - [ ] Structural hazards: resource conflicts
  - [ ] Data hazards: RAW, WAR, WAW
  - [ ] Control hazards: branch prediction
- [ ] Hazard resolution: stalls (bubbles), forwarding/bypassing
- [ ] Branch prediction: static (predict taken/not taken), dynamic (2-bit counter)
- [ ] Effective CPI with stalls
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 💾 Memory Hierarchy
- [ ] Memory types: SRAM, DRAM, ROM types
- [ ] Memory hierarchy: registers → L1 cache → L2 cache → Main memory → Secondary
- [ ] Locality of reference: temporal and spatial
- [ ] Cache memory organization
- [ ] Cache mapping:
  - [ ] Direct mapped: block → specific cache line
  - [ ] Fully associative: block → any cache line
  - [ ] Set-associative: k-way set associative
- [ ] Cache replacement policies: LRU, FIFO, Random
- [ ] Write policies: write-through, write-back, write-allocate
- [ ] Effective memory access time (EMAT)
- [ ] Virtual memory — TLB (covered in OS)
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 📥 I/O Organization
- [ ] I/O interfaces: programmed I/O, interrupt-driven I/O, DMA
- [ ] DMA: cycle stealing, burst mode
- [ ] Interrupt handling: maskable, non-maskable, priority
- [ ] Buses: synchronous, asynchronous; address, data, control buses
- [ ] Bus arbitration: daisy chaining, centralized, distributed
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

---

## 📋 Key Formulas

### Pipelining
```
Ideal speedup = Number of stages (k)
Real speedup = (k × n) / (k + n - 1)  [n = instructions, k = stages]
Clock cycles for n instructions = k + (n-1) = n + k - 1
Throughput = n / (n + k - 1) cycles × clock period
CPI (ideal) = 1
CPI (with stalls) = 1 + stalls per instruction
```

### Cache Performance
```
EMAT = Hit rate × Cache time + Miss rate × (Cache time + Memory time)
    [or with write-through: hit rate × cache + miss rate × memory]
Miss rate = 1 - Hit rate

For multi-level cache:
EMAT = L1 hit time + L1 miss rate × (L2 hit time + L2 miss rate × Main memory time)

Cache size = Number of sets × Set associativity × Block size
```

### Cache Addressing
```
Physical address bits = Tag bits + Index bits + Offset bits
Offset bits = log₂(block size in bytes)
Index bits = log₂(number of sets)  [for k-way set assoc: sets = cache_lines / k]
Tag bits = remaining bits
```

### Memory
```
Memory size = 2^(address bits) bytes
Number of address lines needed = log₂(memory size)
RAM chips needed = (Memory size × width) / (chip size × chip width)
```

### IEEE 754 Single Precision
```
Value = (-1)^sign × 2^(exponent-127) × 1.mantissa
Normalized: 1.mantissa (implicit leading 1)
Denormalized: 0.mantissa (when exponent = 0)
Infinity: exponent = 255, mantissa = 0
NaN: exponent = 255, mantissa ≠ 0
```

---

## ⚠️ Common Mistakes

1. **Pipeline speedup:** Real speedup ≠ number of stages due to pipeline fill/drain
2. **Cache index calculation:** For set-associative, number of sets = total lines / ways
3. **Direct mapped vs. fully associative:** Same block size but different conflict behavior
4. **Data hazard types:** RAW (true dependency), WAR (anti-dependency), WAW (output dependency)
5. **Write-through vs. write-back:** Write-back is faster but may lose data on crash
6. **Booth's multiplication:** Works for signed numbers; handles negative multiplier
7. **IEEE 754 exponent bias:** Single = 127, Double = 1023
8. **DMA:** DMA steals bus cycles; CPU doesn't know about individual DMA operations

---

## 📈 PYQ Frequency Analysis

| Topic | Frequency |
|-------|-----------|
| Cache calculations (EMAT, hit rate) | Every year |
| Pipelining (speedup, hazards) | Every year |
| Number representation / IEEE 754 | Most years |
| Addressing modes | Most years |
| Memory organization | Some years |

---

## 📚 Resources

- **Primary:** Computer Organization — Carl Hamacher
- **Alternate:** Computer Organization & Design — Patterson & Hennessy
- **Video:** Neso Academy — COA playlist
- **Practice:** GATE Overflow COA tag

---

## 📅 PYQ Progress Tracker

- [ ] PYQs 2020–2026 solved
- [ ] PYQs 2015–2019 solved
- [ ] PYQs 2010–2014 solved

---

*Updated: ___ | Revision Count: ___*
