# CISSP Formula & Quick Reference Cheatsheet

> This is your daily reference card. Aim to recall every formula here without looking.

---

## Risk Management Formulas

```
SLE  = Asset Value × Exposure Factor (EF)
ALE  = SLE × ARO
Residual Risk = Total Risk × Controls Gap

Value of Safeguard = (ALE before safeguard) − (ALE after safeguard) − (Annual cost of safeguard)

Implement safeguard only if:  ALE before > ALE after + Annual cost
```

| Term | Full Name | Meaning |
|------|-----------|---------|
| AV | Asset Value | Dollar value of the asset |
| EF | Exposure Factor | % of asset lost per incident (0.0–1.0) |
| SLE | Single Loss Expectancy | Cost of ONE occurrence |
| ARO | Annualised Rate of Occurrence | How often per year (0.1 = once per 10 yrs) |
| ALE | Annualised Loss Expectancy | Expected annual loss |

### Worked Example
- Server worth: $500,000
- Ransomware encrypts 80% of data → EF = 0.80
- SLE = $500,000 × 0.80 = **$400,000**
- Expected once every 2 years → ARO = 0.5
- ALE = $400,000 × 0.5 = **$200,000/year**
- EDR solution costs $50,000/year; reduces ALE to $20,000
- Value = $200,000 − $20,000 − $50,000 = **$130,000 net benefit → implement it**

---

## Symmetric Key Count Formula

```
Number of symmetric keys needed for N users = N(N-1) / 2
```

| Users | Keys Needed |
|-------|------------|
| 2 | 1 |
| 5 | 10 |
| 10 | 45 |
| 100 | 4,950 |

> This shows why symmetric key management doesn't scale — asymmetric solves this.

---

## Biometrics

```
Lower CER = More accurate system

If you reduce FAR → FRR increases (and vice versa)
CER = point where FAR = FRR
```

| Acronym | Full Name | Good or Bad? |
|---------|-----------|-------------|
| FAR / Type II Error | False Acceptance Rate | Bad — impostor accepted |
| FRR / Type I Error | False Rejection Rate | Bad — valid user rejected |
| CER | Crossover Error Rate | Lower = better accuracy |

---

## OSI Model Quick Reference

| # | Layer | Protocols | Device | Encapsulation |
|---|-------|-----------|--------|---------------|
| 7 | Application | HTTP, FTP, SMTP, DNS, SNMP | Gateway | Data |
| 6 | Presentation | TLS, SSL, JPEG, GIF | — | Data |
| 5 | Session | NetBIOS, RPC, NFS, SQL | — | Data |
| 4 | Transport | TCP, UDP, SSL | — | Segment |
| 3 | Network | IP, ICMP, OSPF, RIP | Router | Packet |
| 2 | Data Link | Ethernet, ARP, PPP, FDDI | Switch, Bridge | Frame |
| 1 | Physical | Coax, Fibre, Copper | Hub, Repeater | Bits |

---

## Common Port Numbers

| Port | Protocol | Note |
|------|---------|------|
| 20/21 | FTP | 20=data, 21=control |
| 22 | SSH | Encrypted remote access |
| 23 | Telnet | Unencrypted — avoid |
| 25 | SMTP | Email sending |
| 53 | DNS | Name resolution |
| 80 | HTTP | Unencrypted web |
| 110 | POP3 | Email retrieval |
| 143 | IMAP | Email retrieval (leaves on server) |
| 161/162 | SNMP | Network monitoring |
| 389 | LDAP | Directory access |
| 443 | HTTPS | Encrypted web |
| 636 | LDAPS | Encrypted directory |
| 3389 | RDP | Remote desktop |

---

## Cryptography Quick Reference

| Algorithm | Type | Key Size | Current Status |
|-----------|------|---------|---------------|
| DES | Symmetric block | 56-bit | Broken — obsolete |
| 3DES | Symmetric block | 112/168-bit | Deprecated |
| AES-128 | Symmetric block | 128-bit | Acceptable |
| AES-256 | Symmetric block | 256-bit | Current standard |
| RSA-2048 | Asymmetric | 2048-bit | Current minimum |
| ECC-256 | Asymmetric | 256-bit | Efficient, current |
| MD5 | Hash | 128-bit | Broken — collision attacks |
| SHA-1 | Hash | 160-bit | Deprecated |
| SHA-256 | Hash | 256-bit | Current standard |

---

## Security Model Quick Reference

| Model | Protects | Rule 1 | Rule 2 |
|-------|---------|--------|--------|
| Bell-LaPadula | Confidentiality | No read UP | No write DOWN |
| Biba | Integrity | No read DOWN | No write UP |
| Clark-Wilson | Integrity | Separation of duties | Audit trails required |
| Brewer-Nash | Conflicts of interest | No access to competing data | Dynamic based on history |

---

## Fire Classes

| Class | Fuel | Suppression |
|-------|------|------------|
| A | Wood, paper, fabric | Water, soda acid |
| B | Liquids, petroleum, gases | CO2, halon substitute, dry chemical |
| C | Electrical equipment | CO2, halon substitute (NEVER water) |
| D | Combustible metals | Dry powder (specific to metal) |

---

## Recovery Site Comparison

| Site | Readiness | RTO | Cost |
|------|-----------|-----|------|
| Hot | Fully operational | Hours | Highest |
| Warm | Hardware ready, needs config | Days | Medium |
| Cold | Shell building only | Weeks | Lowest |

---

## Backup Types

| Type | Backs Up | Clears Archive Bit | Restore Time |
|------|---------|-------------------|-------------|
| Full | Everything | Yes | Fastest (one set) |
| Incremental | Since last backup (any type) | Yes | Slowest (full + all incrementals) |
| Differential | Since last full backup | No | Medium (full + one differential) |
