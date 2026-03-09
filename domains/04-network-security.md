# Domain 4: Communication & Network Security

**Exam Weight:** 13%  
**Study Time:** ~10–14 hours  
**Mindset:** Understand each layer of the OSI model and what can go wrong at each one.

---

## 4.1 OSI Model

| Layer | # | Protocol/Technology | What It Does |
|-------|---|-------------------|-------------|
| Application | 7 | HTTP, FTP, SMTP, DNS | User-facing services |
| Presentation | 6 | TLS, SSL, JPEG, MPEG | Formatting, encryption |
| Session | 5 | NetBIOS, RPC, SQL | Establish/manage sessions |
| Transport | 4 | TCP, UDP | End-to-end delivery, ports |
| Network | 3 | IP, ICMP, RIP, OSPF | Routing, IP addressing |
| Data Link | 2 | Ethernet, ARP, PPP | MAC addressing, framing |
| Physical | 1 | Coax, fibre, copper | Bits on wire |

> **Memory:** "All People Seem To Need Data Processing" (Application → Physical)

---

## 4.2 Firewall Types

| Type | Layer | How It Works | Pros | Cons |
|------|-------|-------------|------|------|
| **Packet Filtering** | 3 | Checks source/dest IP and port | Fast, simple | No context, no payload inspection |
| **Stateful Inspection** | 3–4 | Tracks connection state | Better security than packet filtering | Can be overwhelmed by state table attack |
| **Application Proxy** | 7 | Full proxy, inspects payload | Highest security | Slow, one proxy per service |
| **Circuit-Level Proxy** | 5 | Validates handshake only | Flexible, no per-service proxy | Less granular than app proxy |
| **Dynamic Packet Filtering** | 3 | Opens/closes ports dynamically | Allows return traffic | 4th generation complexity |
| **Kernel Proxy** | All | Inspects at kernel level per packet | Fast and thorough | 5th generation, complex |

---

## 4.3 VPN Protocols

| Protocol | Layer | Notes |
|----------|-------|-------|
| **PPTP** | Layer 2 | Microsoft. IP networks only. Weak security. |
| **L2TP** | Layer 2 | Cisco + Microsoft. No native encryption — must pair with IPSec. |
| **IPSec** | Layer 3 | Strong encryption and auth. LAN-to-LAN focus. |
| **SSL/TLS VPN** | Layer 7 | Browser-based. Easy client deployment. |

### IPSec Modes
- **Transport mode:** Payload encrypted only. Headers visible.
- **Tunnel mode:** Entire packet (payload + headers) encrypted. Used for site-to-site VPN.

---

## 4.4 Common Attacks & Countermeasures

| Attack | Description | Countermeasure |
|--------|-------------|----------------|
| **DoS** | Overwhelm a system to deny service | Rate limiting, IDS, patching |
| **DDoS** | Multiple sources attacking simultaneously | Upstream filtering, CDN, IDS |
| **SYN Flood** | Sends SYN but never ACK — fills connection table | SYN cookies, reduce timeout, IDS |
| **Smurf** | Spoofed ICMP broadcast amplification | Disable directed broadcasts, ingress filtering |
| **ARP Poisoning** | Falsify ARP table to intercept traffic | Dynamic ARP Inspection (DAI), static ARP |
| **IP Spoofing** | Forge source IP address | Ingress/egress filtering, IPSec |
| **Man-in-the-Middle** | Intercept communications | Encryption, mutual authentication, PKI |
| **Replay Attack** | Capture and resend authentication data | Timestamps, nonces, session tokens |

---

## 4.5 Wireless Security

| Standard | Security | Notes |
|----------|---------|-------|
| **WEP** | Broken | RC4 with weak IV. Do not use. |
| **WPA** | Weak | TKIP — improved but still vulnerable |
| **WPA2** | Good | AES-CCMP. Current minimum standard. |
| **WPA3** | Best | SAE. Resistant to offline dictionary attacks. |

---

## Domain 4 Summary — Must Know List

- [ ] OSI 7 layers — name, number, and what lives at each
- [ ] TCP 3-way handshake: SYN → SYN/ACK → ACK
- [ ] Common ports: 21 FTP, 22 SSH, 23 Telnet, 25 SMTP, 53 DNS, 80 HTTP, 443 HTTPS
- [ ] Firewall types in order of increasing security capability
- [ ] IPSec: Transport mode vs Tunnel mode
- [ ] SYN flood: mechanism and countermeasure
- [ ] WPA2 minimum standard; WEP is broken
