# Description
The GraphQL API exposes private content due to missing authorization checks
Attackers can query umpublished or restricted posts by manipulating GraphQL queries.

# Lab Setup
* Platform: PortSwigger Web Security Academy
* Lab: Accessing private GraphQL posts
* Trget: GraphQL API endpoint

# Exploitation Steps
1. Intercept a GraphQL request using Burp Suite
2. Identify queries used to fetch public posts
3. Modify the query to request private or unpublished endpoints
4. Send the modified request to the GraphQL endpoint

# Result
* Private GraphQL posts were successfully accessed 
* Sensitive data was disclosed without authorization 

# Weakness 
* Missing access control checks at the GraphQL reoslvers level

# Mitigation
* Enforce authorization checks on all GraphQL resolvers
* Restrict access to sensitive fields based on user roles 

