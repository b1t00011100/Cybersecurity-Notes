# SQL Injection

- SQL Injection is an vulnerability where an attacker injects malicious SQL queries into input fields to manipulate the database.

### Exploitation

- Attacker finds input fields (login, search, URL param)
- Injects payloads like :
    
    `' OR 1=1 --` 
    
- If input is not validated, then query changes.
- This can :
    - Bypass Login
    - Dump databases
    - Modify / Delete data

### Remediation

- Use parameterized queries / prepared statements
- Input validation and sanitization
- Least privilege for db users
- Avoid displaying SQL errors