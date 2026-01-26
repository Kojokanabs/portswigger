# Inconsistent security controls

# Description 
Security checks are applied inconsistently across similar functionality.
Attackers can access restricted actions through less-protected endpoints.

# Lab Setup
* Platform: PortSwigger Web Security Academy
* Lab: Inconsistent security controls
* Target: Multiple business endpoints 

# Exploitation 
1 Identify functionality protected in one context
2 Locate alternate endpoints offering similar actions
3 Access the actions through a waeker endpoint
4 Bypass security checks 

# Result
* Restricted functionality accessed without authorization 

# Weakness 
* Security controls not uniformly enforced

# Mitigation
* Apply consistent authorization and validation across all endpoints 
* Centralize security logic 
