# Privilege Escalation Techniques

## Overview
After gaining initial access, privilege escalation techniques were used to obtain **root access** by exploiting **misconfigured permissions and SUID binaries**.

## Commands Used
```bash
# List all users and groups
cat /etc/passwd

# Check for misconfigured SUID binaries
find / -perm -u=s -type f 2>/dev/null

# Exploit misconfigured sudo privileges
sudo -l
sudo /usr/bin/vulnerable_binary
```
## Findings
1. The target system had world-writable scripts executed as root, allowing privilege escalation.
2. A misconfigured sudo entry permitted running commands as root without authentication.
3. An SUID binary was found that could be exploited for unauthorized root access.

## Mitigation Strategies
1. Restrict SUID binaries and remove unnecessary file privileges.
2. Regularly audit sudo permissions to prevent misconfigurations.
3. Implement logging and monitoring to detect unauthorized privilege escalation attempts.
4. Apply the principle of least privilege (PoLP) to all user accounts.