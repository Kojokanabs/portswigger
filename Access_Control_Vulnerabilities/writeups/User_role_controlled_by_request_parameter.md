# Description
The application determines user privilege based on a client-controlled request parameter.
Manipulating this parameter allows privilege escalation

# Lab Setup
* Platform: PotSwigger Web Security Academy
* Lab: User role controlled by request paramter
* Target: Role parameter in HTTP request 

# Exploitation
1 Intercept request in Burp Suite
2 Identify role-related parameter
3 Modify role value from user to admin
4 Forward request

# Result 
* User role escalation to administrator
* Admin-only functionality unlocked

# Weakness 
* Trusting user-supplied input for authorization decisions

# Mitigation
* Never trust client-side role indicators
* Derive authorization from server-side session data

