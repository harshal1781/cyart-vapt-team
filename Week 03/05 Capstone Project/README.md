# Lab 5: Capstone Project Workflow

This project simulated an end-to-end VAPT engagement against the Kioptrix: Level 1 virtual machine using Kali Linux and Metasploit.

## Workflow

1. **Reconnaissance**  
   Conducted network discovery using `netdiscover` and service enumeration with `nmap` on target IP. Open ports included 22 (SSH), 80 (HTTP), and 139 (Samba). OpenVAS confirmed a critical vulnerability in the Samba service (version 2.2.1a).

2. **Exploitation**  
   Leveraged Metasploit’s `exploit/multi/samba/usermap_script` and `exploit/linux/samba/trans2open` modules to exploit the Samba vulnerability. A reverse shell was successfully obtained using the `linux/x86/shell_reverse_tcp` payload. Multiple sessions were established and verified.

3. **Privilege Escalation**  
   Identified a vulnerable SUID binary (`/usr/bin/nmap`). Used interactive mode to escalate privileges to root (`!sh`). Verified root access with `whoami` and `id`.

4. **Evidence Collection**  
   Retrieved sensitive files (`/etc/passwd`, `/etc/shadow`) and hashed them locally using `sha256sum` to maintain forensic integrity. Chain-of-custody was documented.

5. **Remediation Planning**  
   Recommended upgrading Samba to a secure version, disabling unused shares, and restricting SMB ports (139/445) via firewall. A follow-up OpenVAS scan confirmed successful remediation.

6. **Reporting**  
   Delivered a PTES-compliant report including technical findings and a non-technical summary for stakeholders. Documentation included session logs, evidence hashes, and remediation verification.
