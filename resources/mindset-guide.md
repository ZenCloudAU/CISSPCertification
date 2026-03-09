# The CISSP Mindset Guide

## Think Like a Manager, Not a Technician

This is the single most important thing to internalise before sitting the CISSP exam.

The CISSP is not a technical certification in the traditional sense. It is a **managerial and governance** certification that validates your ability to think strategically about security across an entire organisation.

---

## The Manager Filter

Before selecting any answer, run it through this filter:

> "Is this what a **Chief Information Security Officer** or **Senior Manager** would do — not what a sysadmin would do?"

### Examples

| Scenario | Technician Thinks | Manager Thinks |
|----------|------------------|----------------|
| Employee shares their password | "Lock the account immediately" | "Update the acceptable use policy and run security awareness training" |
| New vulnerability found | "Patch it now" | "Assess risk, follow change management process, patch through approved channels" |
| Suspicious network traffic | "Block the IP" | "Investigate through proper incident response procedures, document findings" |
| Request to bypass security for a VIP | "OK, it's the CEO" | "No — policy applies to everyone; document the request and escalate if needed" |

---

## The Priority Hierarchy

When multiple answers seem correct, apply this hierarchy:

```
1. People safety always first
2. Senior management support / governance
3. Policy and procedures
4. Risk assessment / BIA
5. Training and awareness
6. Technical controls
7. Specific technical solutions
```

**Example:** "A new system is being deployed. What should happen FIRST?"
- Not: "Configure the firewall"
- Not: "Run a vulnerability scan"
- Yes: "Ensure management has approved and classified the system, defined security requirements, and that a risk assessment has been conducted"

---

## How to Read CISSP Questions

### Step 1: Identify what is really being asked
CISSP questions often include a lot of context. Strip it to the core question.

### Step 2: Identify the keywords
Watch for: **first, best, most, primary, immediate, CISO, senior manager, policy, risk**

### Step 3: Eliminate obviously wrong answers
Narrow to 2 answers. Then apply the manager filter.

### Step 4: Choose the answer with the highest strategic value
Governance > policy > training > technology

---

## Common Answer Patterns

### When the answer involves "first step"
Almost always one of:
- Obtain management support/approval
- Conduct a risk assessment
- Define scope
- Review/update policy

### When the question involves an incident
The correct sequence is almost always:
1. Contain the damage (don't destroy evidence)
2. Notify appropriate parties
3. Investigate
4. Eradicate
5. Recover
6. Document lessons learned

### When the question involves a new control
Ask: Has a risk assessment been done? Has management approved? Has the policy been updated? These come before implementation.

### When two answers both seem correct
Choose the one that:
- Is proactive rather than reactive
- Addresses the root cause rather than the symptom
- Involves policy/governance rather than technology
- Requires less assumption about context

---

## Phil's Contextual Advantage

Your background in presales, solutions architecture, and Technical Service Delivery Management gives you a genuine advantage here:

- **Presales:** You're used to translating technical concepts into business value — exactly what CISSP rewards
- **Solutions architecture:** You think in systems and trade-offs, not single components
- **Service delivery:** You understand SLAs, escalation paths, governance, and documentation

When you encounter a CISSP scenario, map it to a client engagement you've managed. Ask yourself: "What would I tell a CISO client in this situation?" That instinct is usually pointing to the right answer.

---

## The Avoid List

Things that are almost never the right CISSP answer:

- ❌ "Do it immediately without approval"
- ❌ "Implement the technical control first, then update policy"
- ❌ "The CISO should make all the decisions" (Senior Management is ultimately responsible)
- ❌ "Ignore the risk" (always wrong — accept, mitigate, transfer, or avoid)
- ❌ "The penetration tester doesn't need written consent" (always required)
- ❌ "Two passwords is MFA" (same factor type = NOT MFA)
