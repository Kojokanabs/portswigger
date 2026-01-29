Accidental Exposure of Private GraphQL fields
 
# Description
The GraphQL API unintentionally exposes sensitive user credential fields
Attacker can induce the API to return confidential data due to improper access control.

# Testing Context:
* Plaform: PortSwigger Web Security Academy
* Scenario: Accidental exposure of private GraphQL fields
* Target: GraphQL user management endpoint

# Exploitation Steps 
1. Authenticate as a privildge user
2. Intercept GraphQL queries related to user managememt 
3. Modify queries to request sensitve credential fields 
4. Extract exposed data and perform unauthorized priviledge actions

# Security Impact
* Disclosure of sensitive credential-related fields 
* Abuse of administrative functionality
* Risk of account compromise and data integrity loss  

# Root-Cause-Analysis
* Overly permissive GraphQL schema
* Missing field-level authorization controls

# Secure-by-Design MItigations
* Restrict sensitive fields using explicit schema allowlist
* Enforce field-level authorization based on user roles
* Apply deny-by-default access control for GraphQL fields

# OWASP Mapping
* AO1- Broken Access Control
 
