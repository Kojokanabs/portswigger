# Description
A horizontal priviledge escalation flaw can be chained to gain vertical (admin) priviledge

# Lab Setup
* Platform: PortSwigger Web Security Academy
* Lab: Horizontal to vertical priviledge escalation

# Exploitation Steps 
1 Exploitation IDOR to access another user's data
2 Identify admin user functionality 
3 Use obtained access to perform admin actions

# Result
* Full administrative access achieved

# Weakness 
* Chained authorization failures 
* Lack of priviledge separation  

# Mitigation
* Enforcement strict authorization at every priviledge level
* Apply defense-in-depth access controls  
