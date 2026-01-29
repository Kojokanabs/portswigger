Finding Hidden GraphQL Endpoint

# Description 
The appication uses a hidden GraphQL endpoint that is not directly exposed through the UI
Despite limited introspection defenses, the endpoint can still be discovered andabused

# Testing Context
* Platform: PortSwigger Web and Academy 
* Lab: Finding a hidden GraphQL endpoint

# Exploitation Steps
1. Analyze application traffic using Burp Suite
2. Review JavaScript files for hardcoded API path or GraphQL references
2. Identify potential GraphQL endpoint URLs
3. Send crafted GraphQL queries to the discovered endpoint
4. Execute privilege GraphQL mutations via the APIs.

# Security Impact 
* Unauthorized execution of administrative actions
* Complete bypass of access control mechanisms
* Risk of data loss, account manipulation, and service abuse.
* Severe compromises of application intergrity and trust boundaries  

# Root Cause Analysis
* The application relies on security through obscurity to protect sensitive GraphQL endpoint
* Authentication and authorization controls are not consistently enforced on the hidden endpoint.
* Disabling GraphQL introspection is incorrectly treated as a sufficient security control.
* APIs security assumptions are based on UI exposure rather than backend enforcement

# Why Automated Tools is Often Miss This
* The endpoint is not directly linked or advertised in application responses
* Discovery requires manual anaysis of JavaScript and network traffic
* Automated scanners typically do not enumerate undocumented GraphQL endpoints 
* THe vulnerability is logic-based rather than signature-based

# Secure-by-Design Mitigation
* Never  rely on hidden or undocumented endpoints for security
* Enforce authentication and authorization on all GraphQL activities
* Apply role-based access control for sensitive mutations
* Implement monitoring and alerting for abnormal GraphQL activity
* Treat introspection disabling as a hardening measure, not a security boundary

# OWASP Mapping
* OWASP Top 10:A01 - Broken Access Control
* OWASP API Top 10:API1 - Broken Object Level Authorization

