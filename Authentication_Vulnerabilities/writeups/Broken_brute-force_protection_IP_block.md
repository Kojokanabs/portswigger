# Brute-Force Protection (IP Block Bypass)

# Description 
The application blocks brute-force attempts based soley on IP address.
Attackers can bypass this control by rotating or spoofing IP-related headers

# Lab Setup
* Platform: PortSwigger Web Security Academy 
* Lab: Broken brute-force protection, IP block
* Target: LOgin endpoint

# Exploitation 
1 Trigger IP-based blocking through repeated login failures
2 Modify headers such as X-Forward-For
3 Replay login attempts from different spoofed IPs
4 Observe that brute-force attempts continue without restriction

# Result
* IP-based blocking was bypassed
* Authentication attempts continued unhindered

# Weakness
* Overreliance on IP address for security decision
* Trust in user-controlled headers

# Mitigation
* Do not trust client-supplied IP headers
* Combine IP tracking with user-based and behavioral controls
* Apply rate limits at application and infrastructure levels

