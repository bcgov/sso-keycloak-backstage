* [Intro to terms](#Intro-to-terms)
* [Learn about the Open ID connect and OAuth Protocols](#Learn-about-the-Open-ID-connect-and-OAuth-Protocols)
* [Learn about Keycloak and its APIs](#Learn-about-Keycloak-and-its-APIs)
* [How to set up and use your KeyCloak Client](#How-to-set-up-and-use-your-KeyCloak-Client)
* [Q&A with Us](#Q\&A-with-Us)
* [Azure IDIR and IDIR - What's the difference?](#Azure-IDIR-and-IDIR-What's-the-difference)


## Intro to terms

### Authentication 

Authentication is the process of verifying who someone is

### Authorization

Authorization is the process of verifying what specific applications, files, and data a user has access to. For further detail on the OAuth2 flow being used for clients in the standard realm, please see the [Authorization Code Flow](https://auth0.com/docs/authorization/flows/authorization-code-flow).


### Identity Provider 

An "Identity Provider" is the holder of the identity that is used to log in with. The Pathfinder SSO service is NOT an identity provider. When a user of your application logs in, they will not be providing credentials to your application directly, or even to the Pathfinder SSO service. They will be logging in directly with the identity provider. That login event is then propagated back to your application in the form of a token that proves that they have logged in correctly.

### [Keycloak how we describe it](https://github.com/bcgov/sso-keycloak/wiki/What-is-Keycloak-@-BC-Government%3F#what-is-keycloak) 

### Newbie Guide

Visit [this page](https://github.com/bcgov/sso-keycloak/discussions/136) to understand key concepts and terms as you make use of our Self Service application to integrate your digital application with a with BC government approved login option.


## Learn about the Open ID connect and OAuth Protocols
### Readings for OAuth 2.0:
- https://tools.ietf.org/html/rfc6749
- https://brockallen.com/2019/01/03/the-state-of-the-implicit-flow-in-oauth2/
- https://tools.ietf.org/html/rfc6819
- https://tools.ietf.org/html/draft-ietf-oauth-security-topics-13
- https://tools.ietf.org/html/draft-parecki-oauth-browser-based-apps-02

### OIDC 101
The following links are a good introduction or refresher to the OIDC standard.
- [SAML2 vs JWT: Understanding OpenID Connect Part 1](https://medium.com/@robert.broeckelmann/saml2-vs-jwt-understanding-openid-connect-part-1-fffe0d50f953)
- [SAML2 vs JWT: Understanding OpenID Connect Part 2](https://medium.com/@robert.broeckelmann/saml2-vs-jwt-understanding-openid-connect-part-2-f361ca867baa)



## Learn about Keycloak and its APIs

* [Red Hat SSO (Keycloak)](https://access.redhat.com/documentation/en-us/red_hat_single_sign-on/7.4/)
* [Realm Admin guide](https://access.redhat.com/documentation/en-us/red_hat_single_sign-on/7.4/html/server_administration_guide/index)
* [API usage](https://access.redhat.com/webassets/avalon/d/red-hat-single-sign-on/version-7.4/restapi/)
## How to set up and use your KeyCloak Client
- [How OIDC authorization code flow works with a public client](https://www.pingidentity.com/en/company/blog/posts/2018/securely-using-oidc-authorization-code-flow-public-client-single-page-apps.html)

## Q&A with Us

[Github Discussions Q&A on Gold](https://github.com/bcgov/sso-keycloak/discussions/categories/gold-q-a)

[Stackover flow Collection 1](https://stackoverflow.developer.gov.bc.ca/collections/179) 

[Stackover flow Collection 2](https://stackoverflow.developer.gov.bc.ca/search?q=custom+realm) 


## Azure IDIR and IDIR - What's the difference?
Using Azure IDIR adds the benefit of MFA (multi-factor authentication). This is a step up security-wise from regular IDIR. 

You may have to educate your end users on MFA and please take note if your IDIR is not tied to a gov.bc.ca email address, please use idir_username@gov.bc.ca when prompted for your email. 

You can **learn** [here from our IDIR Partner](https://intranet.gov.bc.ca/thehub/ocio/ocio-enterprise-services/information-security-branch/information-security-mfa/mfa-registration)

#### *Have any questions? We would love to hear from you.* [![Semantic description of image](https://user-images.githubusercontent.com/87393930/133688357-09f82374-ba18-4402-8089-c0a989dde882.png)][2]   <a href="mailto:bcgov.sso@gov.bc.ca?"><img src="https://user-images.githubusercontent.com/87393930/133690650-b706e658-27bf-4066-92ba-3a7d8a4593ef.png"/></a>
[2]: https://chat.developer.gov.bc.ca/channel/sso
[3]: https://[mail](mailto:bcgov.sso@gov.bc.ca)[email](mailto:bcgov.sso@gov.bc.ca)

