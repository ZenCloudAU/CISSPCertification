# Domain 3: Security Architecture & Engineering

**Exam Weight:** 13%  
**Study Time:** ~10–14 hours  
**Mindset:** Security must be built in, not bolted on. Architecture decisions have long-term consequences.

---

## 3.1 Security Models

Security models provide a theoretical framework that security policies are built on.

### Bell-LaPadula Model (Confidentiality)
Designed for military environments. Protects **confidentiality**.

| Rule | Meaning | Memory Hook |
|------|---------|-------------|
| **Simple Security Rule** | No read up | Subjects can't read data at a higher classification |
| **Star (*) Property Rule** | No write down | Subjects can't write data to a lower classification |
| **Strong Star Property** | Read/write only at same level | Full restriction |

> **Limitation:** Does not address integrity. Does not handle modern file sharing.

### Biba Model (Integrity)
Mirror image of Bell-LaPadula. Protects **integrity**.

| Rule | Meaning | Memory Hook |
|------|---------|-------------|
| **Simple Integrity Axiom** | No read down | Subjects can't read lower integrity data (prevents corruption) |
| **Star (*) Integrity Axiom** | No write up | Subjects can't modify higher integrity objects |

> **Memory trick:** Bell-LaPadula = Confidentiality = military. Biba = Integrity = commercial.

### Clark-Wilson Model (Integrity — Commercial)
Designed for commercial environments. Enforces integrity through:
- **Separation of duties** — no single person can complete a transaction alone
- **Audit trails** — all transactions are logged
- **Well-formed transactions** — data can only be modified through authorised programs
- Access triple: **Subject → Program → Object**

### Brewer-Nash Model (Chinese Wall)
- Prevents **conflicts of interest**
- Access controls change based on prior access history
- Common in financial/legal environments (e.g. can't access Coca-Cola data if you've accessed Pepsi data)

### Quick Comparison

| Model | Protects | Key Concept |
|-------|---------|------------|
| Bell-LaPadula | Confidentiality | No read up, no write down |
| Biba | Integrity | No read down, no write up |
| Clark-Wilson | Integrity | Transactions, separation of duties |
| Brewer-Nash | Conflict of interest | Dynamic access based on history |

---

## 3.2 Trusted Computing Base (TCB)

The **TCB** is the total combination of protection mechanisms in a system (hardware, software, firmware) that are responsible for enforcing the security policy.

### Key Components

| Component | Description |
|-----------|-------------|
| **Security Perimeter** | Boundary dividing trusted from untrusted components |
| **Reference Monitor** | Abstract concept — mediates all access between subjects and objects |
| **Security Kernel** | Hardware/software/firmware implementation of the reference monitor |

### Protection Rings

```
Ring 0: OS Kernel          ← Most privileged
Ring 1: Remaining OS
Ring 2: I/O Drivers & Utilities
Ring 3: Applications       ← Least privileged
```

Processes in inner rings can access outer rings. Processes in outer rings CANNOT access inner rings without permission.

---

## 3.3 Cryptography

### Symmetric vs Asymmetric

| | Symmetric | Asymmetric |
|-|-----------|-----------|
| Keys | One shared key | Public + private key pair |
| Speed | Fast | Slow |
| Key distribution | Out-of-band required | Public key distributed freely |
| Use | Bulk data encryption | Key exchange, digital signatures |
| Examples | AES, DES, 3DES, Blowfish | RSA, ECC, Diffie-Hellman |

### Common Algorithms

| Algorithm | Type | Key Size | Notes |
|-----------|------|---------|-------|
| **DES** | Symmetric block | 56-bit | Obsolete — too weak |
| **3DES** | Symmetric block | 112/168-bit | DES applied 3 times |
| **AES** | Symmetric block | 128/192/256-bit | Current standard |
| **RSA** | Asymmetric | 2048+ bit | Based on prime factoring |
| **ECC** | Asymmetric | 256-bit ≈ RSA 3072 | Efficient, used in mobile |
| **Diffie-Hellman** | Key exchange | Variable | Key exchange only, no encrypt |

### Hashing

Hashing produces a fixed-length output (digest) from variable-length input. One-way — cannot reverse.

| Algorithm | Output Size | Status |
|-----------|------------|--------|
| MD5 | 128-bit | Broken — collision attacks exist |
| SHA-1 | 160-bit | Deprecated |
| SHA-256 | 256-bit | Current standard |
| SHA-3 | Variable | Latest standard |

### Digital Signatures
1. Sender hashes the message
2. Sender encrypts hash with **private key** (this is the signature)
3. Receiver decrypts with sender's **public key**
4. Receiver hashes message independently
5. If hashes match → integrity + authentication + non-repudiation confirmed

### PKI — Public Key Infrastructure
- **CA (Certificate Authority):** Issues and signs digital certificates
- **RA (Registration Authority):** Verifies identity before CA issues cert
- **CRL (Certificate Revocation List):** List of revoked certificates
- **OCSP:** Online Certificate Status Protocol — real-time cert validation

---

## 3.4 Physical Security

### Site Selection Factors
- Crime rate and natural disaster risk in area
- Distance to emergency services (fire, police)
- Avoid ground floor or basement for data centres (flooding risk)
- Data centre ideally in core of building (not top floor, not basement)

### Fire Suppression

| Fire Class | Material | Suppression |
|-----------|---------|------------|
| A | Wood, paper | Water or soda acid |
| B | Liquids, petroleum | CO2, halon substitute |
| C | Electrical equipment | CO2, halon substitute (NOT water) |
| D | Combustible metals | Dry powder only |

> **Critical exam point:** Never use water on Class C (electrical) fires.

### Sprinkler Systems

| Type | Description | Best For |
|------|-------------|---------|
| **Wet pipe** | Always contains water | Standard environments |
| **Dry pipe** | Water held back by valve | Cold climates |
| **Pre-action** | Requires two triggers | Data centres (prevents accidental discharge) |
| **Deluge** | Open heads, large volume | High-hazard, not data centres |

---

## Domain 3 Summary — Must Know List

- [ ] Bell-LaPadula: confidentiality, no read up, no write down
- [ ] Biba: integrity, no read down, no write up
- [ ] Clark-Wilson: commercial integrity, separation of duties, audit
- [ ] Brewer-Nash: Chinese Wall, conflict of interest
- [ ] Protection rings 0–3 and what lives in each
- [ ] Symmetric vs asymmetric: speed, key count, use cases
- [ ] AES, RSA, SHA-256 as current standards
- [ ] Digital signature process (private key signs, public key verifies)
- [ ] Fire classes A/B/C/D and correct suppression for each
- [ ] Pre-action sprinklers for data centres
