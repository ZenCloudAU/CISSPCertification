# Domain 8: Software Development Security

**Exam Weight:** 10%  
**Study Time:** ~7–10 hours

---

## 8.1 Software Development Lifecycle (SDLC)

Security must be integrated at EVERY phase — not added at the end.

| Phase | Security Activity |
|-------|-----------------|
| **Requirements** | Security requirements defined, threat modelling begins |
| **Design** | Security architecture, access control design, data handling |
| **Development** | Secure coding standards, code review |
| **Testing** | Vulnerability scanning, pen testing, SAST/DAST |
| **Deployment** | Secure configuration, change management |
| **Maintenance** | Patch management, vulnerability monitoring |

---

## 8.2 SDLC Models

| Model | Description | Security Fit |
|-------|-------------|-------------|
| **Waterfall** | Sequential phases, no going back | Poor — security late |
| **Spiral** | Iterative with risk analysis at each cycle | Good — risk-driven |
| **Agile** | Short sprints, continuous delivery | Good if security is in sprint definition |
| **DevSecOps** | Security integrated into CI/CD pipeline | Best — shift-left security |

---

## 8.3 Common Vulnerabilities

| Vulnerability | Description | Prevention |
|---------------|-------------|-----------|
| **Buffer Overflow** | Writing past memory boundaries — execute arbitrary code | Input validation, safe functions, ASLR, DEP |
| **SQL Injection** | Malicious SQL in user input | Parameterised queries, input sanitisation |
| **XSS** | Injecting client-side scripts | Output encoding, CSP headers |
| **CSRF** | Tricking browser into making authenticated requests | CSRF tokens, SameSite cookies |
| **Race Condition (TOC/TOU)** | Timing gap between check and use | Atomic operations, locks |

---

## 8.4 Capability Maturity Model (CMM)

| Level | Name | Description |
|-------|------|-------------|
| 1 | **Initial** | Ad-hoc, chaotic — no defined processes |
| 2 | **Repeatable** | Basic project management established |
| 3 | **Defined** | Formal documented processes organisation-wide |
| 4 | **Managed** | Quantitative metrics collected and used |
| 5 | **Optimising** | Continuous improvement culture and budget |

---

## 8.5 Database Security

| Threat | Description | Countermeasure |
|--------|-------------|----------------|
| **Aggregation** | Combining low-sensitivity data to infer high-sensitivity data | Limit queries, context-aware access control |
| **Inference** | Deducing sensitive info from permitted queries | Cell suppression, partitioning |
| **Polyinstantiation** | Multiple versions of same record for different clearance levels | Used to prevent inference in MAC environments |

---

## Domain 8 Summary — Must Know List

- [ ] Security in SDLC: must be at every phase, not just testing
- [ ] Waterfall vs Spiral vs Agile security implications
- [ ] Buffer overflow: cause, exploit, and prevention
- [ ] SQL injection prevention: parameterised queries
- [ ] CMM 5 levels in order
- [ ] Aggregation vs inference (database threats)
