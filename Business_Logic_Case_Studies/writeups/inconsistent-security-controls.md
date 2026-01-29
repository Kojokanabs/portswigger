# Inconsistent security controls

# Description 
The application applies Security controls  inconsistently across similar or related functionality.
While certain actions are properly protected in one context, equivalent functionality exposed through alternative endpoints lacks the same enforcement. The inconsistency alloows attackers to bypass restriction by accessing less-protected endpoints.

# Testing Context
* Platform: PortSwigger Web Security Academy
* Lab: Inconsistent security controls
* Target: Multiple business endpoints 

# Exploitation 
1 Identify functionality that is protected in one context
2 Locate alternate endpoints thatp perform equivalent actions
3 Access the same functionality through a weaker or unprotected endpoint
4 Bypass security checks and perform restricted actions

# Security Impact
* Unauthorized access to restricted functionality
* Bypass of authorization and validation controls
* Increase attack surface due to uneven security enforcement 
* Erosion of trust in access control and business logic integrity

# Root Cause Analysis
* Security controls are implemented per endpoint rather than per business capacity
* Authorization logic is duplicated and inconsistently applied
* No centralized enforcement mechanism for access control
* Security reviews focus on individual endpoints instead of functional equivalence

# Why Automated Tools Often Miss This
* The issue is logic-based rather than input-based
* Requires identifying functionally equivalent endpoints
* Automated scanners typically assess endpoints in isolation
* Tools lack awareness of intended access control consistency

# Secure-by-Design Mitigations
* Apply consistent authorization and validation across all endpoints
* Centralize security logic for authentication and authorization
* Enforce access control at the business-function level, not per route
* Regularly audit for functional duplication and security drift
* Design APIs assuming attackers will seek the weakest enforcement point

# OWASP Mapping
* OWASP Top 10:A01 Broken Access Control
* OWASP Top 10:A04 - Insecure Design 
