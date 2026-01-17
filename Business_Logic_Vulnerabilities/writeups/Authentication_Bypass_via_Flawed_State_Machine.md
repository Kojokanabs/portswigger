# Authentication Bypass via Flawed state Machine
The application implements authentication as a multi-step process but fails to correctly enforce the required order of steps.
By manipulating the authentication flow, an attacker can reach an authenticated state without completing all required checks

# Lab Setup
* Platform: PortSwigger Web Security Academy
* Lab: Authentication bypass via flawed state machine
* Target: Login and post-authentication endpoints

# Exploitation Steps
1 Start the login process with valid credentials
2 Intercept requests using Burp Suite
3 Skip or replay authentication steps out of order
4 Directly access authenticated endpoints without completing the full login flow

# Result
* Authentication was successfully bypassed 
* Access to protected resources was obtained without proper authentication

# Weakness
* Authentication logic relies on client-side state
* Backend does not strictly enforce authentication step sequence 

# Mitigation
* Enforce authentication state transitions server-side
* Ensure users cannot access protected endpoint unless authentication steps are completed
* Avoid trusting client-controlled workflow state


