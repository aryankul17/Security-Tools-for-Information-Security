# Midterm CTF Challenge

## Overview
This Capture The Flag (CTF) challenge focused on applying **penetration testing techniques** to exploit vulnerabilities in a simulated environment. The objective was to perform **network reconnaissance, web exploitation, and privilege escalation** to capture hidden flags.

## Attack Steps
1. **Network Scanning:** Used Nmap to identify live hosts and open ports.
2. **Web Vulnerability Assessment:** Ran Nikto to detect misconfigurations and vulnerabilities.
3. **Exploitation:** Used SQL injection via SQLMap to extract database credentials.
4. **Brute-Force Attack:** Conducted credential brute-forcing using Hydra.
5. **Privilege Escalation:** Identified and exploited a misconfigured sudo privilege to gain root access.

## Tools Used
- **Nmap** – Network discovery and port scanning
- **Nikto** – Web vulnerability assessment
- **SQLMap** – SQL injection automation
- **Hydra** – Brute-force attack on login credentials
- **Metasploit** – Exploitation framework for privilege escalation
- **Wireshark** – Network traffic analysis

## Lessons Learned
- The importance of **reconnaissance and enumeration** in penetration testing.
- **Identifying weak configurations** in web applications and authentication mechanisms.
- The risks associated with **privilege escalation and misconfigured sudo permissions**.

For a detailed breakdown of findings and methodology, refer to the Midterm Report.
