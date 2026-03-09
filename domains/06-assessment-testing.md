# Domain 6: Security Assessment & Testing

**Exam Weight:** 12%  
**Study Time:** ~7–10 hours

---

## 6.1 Vulnerability Assessment vs Penetration Testing

| | Vulnerability Assessment | Penetration Testing |
|-|------------------------|-------------------|
| Goal | Identify weaknesses | Exploit weaknesses |
| Depth | Broad scan | Deep targeted attack |
| Authorisation | Always required | Always required |
| Report | List of vulnerabilities | What was achieved + how |

---

## 6.2 Penetration Testing — 5 Phases

1. **Discovery (Footprinting):** OSINT, DNS lookup, network mapping
2. **Enumeration:** Port scans, service identification, OS fingerprinting
3. **Vulnerability Mapping:** Match findings to known CVEs
4. **Exploitation:** Attempt to gain unauthorised access
5. **Report to Management:** Documented findings + remediation recommendations

> **Always:** Written authorisation (Rules of Engagement) must be obtained BEFORE any testing begins.

---

## 6.3 Knowledge Levels

| Type | What the Tester Knows |
|------|----------------------|
| **Black Box (Zero Knowledge)** | Nothing about the target |
| **Grey Box (Partial Knowledge)** | Some info (e.g. network diagrams) |
| **White Box (Full Knowledge)** | Complete system knowledge |

---

## 6.4 Security Controls Testing

| Control Type | Examples |
|-------------|---------|
| **Administrative** | Policy review, training records, background checks |
| **Technical** | Vulnerability scans, code review, log analysis |
| **Physical** | Access log review, badge audits, CCTV review |

---

## 6.5 Log Review & SIEM

- **SIEM** (Security Information and Event Management): Collects, correlates, and alerts on logs
- **Audit logs** must be protected from modification (write-once media, digital signatures)
- **Clipping levels:** Threshold of normal violations before alerting — reduces noise

---

## Domain 6 Summary — Must Know List

- [ ] Vulnerability assessment vs pen test: identify vs exploit
- [ ] 5 pen test phases in order
- [ ] Written authorisation is ALWAYS required first
- [ ] Black/grey/white box definitions
- [ ] SIEM purpose: collection, correlation, alerting
