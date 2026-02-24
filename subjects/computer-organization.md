# 🖥️ Computer Organization & Architecture (COA)

![Weightage](https://img.shields.io/badge/Weightage-5–7%20marks-orange)
![Priority](https://img.shields.io/badge/Priority-High-orange)

---

## 📋 Topic Checklist

### 🔷 Number Systems & Data Representation
- [ ] Binary, Octal, Hexadecimal conversions
- [ ] Signed representation: sign-magnitude, 1's complement, 2's complement
- [ ] Fixed-point representation
- [ ] IEEE 754 floating-point: single precision (32-bit), double precision (64-bit)
- [ ] Floating-point operations and rounding errors
- [ ] BCD (Binary Coded Decimal)
- [ ] Character codes: ASCII, Unicode

### 🔷 Boolean Algebra & Logic Gates
- [ ] Basic gates: AND, OR, NOT, NAND, NOR, XOR, XNOR
- [ ] Boolean laws and theorems
- [ ] De Morgan's theorems
- [ ] SOP (Sum of Products) and POS (Product of Sums)
- [ ] Karnaugh Maps (K-maps): 2, 3, 4 variable
- [ ] Quine-McCluskey method (tabular minimization)
- [ ] Universal gates: NAND and NOR

### 🔷 Combinational Circuits
- [ ] Adders: half adder, full adder, ripple carry adder, carry lookahead adder
- [ ] Subtractors: using 2's complement
- [ ] Multiplexers (MUX) and Demultiplexers (DEMUX)
- [ ] Encoders and Decoders
- [ ] Comparators

### 🔷 Sequential Circuits
- [ ] Latches: SR latch (NOR, NAND)
- [ ] Flip-flops: SR, D, JK, T
- [ ] Flip-flop conversions
- [ ] Registers: shift registers (SISO, SIPO, PISO, PIPO)
- [ ] Counters: synchronous, asynchronous (ripple), modulo-N counters
- [ ] Finite state machines: Moore vs Mealy

### 🔷 Processor Organization
- [ ] Von Neumann architecture
- [ ] Instruction cycle: fetch, decode, execute
- [ ] Registers: PC, MAR, MDR, IR, ACC, SP
- [ ] ALU operations
- [ ] Data path and control path
- [ ] Control unit design: hardwired vs microprogrammed

### 🔷 Instruction Set Architecture (ISA)
- [ ] Instruction formats: zero, one, two, three address
- [ ] Addressing modes:
  - [ ] Immediate, Direct, Indirect
  - [ ] Register, Register Indirect
  - [ ] Displacement (base register, PC-relative, indexed)
- [ ] RISC vs CISC comparison
- [ ] Little-endian vs big-endian

### 🔷 Memory Hierarchy
- [ ] Registers → Cache → RAM → Disk
- [ ] Cache memory — direct mapping, set-associative, fully-associative
- [ ] Cache replacement policies: LRU, FIFO, LFU, Random
- [ ] Write policies: write-through, write-back
- [ ] Cache miss types: cold miss, conflict miss, capacity miss
- [ ] Effective memory access time (cache + main memory)
- [ ] Virtual memory — page table, TLB (see OS subject)
- [ ] Main memory — DRAM, SRAM

### 🔷 Pipelining
- [ ] Instruction pipeline stages: IF, ID, EX, MEM, WB
- [ ] Pipeline throughput and speedup
- [ ] Pipeline hazards:
  - [ ] Structural hazards — resource conflicts
  - [ ] Data hazards — RAW, WAW, WAR dependencies
  - [ ] Control hazards — branch prediction
- [ ] Hazard resolution: stalling (bubbles), forwarding, branch prediction
- [ ] Pipeline performance with stalls

### 🔷 I/O Organization
- [ ] I/O interfacing — programmed I/O, interrupt-driven I/O, DMA
- [ ] Interrupts — vectored, non-vectored, priority
- [ ] DMA (Direct Memory Access)
- [ ] I/O buses and protocols

---

## ⚡ Key Formulas

### Performance Equations
```
CPU Time = Instruction Count × CPI × Clock Cycle Time
         = (IC × CPI) / Clock Rate

MIPS = Clock Rate / (CPI × 10⁶)

Speedup = Performance_new / Performance_old
        = Execution_time_old / Execution_time_new

Amdahl's Law: Speedup = 1 / [(1-f) + f/S]
  Where f = fraction of task that can be parallelized
        S = speedup of that fraction
```

### Cache Performance
```
AMAT = Hit time + Miss rate × Miss penalty
     = h × T_cache + (1-h) × T_main

Where h = cache hit rate, T_cache = cache access time, T_main = main memory time

For multi-level cache:
AMAT = L1 hit time + L1 miss rate × (L2 hit time + L2 miss rate × L2 miss penalty)
```

### Pipeline Speedup
```
Ideal speedup = Number of stages (k)

With stalls:
CPI_pipeline = 1 + stalls per instruction

Pipeline speedup = (CPI_non-pipelined) / (CPI_pipelined)
                 ≈ k / (1 + stall_rate × stall_cycles)
```

### IEEE 754 (Single Precision)
```
32 bits: 1 sign | 8 exponent | 23 mantissa
Biased exponent: actual + 127
Value = (-1)^sign × 1.mantissa × 2^(exponent - 127)
```

---

## ❌ Common Mistakes

| Mistake | Correct Understanding |
|---|---|
| 2's complement range | For n bits: −2^(n-1) to 2^(n-1)−1 |
| Direct mapped = 1-way | Direct mapped = 1-way set associative |
| Pipeline speedup always = k | Only ideal; stalls reduce it |
| WAR is a true dependency | RAW is true dependency; WAR/WAW are false (anti/output) |
| Write-through = always better | Write-back is faster but needs dirty bit tracking |
| Cache miss = always bad | Cold misses are unavoidable; focus on reducing conflict misses |

---

## 📊 PYQ Frequency Analysis (2015–2024)

| Topic | Frequency | Marks Range |
|---|:---:|:---:|
| Cache memory calculations | Very High (every year) | 1–3 |
| Pipeline performance | Very High | 1–2 |
| Addressing modes | High | 1 |
| IEEE 754 floating point | High | 1–2 |
| Number representations | Medium | 1 |
| I/O and DMA | Low | 1 |

---

## 🎯 Confidence Tracker

| Topic | Confidence | Last Revised |
|---|:---:|---|
| Number Systems | ☐ Low / ☐ Med / ☐ High | |
| Cache Memory | ☐ Low / ☐ Med / ☐ High | |
| Pipelining | ☐ Low / ☐ Med / ☐ High | |
| Addressing Modes | ☐ Low / ☐ Med / ☐ High | |
| ISA / Performance | ☐ Low / ☐ Med / ☐ High | |
