# Domain 1: Security & Risk Management

**Exam Weight:** 16% (highest of all domains)  
**Study Time:** ~10–14 hours  
**Mindset:** This domain is about governance, strategy, and management — not technology.

---

## 1.1 The CIA Triad

The foundation of all security decisions. Every exam question can be mapped back to at least one of these.

| Principle | Definition | Examples of Controls |
|-----------|------------|---------------------|
| **Confidentiality** | Prevent unauthorised disclosure of information | Encryption, access controls, classification, NDA |
| **Integrity** | Ensure information is accurate and unmodified | Hashing, digital signatures, audit trails, version control |
| **Availability** | Ensure information/systems are accessible when needed | Redundancy, backups, DDoS protection, failover |

> **Exam tip:** When a question asks about "preventing a hacker from reading data in transit," the answer relates to **confidentiality**. When it asks about "ensuring data wasn't changed," it's **integrity**.

---

## 1.2 Security Governance

Security governance defines how security decisions are made, who is responsible, and how accountability is enforced.

### Key Principle: Top-Down Approach
Security programs must be **initiated and supported by senior management**. A bottom-up approach (IT department driving security without executive support) is considered ineffective and a common exam trap.

### Security Roles

| Role | Responsibility |
|------|---------------|
| **Senior Management** | **Ultimately responsible** for all security outcomes. Signs off on policy. Accepts residual risk. |
| **Security Professional** | Functionally responsible. Designs and implements controls. |
| **Data Owner** | Usually senior management. Assigns classification. Determines handling requirements. |
| **Data Custodian** | Usually IT/Sysadmin. Implements controls. Maintains backups. Day-to-day care. |
| **Data User** | Uses data to perform job functions. Must follow policy. |
| **Auditor** | Independent verification that controls are effective. |

> **Critical distinction:** The Data Owner *decides* classification. The Data Custodian *implements* the controls the Owner requires.

---

## 1.3 Policy Hierarchy

From most strategic to most granular:

```
Policy (strategic intent — what and why)
    └── Standards (mandatory rules — how specifically)
            └── Baselines (minimum platform-specific config)
                    └── Guidelines (recommended, not mandatory)
                            └── Procedures (step-by-step instructions)
```

| Level | Mandatory? | Written by | Example |
|-------|-----------|------------|---------|
| Policy | Yes | Senior management | "We will protect all customer data" |
| Standard | Yes | Security/IT leadership | "All passwords: 12+ chars, complexity required" |
| Baseline | Yes | IT/Security team | "All Windows servers: CIS Benchmark Level 1" |
| Guideline | No | IT/Security team | "Users should lock screens when leaving desk" |
| Procedure | Yes | IT operations | Step-by-step guide to reset a password securely |

### Policy Types
- **Organisational/Program policy:** Broad, covers whole organisation
- **Issue-specific policy:** Addresses one topic (e.g. Acceptable Use Policy, Email Policy)
- **System-specific policy:** Governs a specific system or asset (e.g. database access policy)

---

## 1.4 Risk Management

Risk management is the process of identifying, assessing, and reducing risk to an acceptable level.

### Core Definitions

| Term | Definition |
|------|-----------|
| **Asset** | Anything of value to the organisation |
| **Threat** | Any potential danger to an asset |
| **Threat Agent** | The entity that carries out the threat (hacker, employee, flood) |
| **Vulnerability** | A weakness that a threat agent can exploit |
| **Exposure** | The instance of being susceptible to loss |
| **Risk** | The probability that a threat agent exploits a vulnerability |
| **Countermeasure/Safeguard** | A control that reduces risk |
| **Residual Risk** | Risk remaining after controls are applied |

### Risk Formulas — Memorise These

```
SLE = Asset Value × Exposure Factor (EF)

ALE = SLE × ARO

Residual Risk = Total Risk × Controls Gap

Value of Safeguard = (ALE before) − (ALE after) − (Annual cost of safeguard)
```

| Formula | Full Name | Meaning |
|---------|-----------|---------|
| **SLE** | Single Loss Expectancy | Cost if the threat occurs ONCE |
| **EF** | Exposure Factor | % of asset value lost per incident (0.0–1.0) |
| **ARO** | Annualised Rate of Occurrence | How many times per year the threat is expected |
| **ALE** | Annualised Loss Expectancy | Expected annual cost of the threat |

**Example:**
- Server value: $100,000
- Fire destroys 40% of it → EF = 0.40
- SLE = $100,000 × 0.40 = **$40,000**
- Fire expected once every 10 years → ARO = 0.1
- ALE = $40,000 × 0.1 = **$4,000/year**
- If a sprinkler costs $2,000/year → Worth it (saves $4,000)

