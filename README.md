# FUTURE_CS_01
Cyber Security Internship - Task 1 Vulnerability Assessment Report

## Introduction
This report presents the results of a vulnerability assessment 
conducted on a test website using Nmap.

## Target Information
Target: testphp.vulnweb.com  
Scan Type: Service Version Detection (-sV)

## Scan Results

Open Ports:
- 80/tcp (HTTP)
- 443/tcp (HTTPS)

Service: Cloudflare Proxy

Observation: Multiple web ports are exposed.

## Risk Classification
Risk Level: Low

Reason: Open ports are required for web services, 
but exposure should be monitored.

## Recommendations
- Close unnecessary ports.
- Use proper firewall configuration.
- Keep server software updated.
- Enable security monitoring.

## Scan Screenshot
![Nmap Scan](scan%20report.jpeg)



## Phase 2 – OWASP ZAP Scan

### Tool Used
OWASP ZAP 2.17.0 (Automated Scan)

### Target
http://testphp.vulnweb.com

### Scan Method
An automated scan was performed using OWASP ZAP.  
The tool crawled the application and conducted active vulnerability testing.

---

## Vulnerabilities Identified

- Cross Site Scripting (Reflected) – 19
- SQL Injection
- SQL Injection – MySQL (9)
- Absence of Anti-CSRF Tokens
- Content Security Policy Not Set
- XSLT Injection (2)
- Missing Anti-clickjacking Header

---

## Risk Level
High

---

## Risk Explanation

The presence of SQL Injection and Cross-Site Scripting vulnerabilities indicates critical security weaknesses.  
Attackers may exploit these issues to steal sensitive data, manipulate application behavior, or compromise the backend database.

---

## Business Impact

- Data Breach
- Credential Theft
- Financial Loss
- System Compromise

---

## Recommendations

- Implement input validation and output encoding
- Use prepared statements to prevent SQL Injection
- Enable CSRF protection tokens
- Configure Content Security Policy (CSP)
- Set proper security headers

---

## Evidence

[Download Full ZAP Report](ZAP_Report_file.pdf)



