## 4. Network Protocol Attacks Lab

* **Objective:** Intercept network traffic and harvest credentials using MitM attacks.
* **Workflow:**
    1.  Executed `Responder` on the lab network.
    2.  Waited for a victim machine (`192.168.18.132`) to broadcast an LLMNR request.
    3.  Successfully captured an NTLMv2 hash from the victim.
    4.  (Separately) Used `Ettercap` to perform an ARP spoofing attack, intercepting HTTP traffic and capturing clear-text credentials.
* **Key Finding:** Lack of network segmentation and use of unencrypted protocols (HTTP) puts credentials at high risk of interception.
