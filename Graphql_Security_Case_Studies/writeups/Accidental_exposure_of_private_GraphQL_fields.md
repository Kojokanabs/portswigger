# Description
The GraphQL API unintentionally exposes sensitive user credential fields
Attacker can induce the API to return confidential data due to improper access control.

# Lab Setup
* Platform: PortSwigger Web Security Academy
* Lab: Accidental exposure of private GraphQL fields
* Target: GraphQL user management endpoint

# Exploitation Steps 
1. LOng in as an administrator
2. Intercept GraphQL queries related to user managememt 
3. Modify queries to request sensitve credential fields 
4. Extract exposed data and perform priviledge actions

# Result
* Private credentials fields were dosclosed 
* Adminstrative privileges were abused to delete user carlos  

# Weakness
* Overly persissive GraphQL schema
* Sensitive fields not properly restricted

# MItigation
* Limit GraphQL filed exposure using strict schema design
* Apply role-based access control to sensitive fields
 
