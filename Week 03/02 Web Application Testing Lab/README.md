# Lab 2: Web Application Testing Workflow

This lab involved a comprehensive assessment of the Damn Vulnerable Web Application (DVWA).

## Workflow

1.  **Setup**: Deployed DVWA on a local VM. Set the security level to "Low" for initial testing.
2.  **Automated Scanning**: Used `sqlmap` to automatically detect and confirm a critical SQL Injection vulnerability in the user ID parameter.
3.  **Manual Testing**:
    * Used Burp Suite to intercept HTTP requests and manipulate session cookies to test for broken session management.
    * Manually injected payloads (`<script>alert(1)</script>`) to confirm Reflected XSS vulnerabilities in input forms.
4.  **Documentation**: All findings were logged, and a checklist for future web assessments was created.
