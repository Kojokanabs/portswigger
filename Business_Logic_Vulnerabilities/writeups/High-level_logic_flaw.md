# High-level logic flaw

# Description
The application enforces individual checks correctly but fails to consider the overall business logic
Attackers can exploit this gap to achieve unintended outcomes

# Lab Setup
* Platform: PortSwigger Web Security Academy
* Lab: High-level logic flaw
* Target: Application workflow

* Exploitation Steps
1 Understand the intended business workflow
2 Identify assumptions made by the application
3 Manipulate the order or combination of actions
4 Achieve a result that violate business intent 

# Result 
* Application behavior deviated from intended logic 
* Business contrainsts were bypassed 

# Weakness
* Incomplete modeling of business logic
* Lack of holistic validation

# Mitigation
* Threat-model business workflows 
* Validate outcomes, not just individual steps
                               
