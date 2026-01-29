Accessing to Private GraphQL Posts via Missing Authorization

# Description
The GraphQL API exposes private content due to missing authorization checks
Attackers can query umpublished or restricted posts by manipulating GraphQL queries.

# Testing Context:
* Platform: PortSwigger Web Security Academy
* Scenario: Accessing private GraphQL posts

# Exploitation Steps
1. Intercept a GraphQL request using Burp Suite
2. Identify queries used to fetch public posts
3. Modify the query to request private or unpublished endpoints
4. Send the modified request to the GraphQL endpoint
5. Obeserve the server response containing restricted content

# Security Impact
* Unauthorized access to private or unpublished content
* Sensitive information disclosure
* Violation of access control and data confidentiality gurantees
* Potential regulatory and privacy compliance impact 

# Root Cause Analysis
* Authorization checks are not enforce within GraphQL resolvers
* Access controls decisions are applied at the API entry point but not per object or field
* The API trusts that client will only request permitted fields and resources

# Why Automated Tools Often Miss This
* The vulnerability is logic-based, not injection-based
* Requires understanding of Graph schema and resolver behavior
* Automated scanners typically do not modify GraphQL queries to access unauthorized fields or objects.

# Secure-by-Design Mitigations
* Enforce authorization checks within every GraphQL resolver.
* Apply object-level and field-level access control
* Implement a deny-by-default aunthorization model
* Restrict schema exposure and disable introspection in production where possible.

# OWASP Mapping
* OWASP Top 10: A01-Broken Access Control

