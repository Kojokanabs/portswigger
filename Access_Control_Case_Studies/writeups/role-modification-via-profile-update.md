# Description 
The application allows users to update sensitive attributes in their profile, including their role.
This enable unauthorized privilege escalation

# Lab Setup
* Platform: PortSwigger Web Security Academy 
* Lab: User role can be modified in user profile 
* Target: Profile update endpoint

# Exploitation Steps
1 Intercept profile update request 
2 Add or modify role parameter
3 Change role to admin
4 Submit request 

# Result 
* Account upgraded to administrator

# Weakness
* Lack of authorization checks on profile updates

# Mitigation
* Restrict modification of sensitive attributes
* Enforce server-side validation of allowed fields 

