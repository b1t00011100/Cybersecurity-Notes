# Session Fixation

- Attacker forces a user to use a known session ID.

### Exploitation

- Send victim a fixed session link
- Victim logs in → attacker reuses session
- This can lead to :
    - Account Hijacking
    - User impersonation
    - Data theft
    - Unauthorized transactions
    - Privilege Escalation
    - Malicious Activity

### Remediation

- Regenerate session IDs after login
- Secure session handling