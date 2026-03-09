# Domain 1 Quiz: Security & Risk Management

**15 questions** | Cover all material in `domains/01-security-risk-mgmt.md` before attempting  
**Target score:** 12/15 (80%) before moving on

---

> Try each question before reading the answer. For any you get wrong, re-read the relevant section.

---

**Q1.** A server is valued at $300,000. A flood is estimated to destroy 30% of its value. Floods are expected once every 5 years. What is the ALE?

<details>
<summary>Show Answer</summary>

**$18,000**

- EF = 0.30
- SLE = $300,000 × 0.30 = $90,000
- ARO = 1/5 = 0.2
- ALE = $90,000 × 0.2 = **$18,000**

</details>

---

**Q2.** Who has the FINAL responsibility for protecting an organisation's assets?

A) The CISO  
B) The Data Custodian  
C) Senior Management  
D) The Security Administrator

<details>
<summary>Show Answer</summary>

**C) Senior Management**

Senior management is ultimately responsible for all security outcomes, including assigning appropriate resources and accepting residual risk. The CISO and Security Administrator are functionally responsible.

</details>

---

**Q3.** A countermeasure costs $50,000/year to operate. Without it, ALE is $40,000. Should it be implemented?

<details>
<summary>Show Answer</summary>

**No.**

The value of the safeguard = ALE before ($40,000) − ALE after ($0) − Annual cost ($50,000) = **−$10,000**

A negative value means the safeguard costs more than the risk it prevents. It should NOT be implemented.

</details>

---

**Q4.** Which of the following is an example of a GUIDELINE?

A) "All passwords must be at least 12 characters"  
B) "Users should lock their screen when leaving their desk"  
C) "Servers must be patched within 30 days of a critical release"  
D) "The organisation will protect all customer data"

<details>
<summary>Show Answer</summary>

**B) "Users should lock their screen when leaving their desk"**

The word "should" (not "must") indicates this is a guideline — recommended but not mandatory. A = Standard. C = Standard. D = Policy.

</details>

---

**Q5.** What is the correct order of the policy hierarchy from most strategic to most granular?

<details>
<summary>Show Answer</summary>

**Policy → Standards → Baselines → Guidelines → Procedures**

</details>

---

**Q6.** A Data Owner has left the company. Who is MOST likely to take over their responsibilities?

A) The Data User  
B) Senior Management  
C) The Data Custodian  
D) The Security Administrator

<details>
<summary>Show Answer</summary>

**B) Senior Management**

Data Owners are typically senior managers. When one leaves, their responsibilities fall to another senior manager, not to the custodian or administrator.

</details>

---

**Q7.** What is the difference between Due Diligence and Due Care?

<details>
<summary>Show Answer</summary>

- **Due Diligence:** The act of investigating and understanding risks before taking action. Research phase.
- **Due Care:** Taking responsible action based on what you've learned. Implementation phase.

Example: Conducting a risk assessment (due diligence) → installing a firewall (due care).

</details>

---

**Q8.** A company discovers a risk but decides the cost of mitigation is greater than the potential loss. What risk response is this?

A) Risk Transfer  
B) Risk Avoidance  
C) Risk Reduction  
D) Risk Acceptance

<details>
<summary>Show Answer</summary>

**D) Risk Acceptance**

The company consciously acknowledges the risk and decides to live with it because the cost-benefit doesn't justify controls. This must be documented and approved by management.

</details>

---

**Q9.** Which type of risk analysis assigns dollar amounts to assets and threats?

A) Qualitative  
B) Quantitative  
C) Hybrid  
D) Delphi

<details>
<summary>Show Answer</summary>

**B) Quantitative**

Quantitative analysis uses actual numbers (ALE, SLE, ARO) to express risk in dollar terms. Qualitative uses ratings like High/Medium/Low.

</details>

---

**Q10.** In the ISC2 Code of Ethics, which canon takes the HIGHEST priority?

A) Advance and protect the profession  
B) Provide diligent and competent service  
C) Protect society and the common good  
D) Act honourably and legally

<details>
<summary>Show Answer</summary>

**C) Protect society and the common good**

The four canons are listed in priority order. Canon 1 (protect society) always takes precedence over Canons 2, 3, and 4.

</details>

---

**Q11.** A manager ignores a known vulnerability because they "don't think it's a real risk." What is this called?

A) Risk Transfer  
B) Risk Rejection  
C) Risk Acceptance  
D) Risk Avoidance

<details>
<summary>Show Answer</summary>

**B) Risk Rejection**

Risk Rejection (also called ignoring the risk) is different from Risk Acceptance. Acceptance requires a conscious, documented management decision. Simply ignoring a risk is negligent and is NEVER acceptable in CISSP.

</details>

---

**Q12.** Which of the following best describes the PRIMARY goal of a Business Continuity Plan (BCP)?

A) Restore IT systems after a disaster  
B) Ensure critical business functions continue during a disruption  
C) Identify all possible threats to the organisation  
D) Provide insurance against financial losses

<details>
<summary>Show Answer</summary>

**B) Ensure critical business functions continue during a disruption**

BCP is broader than DRP (which focuses on IT restoration). BCP keeps the business running. DRP is a component of BCP.

</details>

---

**Q13.** What is the MOST important first step when establishing a security program?

A) Installing firewalls and IDS  
B) Hiring a CISO  
C) Obtaining senior management support  
D) Conducting a risk assessment

<details>
<summary>Show Answer</summary>

**C) Obtaining senior management support**

Without executive support, a security program will fail regardless of technical controls. This is the foundation. The top-down approach starts here.

</details>

---

**Q14.** A law that covers healthcare data privacy in the United States is:

A) GDPR  
B) GLBA  
C) HIPAA  
D) SOX

<details>
<summary>Show Answer</summary>

**C) HIPAA**

- HIPAA = Healthcare data (USA)
- GLBA = Financial institutions (USA)
- GDPR = All personal data (EU)
- SOX = Financial reporting (USA publicly traded companies)

</details>

---

**Q15.** An employee transfers to a new department but retains all permissions from their previous role in addition to gaining new ones. This is an example of:

A) Separation of duties  
B) Least privilege violation / Authorisation creep  
C) Need-to-know principle applied correctly  
D) Role-based access control

<details>
<summary>Show Answer</summary>

**B) Least privilege violation / Authorisation creep**

This is called "authorisation creep" — permissions accumulate over time as roles change but old access is never removed. It violates the principle of least privilege.

</details>

---

## Scoring

| Score | Status |
|-------|--------|
| 13–15 | Ready to move to Domain 2 ✅ |
| 10–12 | Review weak areas, re-attempt tomorrow |
| Below 10 | Re-read Domain 1 before continuing |
