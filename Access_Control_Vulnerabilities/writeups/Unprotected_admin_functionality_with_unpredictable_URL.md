# Description 
The application hides the admin panel behind on obscure URL but does not enforce access control
Once discovered, the endpooint is fully accessible.

# Lab Setup
* Platform: PortSwigger Web Security Academy
* Lab: Unprotected admin functionlity with unpredictable URL
* Target: Hidden admin endpoint

# Exploitation Steps
1 Review application source or JavaScript files
2 Identify hidden admin URL
3 Access the endpoint directly 

# Result
* Full admin access obtained without authorization

# Weakness 
* Security by obscurity 
* No authorization checks on sensitive endpoint 

# Mitigation 
* Do not rely on hidden URL for security 
* Apply strict server-side access control 
