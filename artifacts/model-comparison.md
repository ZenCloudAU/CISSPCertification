# Security Model Comparison

## Side-by-Side Model Reference

| Model | Primary Goal | Environment | Key Rules | Limitation |
|-------|-------------|-------------|-----------|-----------|
| **Bell-LaPadula** | Confidentiality | Military/Government | No read up, no write down | Ignores integrity |
| **Biba** | Integrity | Commercial/Financial | No read down, no write up | Ignores confidentiality |
| **Clark-Wilson** | Commercial Integrity | Business | Well-formed transactions, separation of duties | Complex to implement |
| **Brewer-Nash** | Conflict of Interest | Finance/Legal | Dynamic access based on history | Hard to manage at scale |
| **Graham-Denning** | Access control rights | General | Rules for creating/deleting subjects/objects | Theoretical |
| **Harrison-Ruzzo-Ullman** | Access control changes | General | Defines how access rights change | Theoretical |

---

## Bell-LaPadula In Detail

Developed for DoD to protect classified information. Based on mandatory access control.

```
Levels (highest to lowest):
Top Secret → Secret → Confidential → Unclassified

Rules:
  Simple Security Rule: Subject CANNOT read object at HIGHER level
  *-property (Star) Rule: Subject CANNOT write to object at LOWER level
  Strong Star Property: Subject can ONLY read/write at SAME level
```

**Visualisation:**
```
Top Secret  ←  Can't read here (read up blocked)
Secret      ←  Subject is HERE
Confidential ←  Can't write here (write down blocked)
```

---

## Biba In Detail

Developed as the integrity counterpart to Bell-LaPadula.

```
Integrity Levels (highest to lowest):
High Integrity → Medium Integrity → Low Integrity

Rules:
  Simple Integrity Axiom:  Subject CANNOT read object at LOWER integrity level
  *-Integrity Axiom:       Subject CANNOT write to object at HIGHER integrity level
```

**Why no read down?** Reading low-integrity data could corrupt a high-integrity subject's decisions.

---

## Clark-Wilson In Detail

Designed for commercial environments where data integrity during transactions is critical.

### Key Concepts

| Term | Meaning |
|------|---------|
| **CDI** | Constrained Data Item — data that must maintain integrity |
| **UDI** | Unconstrained Data Item — input from untrusted sources |
| **IVP** | Integrity Verification Procedure — verifies CDI is in valid state |
| **TP** | Transformation Procedure — the only authorised way to modify CDI |

### Access Triple
```
Subject → Transformation Procedure → CDI Object
```
Users can ONLY interact with data through approved programs. No direct data manipulation.

---

## Memory Tricks

- **Bell-LaPadula:** "Bell rings at the TOP — confidentiality protects the TOP from leaking down"
- **Biba:** "Biba hates DIRT — no dirty (low integrity) data gets in, no modifications go up"
- **Clark-Wilson:** "Clark works in a BANK — every transaction is audited and controlled"
- **Brewer-Nash:** "The WALL between competing clients — like Chinese food, no mixing"
