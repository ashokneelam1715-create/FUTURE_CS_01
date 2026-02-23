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

