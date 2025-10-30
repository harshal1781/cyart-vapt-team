## 5. Mobile Application Testing Lab

* **Objective:** Use static and dynamic analysis to identify vulnerabilities in an Android APK.

* **Workflow:**
    1. **Static:** Uploaded `DivaApplication.apk` to MobSF. Detected hardcoded API keys and insecure SharedPreferences usage.
    2. Used `Frida` to hook `checkLogin()` and force it to return `true`, bypassing authentication logic.
    3. Used `Drozer` to enumerate exported activities and content providers, identifying weak IPC permissions and unauthorized access paths.

* **Key Finding:** Identified critical flaws including insecure data storage (OWASP M2), client-side authentication bypass (OWASP M4), and exposed IPC components (OWASP M8).
