Welcome community member, we have this page broken down into 2 sections: Who we are and your role as a Gold Custom Community Member and Guidelines we've jointly created with you


# Who is Who


<img   width="600" alt="whoiswho_thumb-Screen Shot 2022-10-05 at 10 28 20 AM" src="https://user-images.githubusercontent.com/56739669/194124175-79085809-5161-4f70-93a3-b713e5114635.png">

# Community Guidelines & Best Practices

Our community supports us and follows our general guidelines and best practices for:

* Everyone in the space understands business requirements for privacy (IDs, authorizations, personal attributes)

* For sharing purposes, need to review the STRA/security & PIA/privacy & legislation/policy for the space

* Rely on out of the box configuration for Keycloak integrations as much as possible

1. ensure logs not are stored or only store for a short period of time.

1. try to avoid using realm-level resources such as groups and roles to share the realm with multiple application teams.

* Use of GUID vs KC ID

1. don't use local users

* Create instructions for realm usage, setup, and basic problem solving

1. make sure the user username has a suffix with ‘@{idp}’ and is based on the source of truth of the user type.

* Offline validation (public key validation)

* Automation

* Session and realm configuration and token timeouts

1. ensure offline tokens are revoked after use or set the maximum time.   

1. validate the token at the application level rather than using an introspection endpoint 

* Processes for maintaining and configuring environments 

* Use Cypress to automate login tests

* Documentation around how to get access to diff tiers of support

* Create a clear Disaster Recovery plan

* Synchronization of changes between environments






#### *Have any questions? We would love to hear from you.[Rocketchat](https://chat.developer.gov.bc.ca/channel/sso) OR [Email](mailto:bcgov.sso@gov.bc.ca)



