# Domain 2: Asset Security

**Exam Weight:** 10%  
**Study Time:** ~7–10 hours  
**Mindset:** Data has a lifecycle. Every decision about data should follow classification and ownership.

---

## 2.1 Information Classification

Classification tells everyone how to handle data — how to store it, transmit it, and destroy it.

### Why Classify?
- Protects data at the right level without over-spending
- Ensures consistent handling by all staff
- Required for regulatory compliance
- Drives access control decisions

### Classification Schemes

| Military | Private/Commercial | Description |
|----------|--------------------|-------------|
| Top Secret | Confidential | Highest — unauthorised disclosure causes grave damage |
| Secret | Private | Serious damage if disclosed |
| Confidential | Sensitive | Some damage if disclosed |
| Sensitive but Unclassified | Internal Use Only | Not public, but not highly sensitive |
| Unclassified | Public | Intended for public access |

> **Exam tip:** Military classification uses formal clearance levels. Commercial uses business impact. Know both schemes.

---

## 2.2 Data Roles

| Role | Responsibility |
|------|---------------|
| **Data Owner** | Assigns classification, responsible for use and protection decisions |
| **Data Custodian** | Implements controls, backups, access mechanisms |
| **Data Controller** (GDPR) | Decides how/why personal data is processed |
| **Data Processor** (GDPR) | Processes data on behalf of the controller |
| **Data Subject** | The individual the data is about |

---

## 2.3 Data Lifecycle

```
Create → Store → Use → Share → Archive → Destroy
```

Each phase has security implications:
- **Create:** Apply classification immediately
- **Store:** Encryption at rest, access controls
- **Use:** Least privilege, monitoring
- **Share:** DLP, DRM, encryption in transit
- **Archive:** Retention policies, integrity checks
- **Destroy:** Secure disposal (degaussing, shredding, crypto-erasure)

---

## 2.4 Data Security Controls

### Encryption
- **At rest:** Protects stored data (AES-256 standard)
- **In transit:** Protects data being transmitted (TLS 1.2+)
- **In use:** Emerging — homomorphic encryption

### Data Loss Prevention (DLP)
- Monitors and blocks unauthorised data transmission
- Can operate at endpoint, network, or cloud level
- Enforces classification-based policies automatically

### Digital Rights Management (DRM)
- Controls what recipients can do with data (open, print, copy, forward)
- Commonly used for documents and media
- Tied to identity — rights travel with the data

---

## 2.5 Retention & Destruction

### Retention Policies
- Data must be retained for the minimum period required by law or policy
- After that period, it must be **securely destroyed** — not just archived indefinitely
- Retaining data longer than necessary increases liability

### Secure Destruction Methods

| Method | Best For | Description |
|--------|---------|-------------|
| **Degaussing** | Magnetic media | Powerful magnetic field wipes data |
| **Overwriting** | HDDs | Write 0s or random data over all sectors |
| **Crypto-erasure** | Encrypted drives | Destroy the encryption key — data unrecoverable |
| **Physical destruction** | All media | Shredding, incineration, pulverising |
| **Purging** | Media for reuse | Complete removal before reassignment |

> **Exam tip:** Simply deleting a file does NOT destroy the data. It only removes the pointer. The data remains until overwritten.

---

## 2.6 Privacy Principles

Key privacy concepts that appear across domains:

- **Data minimisation:** Only collect what you need
- **Purpose limitation:** Use data only for the purpose it was collected
- **Storage limitation:** Don't keep it longer than necessary
- **Accuracy:** Keep it up to date
- **Accountability:** Be able to demonstrate compliance

These align with GDPR principles and are increasingly tested in CISSP.

---

## Domain 2 Summary — Must Know List

- [ ] Military vs commercial classification schemes (both sets of labels)
- [ ] Data Owner vs Data Custodian vs Data User (roles and responsibilities)
- [ ] Data lifecycle phases and the security concern at each phase
- [ ] Secure destruction: degaussing, overwriting, crypto-erasure, physical
- [ ] DLP vs DRM (different tools, different purposes)
- [ ] Why deleting ≠ destroying
- [ ] Retention policy purpose: legal minimum, not indefinite
