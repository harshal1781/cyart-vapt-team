## 2. API Security Testing Lab

* **Objective:** Identify and exploit OWASP API Top 10 vulnerabilities in a test environment.
* **Workflow:**
    1.  Set up Burp Suite to proxy traffic from the DVWA API.
    2.  Enumerated API endpoints (`/api/users`, `/graphql`).
    3.  Tested for BOLA by logging in as `user1` and requesting `/api/users/2` in Burp Repeater. Successfully retrieved `admin` user data.
    4.  Used Postman to send GraphQL introspection queries, successfully mapping the database schema.
* **Key Finding:** Critical BOLA (A01:2023) vulnerability identified, allowing any user to access all other user data.
