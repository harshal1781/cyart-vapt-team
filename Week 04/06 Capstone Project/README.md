## 6. Capstone Project: Full VAPT Engagement

* **Objective:** Conduct a full PTES-based engagement on a HackTheBox machine (Lame).
* **Workflow:**
    1.  **Recon:** `nmap -sC -sV 192.168.18.138` identified `vsftpd 2.3.4`.
    2.  **Exploitation:** Used the `vsftpd_234_backdoor` Metasploit module to gain immediate `root` access.
    3.  **Post-Exploitation:** Enumerated system, located flags.
    4.  **Reporting:** Compiled all findings into a professional PTES report.
    5.  **Remediation:** Recommended immediate patching/replacement of the VSFTPD service. Rescanned with OpenVAS (simulated) to confirm the fix.
* **Key Finding:** An outdated, known-vulnerable service provided a direct, unauthenticated path to root.
