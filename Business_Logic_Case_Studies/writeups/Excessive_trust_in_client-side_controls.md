# Excessive trust in client-side controls

# Description
The application relies on client-side controls (such as hidden fields or disabled inputs) to enforce business rules
Attackers can modify these controls to perform unauthorized actions

# Lab Setup
* Platform: PortSwigger Web Security Academy
* Lab: Excessive trust in client-side controls
* Target: Purchase/business action endpoint

# Exploitation Steps
1 Intercept a request containing client-controlled parameters
2 Identify hidden or restricted values (e.g., price, quantity)
3 Modify the parameter to an unauthorized value
4 Forward the request to bypass business restrictions 

# Result
* Business rules were bypassed 
* Unauthorized actions were successfully performed

# Weakness 
* Application trusts client-side input for critical decisions

# Mitigation
* Enforce all business rules server-side
* Treat client input as untrusted

