# Password Reset Poisoning 

# Description 
The password reset functionality trust user-supplied headers when generating rest links Attackers can poison the reset process to receive password reset links for other users.

# Lab Setup
* Platform: PortSwigger Web Security Academy
* Lab: Password reset poisoning
* Target: Password reset endpoint

# Expliotation Steps
1 Initiate a password reset request
2 Intercept the request using Burp Suite
3 Modify headers such as Host or X-FOrward-Host
4 Capture the piosoned password reset link sent by the application

# Result 
* Password reset link was sent to an attacker-controlled domain
* Account takeover become possible

# Weakness
* Trust in user-controlled headers when generating sensitive links 
* Lack of validation of canonical application domain

# Mitigation
* Use a fixed, server-side domain for reset links
* Ignore untrusted headers when generating URLs
* Validate all password reset workflows strictly  
