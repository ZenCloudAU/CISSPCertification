# Domain 5: Identity & Access Management (IAM)

**Exam Weight:** 13%  
**Study Time:** ~10–14 hours  
**Mindset:** Every access decision follows Identify → Authenticate → Authorise → Audit.

---

## 5.1 The Four A's

| Step | Definition | Example |
|------|-----------|---------|
| **Identification** | Claiming an identity | Entering a username |
| **Authentication** | Proving that identity | Entering a password |
| **Authorisation** | Determining what you can do | Role-based access |
| **Accountability** | Recording what you did | Audit logs |

---

## 5.2 Authentication Factors

| Factor | Type | Examples | Risk |
|--------|------|---------|------|
| Something you **know** | Type 1 | Password, PIN, passphrase | Guessable, shareable |
| Something you **have** | Type 2 | Smart card, token, phone | Losable, stealable |
| Something you **are** | Type 3 | Biometrics | Irrevocable if compromised |

**Multi-Factor Authentication (MFA):** Uses 2+ different factor types. Two passwords = NOT MFA.

---

## 5.3 Biometrics

| Term | Definition |
|------|-----------|
| **FAR / Type II Error** | False Acceptance Rate — impostor accepted |
| **FRR / Type I Error** | False Rejection Rate — legitimate user rejected |
| **CER** | Crossover Error Rate — where FAR = FRR. Lower CER = more accurate. |

> **Exam tip:** Lowering FAR increases FRR and vice versa. CER is the single best measure of accuracy.

---

## 5.4 Access Control Models

| Model | How It Works | Who Controls Access | Used In |
|-------|-------------|---------------------|--------|
| **DAC** (Discretionary) | Owner sets permissions | Resource owner | Windows, Unix (most OSes) |
| **MAC** (Mandatory) | Labels-based, OS enforces | Operating system | Military, government |
| **RBAC** (Role-Based) | Permissions assigned to roles | Admin assigns roles | Enterprise environments |
| **ABAC** (Attribute-Based) | Dynamic, based on attributes | Policy engine | Cloud, modern systems |
| **Rule-Based** | Fixed rules (ACLs) | Admin writes rules | Firewalls, routers |

---

## 5.5 Kerberos Authentication Flow

1. Client requests a **Ticket Granting Ticket (TGT)** from the KDC (AS component)
2. KDC verifies and returns TGT encrypted with client's key
3. Client presents TGT to **Ticket Granting Service (TGS)**
4. TGS returns a **service ticket** for the requested resource
5. Client presents service ticket to the resource
6. Resource grants access

**Kerberos weaknesses:**
- KDC is a single point of failure
- Vulnerable to pass-the-ticket and pass-the-hash attacks
- Relies on time synchronisation (±5 minutes)
- Kerberoasting — attackers can request service tickets and crack offline

---

## 5.6 Single Sign-On (SSO)

| Benefit | Risk |
|---------|------|
| One credential set for all systems | Single point of compromise |
| Reduced password fatigue | If credential stolen, all systems exposed |
| Easier account management | |

**SSO Technologies:** Kerberos, SAML, OAuth 2.0, OpenID Connect, SESAME

---

## Domain 5 Summary — Must Know List

- [ ] Four A's: Identification, Authentication, Authorisation, Accountability
- [ ] Three authentication factors and examples of each
- [ ] FAR, FRR, CER — definitions and trade-offs
- [ ] DAC vs MAC vs RBAC — who controls, when used
- [ ] Kerberos flow: KDC → TGT → TGS → service ticket
- [ ] Kerberos weaknesses (single point of failure, time sync)
- [ ] MFA: must use DIFFERENT factor types
