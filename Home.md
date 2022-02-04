NEED TO FIX LINKS HERE

# SSO Pathfinder Knowledge Base 
>If you are intending to use the Pathfinder SSO service in order to provide authentication for your application, the SSO Pathfinder Knowledge Base is for you. You are in the right place.

* [WHY PATHFINDER SSO?](https://github.com/bcgov/ocp-sso/wiki#why-pathfinder-sso)
* [WHY NOT PATHFINDER SSO?](https://github.com/bcgov/ocp-sso/wiki#why-not-pathfinder-sso)
* [WHAT'S CHANGED?](https://github.com/bcgov/ocp-sso/wiki#whats-changed)

<p align="center">
  <img width="380" height="300" src="https://user-images.githubusercontent.com/87393930/134059693-3b049537-1f5f-45e4-a31d-f6ab52b0431e.png">
</p>

<br>

<br>

#### *Have any questions? We would love to hear from you.* [![Semantic description of image](https://user-images.githubusercontent.com/87393930/133688357-09f82374-ba18-4402-8089-c0a989dde882.png)][2]   <a href="mailto:bcgov.sso@gov.bc.ca?"><img src="https://user-images.githubusercontent.com/87393930/133690650-b706e658-27bf-4066-92ba-3a7d8a4593ef.png"/></a>



[2]: https://chat.developer.gov.bc.ca/channel/sso
[3]: https://[mail](mailto:bcgov.sso@gov.bc.ca)[email](mailto:bcgov.sso@gov.bc.ca)



## Why Pathfinder SSO?

The Pathfinder SSO service (also known as "KeyCloak" or "RedHat SSO"). Provides a simple way for application development teams to set up login functionality for their app from approved identity providers over a standard, secure protocol.

An "Identity Provider" is the _holder_ of the identity that is used to log in with. The Pathfinder SSO service is _NOT_ an identity provider. When a user of your application logs in, they will not be providing credentials to your application directly, or even to the Pathfinder SSO service. They will be logging in directly with the identity provider. That login event is then propagated back to your application in the form of a token that proves that they have logged in correctly.

It is totally possible for your application to integrate with any or all of the identity providers directly instead of using the Pathfinder SSO service. The benefits of using Pathfinder SSO are:

- **Easy setup.** We've made this the #1 feature of this service. You can get your DEV, TEST, and PROD instances running against most of the available identity providers right away. The Pathfinder SSO service already has integrations to the following identity providers: 
  - IDIR (BC Common Logon Page)
  - BCeID Basic (BC Common Logon Page) -- Allows login only with BCeID _Basic_
  - BCeID Business (BC Common Logon Page) -- Allows login only with BCeID _Business_
  - BCeID Basic & Business(BC Common Logon Page) -- Allows login with BCeID _Basic_ or BCeID _Business_
  - GitHub _only in DEV and TEST environments at this time_

- **OIDC protocol.** Where certain identity providers (BCeID in particular) support SAML protocol when used directly, Pathfinder SSO brokers the SAML connection and lets you use OIDC instead. OIDC is more common and simpler to set up in modern programming stacks.
- **Session Management.** Some identity providers don't offer advanced session management capabilities.

- **High Availability Requirements.** The Pathfinder SSO service is working to a formal published service level agreements (see [BC Government SSO Service Definition](https://developer.gov.bc.ca/BC-Government-SSO-Service-Definition)). This service is available 24/7 with questions and answers addressed during business hours only. [Uptime Robot Monitoring](https://stats.uptimerobot.com/m8VZBU5QBW)


### Why Not Pathfinder SSO?
It is technically possible to integrate directly with the various identity providers instead of using OCP-SSO. Architectural reasons for direct integration include:


- **High Volume Expectations.** The service is shared by many dozens of applications. If one application starts sending millions of login requests, the service itself can experience service degradation which is felt by all the users of all the applications. Pathfinder SSO is managed on the OpenShift Platform and scales fluidly, but there are limits to the resources it can consume.
- **Unique Configuration Needs.** New customers no longer receive a dedicated realm where they can experiment and invent on top of the platform (see "What's Changed" below). 
- **BC Services Card Integration Requirements.** Because of the high-security nature of the BC Services Card identity and the private information that is available in the context of a login, BCSC is not allowed to be shared between applications. In a dedicated realm the BCSC integration, once approved and configured by IDIM, can be set up. Since we are not offering dedicated realms at this time, teams that need to integrate with BCSC will need to find another solution (see [BC Services Card Integration](https://github.com/bcgov/ocp-sso/wiki/BC-Service-Card-Integration) for useful advice).

## What's Changed?

As of 2021, the Pathfinder SSO service has changed it's service offering. Existing customers will not be affected, but new customers will experience a different service offering.

* Previously, customers were provisioned their very own KeyCloak *realm*. A realm is like a security zone that is protected from the configuration changes made by other realms. Each team worked in their own realm and was given access to the KeyCloak administration console for their realm where they could make any changes they wanted to.
* In 2020, the OCP-SSO service started to hit maximum capacity for realms in a way that was not possible to mitigate via the usual vertical and horizontal scaling approaches. The KeyCloak product was not designed to handle an unlimited number of realms and we managed to find the limit (unfortunately!).
* Until such time as we have another production instance of KeyCloak that can start adding new realms, new customers will now be added to one of the specially configured *standard realms*. Instead of receiving an entire realm per team, they will receive a pre-configured client inside an existing realm. There is no compromise to the security in this configuration, but it does mean that teams will no longer receive credentials to log on to the KeyCloak server and make changes to their configuration. Changes will be made by the operations team in response to requests for now (we're working on automations to solve this problem). Although this is a compromise in terms of the flexibility of the service, it actually makes setting up simpler and faster for teams.
* New customers get an easy-to-set-up *authentication* component. What about *authorization*? KeyCloak includes features that allow administrators to define roles and groups and assign users to these roles and groups. When a user logs in, their authorization context(s) come through to the application in the form of claims inside their token. The application can check the user's role and/or group membership and execute authorization-aware application logic based on the values. This feature is used by many of the existing applications supported by Pathfinder SSO (but not all of them). Because using this feature requires access to the KeyCloak administration console (or at least API) in order to administrate, it is not available to new customers that do not have their own realm (it would be a potential security breach to allow realm management in a realm shared by many applications). If you need an architectural solution for authorization, see [Handling Authorization](https://github.com/bcgov/ocp-sso/wiki/Handling-Authorization) for useful advice. We are working on providing authorization capabilities to customers in the standard realm, but at this time any authorization features must be handled by means of a request to the operations team.
* We have removed GitHub as an IDP in the production versions of the standard realms. The IDP is still available in dedicated realms and may return to the standard realms pending security review. GitHub is still available as an IDP in the DEV and TEST versions of the service, for teams that find that useful during development cycles.

--------------------



