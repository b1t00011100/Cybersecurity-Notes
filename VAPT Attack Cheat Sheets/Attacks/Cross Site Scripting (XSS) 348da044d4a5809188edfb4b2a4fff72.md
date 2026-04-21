# Cross Site Scripting (XSS)

- XSS is a vulnerability where an attacker injects malicious JavaScript into a web application, which then executed in another user’s browser.

### Exploitation

- Attacker finds an input field (search box, comment section, URL param)
- Inject a payload like :
    
    `<script>alert(1)</script>`
    
- If the app doesn’t sanitize output, the script runs in the victim’s browser
- This can lead to :
    - Session Hijacking (stealing cookies)
    - Credential theft
    - Defacing the page

#### Types

1. **Stored XSS** - saved in DB (most dangerous)
2. **Reflected XSS -** comes via request
3. **DOM-based XSS** - handled on client side

### Remediation

- Output encoding (Most Important)
- Input validation & sanitization
- Use Content Security Policy (CSP)
- Secure cookies attribute (HttpOnly, Secure flags)