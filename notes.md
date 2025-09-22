# Local Network Port Scan Findings

**IP Range Scanned:** 10.0.2.0/24
**Scanner:** Nmap TCP SYN Scan
**Scan Date:** 2025-09-22

---

## Host Findings

### Host: 10.0.2.2
- **Open Ports:** 135/tcp (msrpc), 445/tcp (microsoft-ds), 5357/tcp (wsdapi)
- **Risk Assessment:** Medium – SMB exposed; RPC service can be targeted
- **Mitigation:** Restrict SMB to local subnet, patch OS, use firewall

### Host: 10.0.2.3
- **Open Ports:** 135/tcp, 445/tcp, 5357/tcp
- **Risk Assessment:** Medium
- **Mitigation:** Same as above

### Host: 10.0.2.4
- **Open Ports:** 135/tcp, 445/tcp, 5357/tcp
- **Risk Assessment:** Medium
- **Mitigation:** Same as above

### Host: 10.0.2.15
- **Open Ports:** None
- **Risk Assessment:** Low – no open ports
- **Mitigation:** None required

---

## Summary
- Total hosts scanned: 256
- Total hosts up: 4
- Total open ports found: 12
- Most critical risk: Open SMB ports (445/tcp)
- Recommendation: Apply firewall rules, disable unused services, patch all systems

---

## Interview Questions (Short Answers)
1. **What is an open port?** A network port actively listening for connections.
2. **How does Nmap perform TCP SYN scan?** Sends SYN, expects SYN-ACK for open ports, sends RST to avoid handshake.
3. **Risks of open ports?** Exploitation, unauthorized access, data leaks.
4. **TCP vs UDP scanning?** TCP uses handshake; UDP is connectionless, slower.
5. **How to secure open ports?** Disable unused services, apply firewall rules, patch systems.
6. **Firewall's role?** Filters traffic, blocks/permits ports.
7. **What is a port scan and why attackers do it?** Recon to find exploitable services.
8. **How does Wireshark complement scanning?** Packet-level verification and analysis.
