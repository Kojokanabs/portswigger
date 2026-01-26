# Description 
The application allows user to access other users' data by modifying object identifires in requests.

# Lab Setup
* Platform: PortSwigger Web Security Academy
* Horizontal privilege escalation 
* Target: User-specific resources endpoint 

# Exploitation
1 Intercept request accessing user data
2 Modify user ID or Identifiers 
3 Forward request  

# Result 
* Access to another user's sensitive information 

# Weakness 
* Insecure Direct Object Reference (IDOR)
* Missing ownership checks

# Mitigation
* Verify resource ownership
* Enforce access control per object
 

