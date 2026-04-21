# Command Injection

- Allows execution of OS commands via user input.

### Exploitation

- Input:
    
    `; ls`
    
- Injected into system command → executes on server
- This can lead to :
    - Remote Code Execution

### Remediation

- Avoid direct system calls
- Use safe APIs
- Input validation & sanitization