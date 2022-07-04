# OIDC Primer

## Part 1: https://developer.okta.com/blog/2017/07/25/oidc-primer-part-1
## Part 2
The following has been created based on the structure from https://developer.okta.com/blog/2017/07/25/oidc-primer-part-2

### OIDC in Action – An OpenID Connect Primer, Part 2 of 3
In the [first installment of this OpenID Connect (OIDC) series](https://developer.okta.com/blog/2017/07/25/oidc-primer-part-1), we looked at some OIDC basics, its history, and the various flow types, scopes, and tokens involved. In this post, we’ll dive into the mechanics of OIDC and see the various flows in action.

The token(s) you get back from an OIDC flow and the contents of the /userinfo endpoint are a function of the flow type and scopes requested. 
Your use case will determine which flow to use. Are you building a SPA or mobile app that needs to interact directly with the CSS App Integration (aka OpenID Provider) Do you have middleware, such as Spring Boot or Node.js Express that will interact with the CSS App Integration. Below, we dig into some of the available flows and when it’s appropriate to use them.

**NEED TO CUSTOMIZE**
[Authorization Code Flow](https://developer.okta.com/blog/2017/07/25/oidc-primer-part-2#authorization-code-flow)

The Authorization Code flow is covered in [Section 3.1 of the OIDC spec](http://openid.net/specs/openid-connect-core-1_0.html#CodeFlowAuth). The TL;DR is: a code is returned from the /authorization endpoint which can be exchanged for ID and access tokens using the /token endpoint.

This is a suitable approach when you have a middleware client connected to an CSS App Integration and don’t (necessarily) want tokens to ever come back to an end-user application, such as a browser. It also means the end-user application never needs to know a secret key.

Here’s an example of how this flow gets started using the CSS App:

**INSERT VISUAL 1**


**INSERT TABLE**

#### After you've logged in -- this may need to be customized....

Behind the scenes, a session is established with a fixed username and password. You will be redirected to login and then redirected back to this same page.

On the above screenshot, you see the returned code and original state.

That code can now be exchanged for an id_token and an access_token by the middle tier. This middle tier will validate the state we sent in the authorize request earlier and make a /token request using the Client Secret to mint an access_token and id_token for the user
