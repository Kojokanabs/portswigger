# Username_Enumeration_via_Subtly_Diffrent_Responses

# Description
The application returns slightly diffrent error messages depending on whether a username exits or not.
Although subtle, these diffrences allow attackers to confirm valid usernames.

# Labs Setups

* Platform: PortSwigger Web Security Academy.
* Lab: Username enumeration via diffrent responses.
* Target: LOgin endpoint

# Exploitation Steps
1. Intercept login request in Burp Suite
2. Send multiple login attempts with:
   * Valid username + wrong password
   * Invalid username + random password
3. Observe diffrences in the response such as:
   * "Invalid password"
   * "Invalid uername or password"

# Results
* Valid usernames were successfully enumerated
* Attackers can reduce brute-force scope significantly

# Weakness
* Application leaks authentication state through error messages

# Mitigation
* Use generic error messages for all authentication failures
e.g "Invalid username or password" for every case.   
