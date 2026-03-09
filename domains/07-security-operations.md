# Domain 7: Security Operations

**Exam Weight:** 13%  
**Study Time:** ~10–14 hours

---

## 7.1 Incident Response Lifecycle (NIST SP 800-61)

```
Preparation → Identification → Containment → Eradication → Recovery → Lessons Learned
```

| Phase | Key Activities |
|-------|---------------|
| **Preparation** | Policy, tools, team, training before incidents happen |
| **Identification** | Detect and confirm an incident is occurring |
| **Containment** | Limit the damage. Short-term then long-term containment. |
| **Eradication** | Remove the cause (malware, backdoor, vulnerability) |
| **Recovery** | Restore systems to normal operation. Monitor closely. |
| **Lessons Learned** | Document what happened. Improve for next time. |

---

## 7.2 Digital Forensics

### Chain of Custody
- Documents every person who handled evidence from collection to court
- Any gap in chain = evidence may be inadmissible

### Order of Volatility (collect most volatile first)
1. CPU registers and cache
2. RAM
3. Network connections and routing tables
4. Running processes
5. Hard disk
6. Logs on remote systems
7. Archival media

### Evidence Types

| Type | Description |
|------|-------------|
| **Best Evidence** | Original documents/records — most reliable |
| **Secondary Evidence** | Copies, verbal accounts — less reliable |
| **Direct Evidence** | Proves a fact by itself |
| **Circumstantial** | Suggests a fact but requires inference |
| **Hearsay** | Secondhand — generally not admissible (exceptions for business records) |

---

## 7.3 Disaster Recovery

### Recovery Site Types

| Type | Description | RTO | Cost |
|------|-------------|-----|------|
| **Hot Site** | Fully equipped, operational | Hours | Highest |
| **Warm Site** | Hardware present, needs config | Days | Medium |
| **Cold Site** | Empty building, power/connectivity only | Weeks | Lowest |

### Backup Types

| Type | What's Backed Up | Archive Bit Cleared? | Restore Complexity |
|------|-----------------|---------------------|-------------------|
| **Full** | Everything | Yes | Simple (one backup) |
| **Incremental** | Changed since last backup of any type | Yes | Complex (full + each incremental) |
| **Differential** | Changed since last full backup | No | Moderate (full + latest differential) |

---

## 7.4 Change Management

All changes to production systems must follow formal change management:

1. Request for Change (RFC) submitted
2. Change Advisory Board (CAB) reviews and approves
3. Change is tested in non-production environment
4. Change is implemented with rollback plan ready
5. Change is documented and reviewed

---

## Domain 7 Summary — Must Know List

- [ ] IR lifecycle: 6 phases in correct order
- [ ] Chain of custody: purpose and consequences of gaps
- [ ] Order of volatility: RAM before disk
- [ ] Hot/warm/cold site: RTO and cost trade-offs
- [ ] Backup types: full vs incremental vs differential restore complexity
- [ ] Change management: RFC → CAB → test → implement → document
