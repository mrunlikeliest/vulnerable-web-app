# vulnerable-web-app
This repository is made for having a web application to test OWASP ZAP, how it can be used to test the application manually as well as using GitHub actions

The web application is available at: https://mrunlikeliest.github.io/vulnerable-web-app/

Vulnerabilities in This Web App
Cross-Site Scripting (XSS):

The search input on search.html is vulnerable to XSS because user input is directly injected into the DOM without sanitization.
Test with payloads like:
php
Copy
Edit
<script>alert('XSS')</script>
Insecure Direct Object Reference (IDOR):

The user.html page allows users to view any profile by modifying the id parameter in the URL:
bash
Copy
Edit
https://<your-url>/user.html?id=2
No Authentication or Input Validation:

No input validation or authorization checks are implemented, making it easier to exploit vulnerabilities.
