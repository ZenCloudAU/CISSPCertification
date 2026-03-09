# 8-Week CISSP Study Plan

**Daily commitment:** 1–2 hours  
**Total estimated hours:** 80–100 hours  
**Approach:** Domain-by-domain, mirroring the Infosec 6-day boot camp expanded to 8 weeks

---

## Weekly Overview

| Week | Domain Focus | Est. Hours | Key Milestone |
|------|-------------|------------|---------------|
| 1 | Domain 1 – Security & Risk Management | 10–14 hrs | Risk formulas mastered |
| 2 | Domain 2 – Asset Security | 7–10 hrs | Classification schemes known |
| 3 | Domain 3 – Security Architecture (Part 1) | 10–14 hrs | Security models understood |
| 4 | Domain 3 (cont.) + Domain 4 – Network Security | 10–14 hrs | OSI model & firewall types solid |
| 5 | Domain 5 – Identity & Access Management | 10–14 hrs | Kerberos & access models clear |
| 6 | Domain 6 – Security Assessment & Testing | 7–10 hrs | Pen test phases memorised |
| 7 | Domain 7 – Security Operations | 10–14 hrs | IR lifecycle understood |
| 8 | Domain 8 + Full Review + Mock Exams | 14–16 hrs | Practice exam score 75%+ |

---

## Week 1: Security & Risk Management (Domain 1 — 16%)

**Why it matters:** Highest weight domain. Sets the strategic mindset for the entire exam.

### Day-by-day

| Day | Activity |
|-----|----------|
| Mon | Read [`domains/01-security-risk-mgmt.md`](../domains/01-security-risk-mgmt.md) — CIA triad, governance, roles |
| Tue | Study risk management: SLE, ALE, ARO formulas. Drill until automatic. |
| Wed | Policy hierarchy: Policy → Standards → Baselines → Guidelines → Procedures |
| Thu | Risk responses (Reduce/Transfer/Accept/Avoid). Legal frameworks. Ethics. |
| Fri | Review [`artifacts/formula-cheatsheet.md`](../artifacts/formula-cheatsheet.md) |
| Sat | [`quiz/domain-1-quiz.md`](../quiz/domain-1-quiz.md) — all 15 questions |
| Sun | Review wrong answers. Rest. |

### Week 1 targets
- Able to calculate SLE, ALE from raw numbers in <30 seconds
- Know the 5 levels of the policy hierarchy and what makes each unique
- Understand the difference between Data Owner, Data Custodian, and Data User
- Know all 4 risk responses including when each is appropriate

---

## Week 2: Asset Security (Domain 2 — 10%)

**Why it matters:** Shorter domain but high-frequency in questions. Classification is tested constantly.

### Day-by-day

| Day | Activity |
|-----|----------|
| Mon | Read [`domains/02-asset-security.md`](../domains/02-asset-security.md) — classification schemes |
| Tue | Military vs commercial classification. Data lifecycle. Ownership. |
| Wed | Retention policies, data handling, privacy laws (GDPR, HIPAA, GLBA) |
| Thu | Data security controls: DRM, DLP, encryption at rest vs in transit |
| Fri | Review and cross-link to Domain 1 policies |
| Sat | [`quiz/domain-2-quiz.md`](../quiz/domain-2-quiz.md) |
| Sun | Review. Start previewing Domain 3 concepts. |

---

## Week 3: Security Architecture & Engineering — Part 1 (Domain 3 — 13%)

**Why it matters:** Most technically dense domain. Security models tested heavily.

### Day-by-day

| Day | Activity |
|-----|----------|
| Mon | Security models: Bell-LaPadula, Biba, Clark-Wilson, Brewer-Nash |
| Tue | TCB, reference monitor, security kernel, protection rings |
| Wed | Cryptography: symmetric vs asymmetric, DES/3DES/AES, RSA, hashing |
| Thu | PKI, digital signatures, certificates, SSL/TLS, IPSec |
| Fri | [`artifacts/model-comparison.md`](../artifacts/model-comparison.md) — comparison tables |
| Sat | [`quiz/domain-3-quiz.md`](../quiz/domain-3-quiz.md) — first 8 questions |
| Sun | Review. Focus on anything cryptography-related. |

---

## Week 4: Security Architecture Part 2 + Network Security (Domains 3 & 4)

**Why it matters:** Physical security + full network stack. OSI is tested in almost every exam.

### Day-by-day

| Day | Activity |
|-----|----------|
| Mon | Physical security: site design, locks, CCTV, fire suppression |
| Tue | [`artifacts/osi-tcp-reference.md`](../artifacts/osi-tcp-reference.md) — all 7 layers, protocols, ports |
| Wed | Firewalls: packet filter, stateful, proxy, application-layer, kernel proxy |
| Thu | VPN protocols: PPTP, L2TP, IPSec. Wireless: WEP, WPA, WPA2, 802.11x |
| Fri | Network attacks: DoS, DDoS, spoofing, ARP poisoning, man-in-the-middle |
| Sat | [`quiz/domain-4-quiz.md`](../quiz/domain-4-quiz.md) |
| Sun | Review. Memorise OSI layers and what lives at each. |

