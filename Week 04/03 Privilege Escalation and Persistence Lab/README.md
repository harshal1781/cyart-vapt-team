## 3. Privilege Escalation and Persistence Lab

* **Objective:** Gain root access on a target VM and establish persistence.
* **Workflow:**
    1.  Gained initial shell as `www-data`.
    2.  Uploaded and executed `LinPEAS.sh` for enumeration.
    3.  `LinPEAS` identified a SUID binary (`/usr/bin/find`).
    4.  Used GTFOBins to exploit the SUID `find` binary (`find . -exec /bin/sh -p \; -quit`) and gained a `root` shell.
    5.  Established persistence by adding a reverse shell command to the `root` crontab.
* **Key Finding:** Misconfigured SUID binary provided a direct path to root.