### Risk Responses

| Response | Description | When to Use |
|----------|-------------|-------------|
| **Reduce (Mitigate)** | Implement controls to lower probability or impact | When cost-effective safeguards exist |
| **Transfer (Assign)** | Move risk to another party (insurance, outsourcing) | When risk is too costly to mitigate internally |
| **Accept** | Consciously choose to live with the risk | When cost of mitigation > cost of the risk |
| **Avoid** | Stop the activity that creates the risk | When no other option is acceptable |
| ~~Reject/Ignore~~ | Pretend the risk doesn't exist | **NEVER — this is negligent** |

### Quantitative vs Qualitative Risk Analysis

| | Quantitative | Qualitative |
|-|-------------|------------|
| **Output** | Dollar amounts, percentages | High/Medium/Low ratings |
| **Precision** | High (but complex) | Lower (but faster) |
| **Tools** | SLE, ALE, ARO calculations | Delphi, brainstorming, surveys |
| **Best for** | When exact financial impact needed | When data is limited or time is short |

> **Exam tip:** Purely quantitative risk analysis is technically impossible because you must always estimate some values — making it partially qualitative.

---

## 1.5 Due Diligence vs Due Care

| Concept | Definition | Example |
|---------|-----------|---------|
| **Due Diligence** | Investigating and understanding risks before acting | Conducting a risk assessment before deploying a new system |
| **Due Care** | Taking responsible action based on what you know | Implementing a firewall after the risk assessment identifies network threats |

> Analogy: Due diligence is researching a car before buying. Due care is wearing a seatbelt when you drive it.

---

## 1.6 Legal & Regulatory Frameworks

### Types of Law

| Type | Description | Outcome |
|------|-------------|---------|
| **Criminal Law** | Violations of government law. Protects public. | Jail, fines |
| **Civil Law (Tort)** | Wrongs against individuals/companies. | Financial damages |
| **Administrative/Regulatory** | Standards set by government agencies. | Fines, sanctions |

### Key Privacy Laws

| Law | Jurisdiction | What It Covers |
|-----|-------------|----------------|
| **HIPAA** | USA | Healthcare data protection |
| **GLBA** | USA | Financial institutions, customer data |
| **GDPR** | EU/EEA | All personal data of EU residents |
| **Federal Privacy Act 1974** | USA | Federal agency data handling |
| **Computer Fraud and Abuse Act** | USA | Primary anti-hacking statute |

### Negligence Elements (must prove all three)
1. A legally recognised obligation existed
2. Failure to conform to that standard
3. Proximate causation — the failure caused the damage

---

## 1.7 Business Continuity Planning (BCP)

BCP ensures the organisation can continue critical operations during and after a disruption.

### BCP Steps
1. Project initiation (scope, management support, resources)
2. **Business Impact Analysis (BIA)** — most critical step
3. Recovery strategy development
4. Plan development
5. Implementation
6. Testing and maintenance

### BCP vs DRP
| | BCP | DRP |
|-|-----|-----|
| Focus | Keeping business running | Restoring IT systems |
| Scope | Organisation-wide | IT/technical |
| Timeframe | Ongoing | After a disaster |

### BIA Key Terms
| Term | Definition |
|------|-----------|
| **RTO** | Recovery Time Objective — maximum acceptable downtime |
| **RPO** | Recovery Point Objective — maximum acceptable data loss (time-based) |
| **MTD** | Maximum Tolerable Downtime — absolute limit before business fails |

---

## 1.8 Ethics

### ISC2 Code of Ethics (memorise the order)
1. Protect society, the common good, necessary public trust and confidence, and the infrastructure
2. Act honourably, honestly, justly, responsibly, and legally
3. Provide diligent and competent service to principals
4. Advance and protect the profession

> **Exam tip:** These are in priority order. If there's a conflict, #1 takes precedence over #4.

---

## Domain 1 Summary — Must Know List

- [ ] CIA triad definitions and examples for each
- [ ] All risk formulas: SLE, ALE, ARO, residual risk
- [ ] Risk responses: Reduce, Transfer, Accept, Avoid (never Reject/Ignore)
- [ ] Policy hierarchy: Policy → Standards → Baselines → Guidelines → Procedures
- [ ] Security roles: Owner vs Custodian vs User vs Senior Management
- [ ] Due Diligence vs Due Care
- [ ] Top-down vs bottom-up approach (top-down is correct)
- [ ] BCP vs DRP, RTO vs RPO
- [ ] ISC2 Code of Ethics (4 canons in order)
- [ ] Types of law: Criminal vs Civil vs Administrative
