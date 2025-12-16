# Web Application Security Testing Report

## 1. Introduction
This report documents the results of a basic web application security assessment conducted as part of the Future Interns Cyber Security Internship – Task 1.

The testing was performed on a deliberately vulnerable application to understand common web security issues.

## 2. Target Application
- Application Name: Damn Vulnerable Web Application (DVWA)
- Environment: TryHackMe AttackBox
- Access Type: Authorized lab environment

## 3. Tool Used
- OWASP ZAP (Zed Attack Proxy)

OWASP ZAP was used to perform an automated vulnerability scan to identify common security misconfigurations and weaknesses.

## 4. Identified Vulnerabilities

### 4.1 Absence of Anti-CSRF Tokens
- Risk Level: Medium
- Description: Forms in the application do not include Anti-CSRF tokens, making them vulnerable to Cross-Site Request Forgery attacks.
- Impact: Attackers may trick authenticated users into performing unintended actions.
- Mitigation: Implement Anti-CSRF tokens in all state-changing forms.

### 4.2 Missing Anti-Clickjacking Header
- Risk Level: Medium
- Description: The application does not include X-Frame-Options or Content-Security-Policy headers.
- Impact: The application may be vulnerable to clickjacking attacks.
- Mitigation: Add X-Frame-Options or frame-ancestors directive in CSP.

### 4.3 Security Header Misconfigurations
- Risk Level: Low to Medium
- Description: Multiple security headers such as X-Content-Type-Options and HttpOnly cookie flags were missing.
- Impact: Increased exposure to client-side attacks.
- Mitigation: Properly configure HTTP security headers.

## 5. Conclusion
The assessment identified multiple security weaknesses related to missing security controls and improper configurations. These issues highlight the importance of implementing secure development practices and regular security testing.

This task helped in understanding practical web application security testing using OWASP ZAP.
