# What is keycloak?
Keycloak is an open source Identity and Access Management solution aimed at modern applications and services. It makes it easy to secure applications and services with little to no code. [Keycloak - About](https://www.keycloak.org/)

In BC Government, the Pathfinder SSO Keycloak server acts as an Open ID Connect [OIDC](https://openid.net/connect/) based Identity Provider, mediating with an enterprise user directory or 3rd-party SSO providers for identity information and applications via standards-based tokens and identity assertions.

<img src="https://user-images.githubusercontent.com/56739669/146436802-d9ab5a10-0946-4158-9c72-7943664e433e.jpg" >


## As a digital delivery team, what do i need to know about Keycloak?

Keycloak is organized by _realms_ which manages discrete sets of users that are logically isolated from one another and provides a linkage between the client application and a BC Government Identity Provider.

BC Pathfinder SSO Clients are configured to be part of a Standard Realm where certain realm parameters can be configured by clients and users can only authenticate to the realm in which they belong.

## Why a Standard Realm?
The KeyCloak product was not designed to handle an unlimited number of realms and we managed to find the limit (unfortunately!).

New customers will now be added to one of the specially configured standard realms to help us continue to offer this great common component.

<img src="https://user-images.githubusercontent.com/56739669/138940137-b8f939e2-3d8b-4083-b492-b96e219153c2.png" width="65%" height="50%">

# What are identity providers, and which are available to BC Government?
Identity providers are directories of user accounts with details about those users, called attributes. The ones availbe to Pathfinder SSO Clients are:
- **IDIR** IDIR accounts are given to individuals who work for the B.C. government. Each account has an IDIR username and password for logging in. [reference](https://www2.gov.bc.ca/gov/content/governments/services-for-government/information-management-technology/identity-and-authentication-services/login-best-practices/language-consistency)
- **BCeID** BCeID Accounts enable people to access government services using a single identifier and password.[reference](https://www2.gov.bc.ca/gov/content/governments/services-for-government/information-management-technology/identity-and-authentication-services/bceid-authentication-service)
- **BCSC (BC Services Card)**	The BC Services Card provides access to government services for B.C. residents [reference](https://www2.gov.bc.ca/gov/content/governments/government-id/bc-services-card/log-in-with-card)


# Authentication vs Authorization

Authentication is the process of verifying who someone is, whereas authorization is the process of verifying what specific applications, files, and data a user has access to.

Pathfinder SSO provides authentication only at this time. Teams will need to provide their own authorization means if they leverage the service.

For further detail on the OAuth2 flow being used for clients in the standard realm, please see the [Authorization Code Flow](https://auth0.com/docs/authorization/flows/authorization-code-flow). 