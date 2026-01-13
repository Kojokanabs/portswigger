# Username_Enumeration_via_Response_Timing

# Description
The application processes requests diffrently based on whether a username exits,leading to measurable timing diffrences.

# Lab Setup
* Username enumeration via response timing 
* Tools: Burp Intruder

# Exploitation Steps
1. Capture login request 
2. Use intruder with:
 * Payload list of usernames
 * Fixed incorrect password
3. Analyze response time
4. Identify usernames with consistently longer responses

# Results 
* Valid usernames identified based on delayed responses

# Weakness
* Backend performs extra operations (e.g password hashing)  only for valid users

# Mitigation
* Ensure constant-time authentication logic
* Perform same operations regardless of username validity

