# CISSP Exam Traps & How to Avoid Them

> These are the most common reasons candidates fail. Review this page every week and again the night before your exam.

---

## Trap 1: Thinking Like a Technician

**The mistake:** Choosing the technical fix when a managerial/governance answer exists.

**Example question:** "A security audit reveals employees are sharing passwords. What should you do FIRST?"

- ❌ Wrong: "Implement MFA immediately"
- ✅ Right: "Update the security policy and provide awareness training"

**The rule:** CISSP prioritises policy → training → technology. If an answer involves updating a policy or training staff, it usually beats installing a control.

---

## Trap 2: "First" and "Most Important" Questions

**The mistake:** Jumping to action instead of following proper sequence.

**Example:** "What is the FIRST step in establishing a security program?"
- ❌ Wrong: Conduct a risk assessment
- ✅ Right: Obtain senior management support

**The rule:** The correct first step is almost always one of:
1. Get management buy-in
2. Define scope
3. Identify assets
...NOT implement controls.

---

## Trap 3: Risk Acceptance vs Risk Rejection

**The mistake:** Confusing conscious risk acceptance with ignoring a risk.

- **Risk Acceptance:** Documented management decision to live with a risk (acceptable)
- **Risk Rejection/Ignoring:** Pretending a risk doesn't exist (never acceptable, negligent)

**Exam tip:** If a question describes a manager who acknowledges the risk and formally accepts it → Risk Acceptance. If they simply ignore it → Risk Rejection (wrong choice).

---

## Trap 4: BCP vs DRP

**The mistake:** Using BCP and DRP interchangeably.

| | BCP | DRP |
|-|-----|-----|
| Focus | Business continuity | IT/systems recovery |
| Scope | Whole organisation | Technology systems |
| Activation | Before and during disruption | After a disaster |

**Exam tip:** DRP is a subset of BCP. BCP is the umbrella.

---

## Trap 5: Data Owner vs Data Custodian

**The mistake:** Thinking the IT admin is responsible for classification decisions.

- **Data Owner** = Senior manager = DECIDES classification and protection requirements
- **Data Custodian** = IT/Sysadmin = IMPLEMENTS what the owner requires

**Exam tip:** Any question about "who is responsible for X?" — if X is a strategic decision, it's the Owner. If X is an operational task, it's the Custodian.

---

## Trap 6: The Safeguard Cost Formula Direction

**The mistake:** Implementing a safeguard because it reduces risk — without checking if it's cost-effective.

```
Value of Safeguard = (ALE before) − (ALE after) − (Annual cost of safeguard)
```

If this is **negative → do NOT implement**. The safeguard costs more than the risk.

---

## Trap 7: Bell-LaPadula vs Biba Direction Confusion

**Bell-LaPadula (confidentiality):**
- No read UP (can't read higher)
- No write DOWN (can't write to lower)

**Biba (integrity):**
- No read DOWN (can't read lower)
- No write UP (can't write to higher)

**Memory trick:** BLP protects secrets from leaking DOWN. Biba protects quality from being contaminated from BELOW.

---

## Trap 8: Fire Suppression for Electrical Fires

**The mistake:** Choosing water for a Class C (electrical) fire.

**NEVER use water on electrical equipment.** Water conducts electricity and will cause electrocution and more damage.

Class C fires: CO2 or halon substitute only.

---

## Trap 9: Incremental vs Differential Restore Time

**The mistake:** Thinking differential backups are slower to restore than incremental.

| Type | Backup Time | Restore Time |
|------|------------|-------------|
| Full | Slowest | Fastest (one set) |
| Differential | Medium | Medium (full + 1 differential) |
| Incremental | Fastest | Slowest (full + every incremental since) |

**Exam tip:** "Incremental is faster to back up but slower to restore." Differential is the opposite.

---

## Trap 10: Penetration Testing Requires Authorisation FIRST

**The mistake:** Jumping to the technical activity.

**The rule:** Written authorisation (Rules of Engagement) must ALWAYS be obtained before any penetration testing begins. No exceptions. This is the answer to "What should be done FIRST before a pen test?"

---

## Trap 11: MFA Requires DIFFERENT Factor Types

**The mistake:** Thinking a password + a PIN = MFA.

Both a password and a PIN are "something you know" (Type 1). Using two of the same factor type is NOT multi-factor authentication.

**True MFA examples:**
- Password (Type 1) + Smart card (Type 2) ✅
- PIN (Type 1) + Fingerprint (Type 3) ✅
- Password + Security question ❌ (both Type 1)

---

## Trap 12: CAT Exam Behaviour

**The mistake:** Panicking when the exam ends early or assuming harder questions mean you're failing.

- Exam ending at 100 questions does NOT mean you failed (it may mean you passed decisively)
- Harder questions = the system thinks you might pass (good sign)
- You CANNOT go back to change answers
- Read every question carefully — CISSP wording is precise and deliberate

---

## Trap 13: "Best" vs "First" vs "Most Important"

CISSP questions frequently ask for the "best," "first," or "most important" action. These are different:

- **First:** What's the initial step in a process?
- **Best:** What produces the most effective outcome?
- **Most important:** What has the highest strategic value?

When you see these words, slow down and re-read the full question before answering.

---

## Trap 14: Endorsement After Passing

**The mistake:** Thinking passing the exam = being CISSP certified.

Passing the exam makes you an **Associate of ISC2**. You must:
1. Have (or obtain within 6 years) 5 years of qualifying experience
2. Be endorsed by an existing ISC2 member
3. Pass ISC2's background check

Only then are you a CISSP.

---

## Trap 15: Deleting ≠ Destroying Data

**The mistake:** Thinking deleting a file or formatting a drive destroys the data.

Deleting a file removes the pointer, not the data. The data remains on disk until overwritten.

Secure destruction requires: degaussing, overwriting (multiple passes), crypto-erasure, or physical destruction.
