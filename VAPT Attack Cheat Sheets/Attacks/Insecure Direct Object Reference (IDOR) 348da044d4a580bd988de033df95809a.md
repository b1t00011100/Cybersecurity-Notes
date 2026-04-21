# Insecure Direct Object Reference (IDOR)

- IDOR occurs when application exposes internal object identifiers (like user IDs) without proper authorization checks.

### Exploitation

- Change IDs in URL/API:
    
    `/api/user/123` → `/api/user/124`
    
- If no auth check → access other user’s data
- This can lead to :
    - Data breaches
    - Lack in Confidentiality

### Remediation

- Implement proper authorization checks
- Use indirect references
- Validate user access on server side