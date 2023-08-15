Welcome community member, we have this page broken down into 2 sections: Who we are and your role as a Gold Custom Community Member and Guidelines we've jointly created with you


# Who is Who


<img   width="600" alt="whoiswho_thumb-Screen Shot 2022-10-05 at 10 28 20 AM" src="https://user-images.githubusercontent.com/56739669/194124175-79085809-5161-4f70-93a3-b713e5114635.png">

# Community Guidelines & Best Practices

Our community supports us and follows our general guidelines and best practices for:

1. Everyone in the space understands business requirements for privacy (IDs, authorizations, personal attributes)

2. For sharing purposes, need to review the STRA/security & PIA/privacy & legislation/policy for the space

3. Rely on out of the box configuration for Keycloak integrations as much as possible

&nbsp;&nbsp;&nbsp;&nbsp; a) ensure logs not are stored or only store for a short period of time.

4. try to avoid using realm-level resources such as groups and roles to share the realm with multiple application teams.

5. Use of GUID vs KC ID

&nbsp;&nbsp;&nbsp;&nbsp; a) don't use local users

6. Create instructions for realm usage, setup, and basic problem solving

7. make sure the user username has a suffix with ‘@{idp}’ and is based on the source of truth of the user type.

&nbsp;&nbsp;&nbsp;&nbsp; a) Offline validation (public key validation)

&nbsp;&nbsp;&nbsp;&nbsp; b) Automation

8. Session and realm configuration and token timeouts

&nbsp;&nbsp;&nbsp;&nbsp; a) ensure offline tokens are revoked after use or set the maximum time.   

&nbsp;&nbsp;&nbsp;&nbsp; b) validate the token at the application level rather than using an introspection endpoint 

9. Processes for maintaining and configuring environments 

10. Use Cypress to automate login tests

11. Documentation around how to get access to diff tiers of support

12. Create a clear Disaster Recovery plan

13. Synchronization of changes between environments






#### *Have any questions? We would love to hear from you.[Rocketchat](https://chat.developer.gov.bc.ca/channel/sso) OR [Email](mailto:bcgov.sso@gov.bc.ca)



