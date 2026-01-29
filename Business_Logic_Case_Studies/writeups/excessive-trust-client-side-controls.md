# Excessive trust in client-side controls

# Description
The application relies on client-side controls (such as hidden fields or disabled inputs) to enforce business rules
Attackers can modify these controls to perform unauthorized actions

# Testing Context
* Platform: PortSwigger Web Security Academy
* Lab: Excessive trust in client-side controls
* Target: Purchase/business action endpoint

# Exploitation Steps
1 Intercept a request containing client-controlled parameters
2 Identify hidden, disabled or restricted values (e.g., price, quantity)
3 Modify the parameters to an unauthorized values
4 Forward themanipulated request to bypass business restrictions 

# Security Impact
* Bypass of business rules and validation logic 
* Unauthorized purchases or state changes
* Financial loss and abuse of application functionality
* Loss of trust in transaction integrity

# Root Cause Analysis
* Business rules are enforced on the client side rather than the server side
* The backend trsut user-supplied input for security-crital decisions
* Server validation is incomplete or absent
* Threat modeling does not account for malicious client 

# Why Automated Tools Often Miss This
* The issue is logic-based, not injection-based
* Requires understanding of expected business constrainsts 
* Automated scanners rarely manipulate hidden or disabled paramters
* Tools typically lack context around valid vs invalid business values

# Secure-by-Design Mitigations
* Enforce all business rules and validations on the server side
* Treat all client-supplied input as untrusted(Zero Trust)
* Recalculate sensitive values(e.g, price, discounts) serve-side
* Implement integrity checks for critical transaction data
* Design workflows assuming an actively malicious client 

# OWASP Mapping
* OWASP Top 10:A04 - Insecure Design
* OWASP Top 10:A01 - Broken Access Control

