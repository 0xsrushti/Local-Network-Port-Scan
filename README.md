# Local-Network-Port-Scan
Nmap local network scan and findings

**Objective:**
Discover open ports on devices in the local network to understand network exposure.

**Tools Used:**
- Nmap (TCP SYN scan)
- Wireshark (optional)

**IP Range Scanned:** 10.0.2.0/24

**Steps Performed:**
1. Identified local IP: 10.0.2.15
2. Performed TCP SYN scan: `nmap -sS 10.0.2.0/24 -oN scan_results.txt`
3. Recorded open ports and services
4. Optional Wireshark analysis captured TCP SYN packets
5. Summarized risks and mitigation recommendations

**Key Findings:**
- Hosts 10.0.2.2, 10.0.2.3, 10.0.2.4 have open ports: 135, 445, 5357
- Host 10.0.2.15 has no open ports

**Recommendations:**
- Restrict SMB and RPC services to local subnet
- Apply firewall rules
- Patch systems and disable unused services

**Interview Questions:**
See notes.md for answers
