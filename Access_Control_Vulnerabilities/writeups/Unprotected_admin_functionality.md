# Description 

The application exposes an admin endpoint without enforcing proper access control.
Any authenticated or unauthenticated user can access admin functionality directly via the URL

# Lab Setup
* Platform: PortSwigger Web Security Academy
* Lab: Unprotected admin functionality
* Target: /admin endpoint

# Exploitation Steps
1 Browse the application as a normal user
2 Manually access the /admin endpoint
3 Observe that administrative functions are accessible

# Result
* Unauthorized users gained access to admin functionality
* Critical actions (e.g. deleting user 'Carlos') can be performed

# Weakness 
* Missing server-side authorization checks
* Reliance on UI restrictions instead of access control

# Mitigation
* Enforce role-based access control on all sensitive endpoints 
* Validate user permissions on the server for every request
