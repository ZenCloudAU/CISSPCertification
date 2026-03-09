# OSI & TCP/IP Reference

## OSI Model — Full Detail

| Layer | # | Name | Function | Protocols | Attack Examples |
|-------|---|------|----------|-----------|-----------------|
| 7 | App | Application | User interface to network services | HTTP, HTTPS, FTP, SMTP, DNS, SNMP, LDAP | Phishing, SQL injection, XSS |
| 6 | Pres | Presentation | Formatting, encryption, compression | TLS, SSL, JPEG, MPEG, ASCII | SSL stripping |
| 5 | Sess | Session | Establish, manage, terminate sessions | NetBIOS, RPC, SQL, NFS | Session hijacking |
| 4 | Trans | Transport | End-to-end delivery, port addressing | TCP, UDP, SSL | SYN flood, port scanning |
| 3 | Net | Network | Logical addressing, routing | IP, ICMP, OSPF, BGP, RIP | IP spoofing, ICMP attacks |
| 2 | DL | Data Link | Physical addressing, framing | Ethernet, ARP, PPP, FDDI | ARP poisoning, MAC flooding |
| 1 | Phys | Physical | Bits on wire, physical connectors | Coax, fibre, copper, 802.11 | Wiretapping, jamming |

---

## TCP Three-Way Handshake

```
Client                          Server
  |  ──── SYN ────────────────→  |   (I want to connect)
  |  ←─── SYN/ACK ─────────────  |   (OK, acknowledged)
  |  ──── ACK ────────────────→  |   (Great, connected)
  |                               |
  |    [Session established]      |
```

**SYN Flood Attack:** Attacker sends many SYN packets with spoofed source IPs. Server allocates resources waiting for ACK that never comes. Countermeasure: SYN cookies.

---

## Key Protocols by Layer

### Layer 7 — Application
| Protocol | Port | Purpose |
|----------|------|---------|
| HTTP | 80 | Web (unencrypted) |
| HTTPS | 443 | Web (encrypted) |
| FTP | 20/21 | File transfer |
| SSH | 22 | Secure remote access |
| Telnet | 23 | Remote access (unencrypted — avoid) |
| SMTP | 25 | Email sending |
| DNS | 53 | Name resolution |
| POP3 | 110 | Email retrieval |
| IMAP | 143 | Email (leaves on server) |
| SNMP | 161/162 | Network management |
| LDAP | 389 | Directory services |
| LDAPS | 636 | Encrypted directory |
| RDP | 3389 | Remote desktop |

### Layer 4 — Transport
| Protocol | Connection | Reliability | Use |
|----------|-----------|-------------|-----|
| TCP | Connection-oriented | Reliable, ordered, error-checked | Web, email, file transfer |
| UDP | Connectionless | No guarantee | Streaming, DNS, VoIP |

---

## Network Devices by Layer

| Device | Layer | Function |
|--------|-------|----------|
| Hub | 1 | Broadcasts to all ports — dumb |
| Repeater | 1 | Amplifies signal |
| Bridge | 2 | Forwards by MAC address |
| Switch | 2 | MAC-based forwarding, creates VLANs |
| Router | 3 | IP-based routing between networks |
| Multilayer Switch | 2+3 | Routing + switching in hardware |
| Gateway | 7 | Protocol translation, application proxy |
| Firewall | 3–7 | Access control (varies by type) |
