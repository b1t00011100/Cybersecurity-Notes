# Directory Traversal

- Allows access to restricted files/directories.

### Exploitation

- Payload :
    
    `../../etc/passwd`
    
- Moves outside intended directory
- This can lead to :
    - Sensitive file disclosure
    - Credential leakage
    - Source code disclosure

### Remediation

- Validate file paths
- Use allowlists
- Restrict access to sensitive files