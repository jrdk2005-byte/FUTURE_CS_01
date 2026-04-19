# FUTURE_CS_01 - Vulnerability Assessment Report

## Objective
Perform vulnerability assessment on a live website using Nmap and OWASP ZAP.

## Target
http://demo.testfire.net

## Tools Used
- Nmap
- OWASP ZAP
- Browser Developer Tools

## Steps Performed
1. Performed port scanning using Nmap
2. Identified open ports and services
3. Used OWASP ZAP for automated scanning
4. Analyzed vulnerabilities in alerts tab
5. Documented findings with screenshots

## Nmap Scan Results
- Port 80 (HTTP) – Open
- Port 443 (HTTPS) – Open
- Port 8080 – Open
- Server: Apache Tomcat/Coyote JSP engine

## Vulnerabilities Identified

### 1. Cross Site Scripting (XSS) – High
- Injected script executed in browser
- Can steal session cookies

### 2. SQL Injection – High
- Login form vulnerable to SQL queries
- Can bypass authentication

### 3. Absence of Anti-CSRF Tokens – Medium
- No protection against forged requests

### 4. Missing Security Headers – Low
- X-Content-Type-Options missing
- CSP header not set

## Impact
- Unauthorized access
- Data leakage
- Session hijacking
- System compromise

## Remediation
- Validate and sanitize inputs
- Use prepared statements
- Enable security headers
- Implement CSRF protection

## Screenshots
Check the screenshots folder for:
- Nmap scan
- ZAP scan
- Alerts
- XSS & SQL Injection proof

## Files Included
- Vulnerability report PDF
- Screenshots
- README documentation