---

## Week 5: Identity & Access Management (Domain 5 — 13%)

**Why it matters:** Core operational topic. Access control models tested in complex scenarios.

### Day-by-day

| Day | Activity |
|-----|----------|
| Mon | Read [`domains/05-iam.md`](../domains/05-iam.md) — identification, authentication, authorisation |
| Tue | Authentication factors: something you know/have/are. Biometrics. CER. |
| Wed | Access control models: DAC, MAC, RBAC — when to use each |
| Thu | Kerberos: full authentication flow. SESAME. RADIUS vs TACACS+. |
| Fri | SSO benefits/risks. Federation. SAML. OAuth concepts. |
| Sat | [`quiz/domain-5-quiz.md`](../quiz/domain-5-quiz.md) |
| Sun | Review. Kerberos flow is a frequent exam topic — draw it out. |

---

## Week 6: Security Assessment & Testing (Domain 6 — 12%)

**Why it matters:** Procedural domain — know the correct sequence and terminology precisely.

### Day-by-day

| Day | Activity |
|-----|----------|
| Mon | Read [`domains/06-assessment-testing.md`](../domains/06-assessment-testing.md) |
| Tue | Vulnerability assessment vs penetration testing — key distinctions |
| Wed | Pen test phases: Discovery → Enumeration → Vulnerability Mapping → Exploitation → Report |
| Thu | Audit types: internal, external, third-party. Log review, SIEM. |
| Fri | Code review, fuzzing, static vs dynamic analysis |
| Sat | [`quiz/domain-6-quiz.md`](../quiz/domain-6-quiz.md) |
| Sun | Review. Note that authorisation/consent is always first step in pen testing. |

---

## Week 7: Security Operations (Domain 7 — 13%)

**Why it matters:** Incident response, forensics, and disaster recovery are high-frequency topics.

### Day-by-day

| Day | Activity |
|-----|----------|
| Mon | Read [`domains/07-security-operations.md`](../domains/07-security-operations.md) |
| Tue | Incident response lifecycle: Prepare → Identify → Contain → Eradicate → Recover → Lessons |
| Wed | Digital forensics: chain of custody, evidence types, order of volatility |
| Thu | BCP vs DRP. Hot/warm/cold sites. RTO vs RPO. Backup types. |
| Fri | Patch management, change management, configuration management |
| Sat | [`quiz/domain-7-quiz.md`](../quiz/domain-7-quiz.md) |
| Sun | Review. BCP/DRP terminology is a trap area — see exam-traps.md. |

---

## Week 8: Software Security + Full Review + Mock Exams (Domain 8 — 10%)

**Why it matters:** Final domain + consolidation week. Mock exam performance predicts readiness.

### Day-by-day

| Day | Activity |
|-----|----------|
| Mon | Read [`domains/08-software-security.md`](../domains/08-software-security.md) — SDLC, CMM |
| Tue | Secure coding practices. Buffer overflows. OWASP Top 10 awareness. |
| Wed | Database security: aggregation, inference, polyinstantiation |
| Thu | Full domain sweep: revisit weakest areas from quiz scores |
| Fri | [`resources/exam-traps.md`](../resources/exam-traps.md) — full read-through |
| Sat | **Full timed mock exam (150 questions, 3 hours)**. Target: 75%+ |
| Sun | Review every wrong answer. Book your exam. |

---

## Study Techniques That Work for CISSP

### Active Recall Over Passive Reading
After each section, close the material and write out everything you remember. This is 3x more effective than re-reading.

### The "Why is this wrong?" Method
For every practice question you miss, don't just learn the right answer — articulate why each wrong answer is wrong. CISSP questions often have two plausible answers.

### Scenario Mapping
Tie every concept to a real scenario from your own work. Your presales and delivery background gives you real client scenarios to anchor concepts.

### Spaced Repetition
Use Anki or similar flashcard tools for formulas, acronyms, and access control rules. Review cards daily — 15 minutes before bed works well.

### The Manager Filter
Before finalising any answer, ask: "Is this what a CISO/senior manager would do?" Technical fixes are almost never the best answer when a policy or governance option exists.

---

## Readiness Benchmarks

| Benchmark | Action |
|-----------|--------|
| Practice exam score consistently 65%+ | You are on track |
| Practice exam score consistently 75%+ | You are ready to book |
| Any domain below 60% in practice | Spend extra week on that domain |
| Scoring 80%+ in practice | Book your exam within 2 weeks |
