# Password_Reset_Broken_Logic 

# Description 
The password reset functionality contains logical flaws that allow attackers to reset passwords without proper verification.

#Lab Setup
* Lab: Password reset broken logic 
* Target /forget-password and reset endpoints

# Exploitation Steps
1. Initiate password reset
2. Intercept reset request
3. Manipulation parameters (email /token/user references)
4. Bypass intended verification

# Result
* Account takeover acieved without owning the victim;s email


# Weakness 
* Server trust client-side parameters
* Missing strict validation of reset tokens

# Mitigation
1. Bind reset token to:
 * Specific user
 * Single session
 * Short expiration time
2. Valid token server-side only 
