# 2FA_Simple_Bypass
 
# Description 
The 2FA mechanism is implemented but not properply enforced, allowing attackers to bypass it entirely.

# Lab Setup
* Lab: 2FA simple bypass 
* Flow: Login - 2FA verification 

# Exploitation Steps
1. Login with valid credentials
2. Intercept request before 2FA verification 
3. Directly access authentication endpoint 
4. Observe successful access without 2FA code

# Result
* Full authentification bypass
* Access granted without completing 2FA

* Weakness
* 2FA not enforced server-side 
* Authentication state set too early

# Mitigation 
* Enforce 2FA checks on every sensitives request 
* Only mark sessions as authenticated after successful 2FA 
