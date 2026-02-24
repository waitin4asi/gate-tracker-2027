# 🌐 Computer Networks

![Weightage](https://img.shields.io/badge/Weightage-6–8%20marks-orange)
![Priority](https://img.shields.io/badge/Priority-High-orange)

---

## 📋 Topic Checklist

### 🔷 Network Models
- [ ] OSI 7-layer model — functions of each layer
- [ ] TCP/IP model — 5-layer model and comparison
- [ ] Encapsulation and decapsulation
- [ ] PDU names: segment, packet, frame, bit

### 🔷 Physical Layer
- [ ] Transmission modes: simplex, half-duplex, full-duplex
- [ ] Bandwidth and throughput
- [ ] Nyquist theorem (noiseless channel)
- [ ] Shannon's theorem (noisy channel)
- [ ] Encoding: NRZ, Manchester, differential Manchester
- [ ] Multiplexing: FDM, TDM, WDM, CDMA

### 🔷 Data Link Layer
- [ ] Framing methods: character count, byte stuffing, bit stuffing
- [ ] Error detection: parity, CRC (Cyclic Redundancy Check), checksum
- [ ] Error correction: Hamming code
- [ ] Flow control protocols:
  - [ ] Stop and Wait
  - [ ] Go-Back-N (GBN)
  - [ ] Selective Repeat (SR)
- [ ] Efficiency formulas for sliding window protocols
- [ ] Medium Access Control (MAC):
  - [ ] CSMA/CD (Ethernet)
  - [ ] CSMA/CA (Wi-Fi / 802.11)
  - [ ] Token Ring / Token Bus
- [ ] Ethernet: frame format, collision domain

### 🔷 Network Layer
- [ ] IP addressing: IPv4 (32-bit), IPv6 (128-bit)
- [ ] Subnetting and CIDR notation
- [ ] Supernetting / route aggregation
- [ ] Classful addressing (A, B, C, D, E)
- [ ] Classless addressing (CIDR)
- [ ] Private IP ranges
- [ ] IP datagram format (header fields)
- [ ] Routing algorithms:
  - [ ] Distance Vector Routing (Bellman-Ford, RIP)
  - [ ] Link State Routing (Dijkstra, OSPF)
- [ ] ICMP, ARP, RARP
- [ ] NAT (Network Address Translation)
- [ ] Fragmentation and reassembly

### 🔷 Transport Layer
- [ ] UDP — connectionless, unreliable, lightweight
- [ ] TCP — connection-oriented, reliable, full-duplex
- [ ] TCP 3-way handshake (SYN, SYN-ACK, ACK)
- [ ] TCP connection termination (4-way: FIN, FIN-ACK)
- [ ] TCP flow control — sliding window
- [ ] TCP congestion control:
  - [ ] Slow start
  - [ ] Congestion avoidance
  - [ ] Fast retransmit and fast recovery
  - [ ] AIMD (Additive Increase Multiplicative Decrease)
- [ ] TCP vs UDP comparison table

### 🔷 Application Layer
- [ ] DNS — hierarchy, resolution process
- [ ] HTTP / HTTPS — request/response, stateless
- [ ] FTP — data and control connection
- [ ] SMTP, POP3, IMAP (email protocols)
- [ ] DHCP — dynamic IP assignment
- [ ] SNMP — network management

### 🔷 Network Security (Basics)
- [ ] Symmetric vs asymmetric encryption
- [ ] RSA, DES, AES (conceptual overview)
- [ ] Diffie-Hellman key exchange
- [ ] Digital signatures and certificates
- [ ] SSL/TLS

---

## ⚡ Key Formulas

### Sliding Window Protocols
```
Stop and Wait Efficiency:    η = 1 / (1 + 2a)
                               where a = propagation delay / transmission time

Go-Back-N (GBN):
  Window size ≤ 2^n − 1
  Efficiency = W / (1 + 2a)  if W < (1 + 2a)
             = 1              if W ≥ (1 + 2a)

Selective Repeat (SR):
  Window size ≤ 2^(n-1)
  Efficiency = W / (1 + 2a)  if W < (1 + 2a)
             = 1              if W ≥ (1 + 2a)
```

### Propagation and Transmission
```
Transmission time  = (Message size) / (Bandwidth)
Propagation delay  = (Distance) / (Speed of signal)
Total latency      = Transmission time + Propagation delay + Queuing delay
Throughput         = (Data transferred) / (Total time)
```

### Subnetting
```
Subnet mask of /n  → first n bits are 1s, rest are 0s
Number of hosts per subnet = 2^(32-n) − 2  (subtract network + broadcast)
Number of subnets  = 2^(bits borrowed)
```

### CRC
```
Sender: append (n-1) zeros to message, divide by generator polynomial
        Send message with remainder (checksum) appended
Receiver: divide received frame by generator; if remainder = 0, no error
```

### Shannon's Theorem
```
C = B × log₂(1 + S/N)
Where C = capacity (bps), B = bandwidth (Hz), S/N = signal-to-noise ratio
```

---

## ❌ Common Mistakes

| Mistake | Correct Understanding |
|---|---|
| GBN and SR same window size | GBN: 2^n−1; SR: 2^(n-1) — SR is half of GBN |
| IPv6 = 64-bit | IPv6 is 128-bit |
| TCP handshake is 4-way | TCP connection is 3-way; termination is 4-way |
| ARP resolves IP from domain | ARP resolves MAC from IP; DNS resolves IP from domain |
| CSMA/CD used in Wi-Fi | CSMA/CA used in Wi-Fi; CSMA/CD in Ethernet |
| Class A private: 10.0.0.0/8 | Private ranges: 10.x, 172.16–31.x, 192.168.x.x |

---

## 📊 PYQ Frequency Analysis (2015–2024)

| Topic | Frequency | Marks Range |
|---|:---:|:---:|
| Sliding Window Protocols | Very High (every year) | 1–2 |
| Subnetting / IP Addressing | Very High | 1–2 |
| TCP Congestion Control | High | 1–2 |
| Routing Algorithms | High | 1–2 |
| CRC / Error Detection | Medium | 1 |
| DNS / Application Layer | Medium | 1 |

---

## 🎯 Confidence Tracker

| Topic | Confidence | Last Revised |
|---|:---:|---|
| Sliding Window | ☐ Low / ☐ Med / ☐ High | |
| IP Addressing / Subnetting | ☐ Low / ☐ Med / ☐ High | |
| TCP/UDP | ☐ Low / ☐ Med / ☐ High | |
| Routing | ☐ Low / ☐ Med / ☐ High | |
| Error Detection/Correction | ☐ Low / ☐ Med / ☐ High | |
