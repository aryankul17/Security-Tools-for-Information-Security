# Network Scanning with Nmap

## Overview
Nmap was used for **network reconnaissance**, identifying **active hosts**, detecting **open ports**, and enumerating **running services**.

## Commands Used
```bash
# Scan for live hosts in the subnet
nmap -sn 192.168.1.0/24

# Perform a full port scan on a specific host
nmap -p- 192.168.1.100

# Detect service versions and OS information
nmap -sV -O 192.168.1.100

# Scan for known vulnerabilities using NSE scripts
nmap --script vuln 192.168.1.100

# Perform an aggressive scan with OS detection, version detection, and traceroute
nmap -A 192.168.1.100

```

## Findings 
1. Open ports detected: SSH (22), HTTP (80), MySQL (3306), and FTP (21) were accessible.
2. The web server was outdated, increasing the risk of exploitation.
3. The MySQL database was externally accessible, exposing it to potential brute-force attacks.
4. The FTP service allowed anonymous login, leading to potential unauthorized file access.

## Mitigation Strategies
1. Close unnecessary ports and apply strict firewall rules to restrict external access.
2. Disable anonymous login for services like FTP and enforce authentication policies.
3. Restrict database access to internal network traffic only.
4. Update and patch all running services to mitigate known vulnerabilities.
5. Monitor and log Nmap scans using Intrusion Detection Systems (IDS) to detect unauthorized reconnaissance attempts.