# Server Side Request Forgery (SSRF)

- SSRF tricks a server into making requests to internal or external resources.

### Exploitation

- Input :
    
    `http://localhost/admin`
    
- Server accesses internal service
- This can lead to :
    - Internal Endpoint disclosure
    - Admin panel access

### Remediation

- Validate URLs
- Block Internal IP ranges
- Use allowlists