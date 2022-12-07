<br>

*BC Services Card provides an Open ID Connect authentication server. Integration to this service is not available in the *standard* realms.*

The IDIM team that manages BCSC integration is responsible for safeguarding the personal information that is available in a login context. They have a business requirement that integrations to BCSC cannot be shared without IDIM approval. The standard realm is a shared environment -- if we enabled a BCSC integration in a standard realm it would be technically available to all the clients that are configured to use that realm, thus breaking the security model.

---------------------------------

### Options for Teams with BCSC Requirements

<details>
<summary><b>Join an Existing Dedicated Realm on the SSO-KEYCLOAK(formerly OCP-SSO) server</b></summary>
<br>

With approval from IDIM, it is possible to join an existing realm that shares the same security context as your application and already has BCSC set up. This generally means that the existing clients are all from the same ministry or sector and have the same requirements for personal information through the login process.

There are very few instances of this pattern on SSO-KEYCLOAK(formerly OCP-SSO) at this time, but it is an option that is possible with the help and approval of IDIM.

Be that as it may, if there is a closely related project in your ministry or sector that you think would be a candidate for sharing a BCSC integration, you may wish to start the conversation with IDIM and see if it makes sense for your situation.
</details>

<details>
<summary><b>Integrate Directly with BCSC</b></summary>
<br>

Since IDIM provides an OIDC service for BCSC, your app can integrate directly with that service instead of brokering through Pathfinder SSO. Their security practices usually require a client per application in any case, so your architecture might not require using Pathfinder SSO as a proxy authentication service anyway. In addition, this pattern removes one possible point of failure from the application architecture.
</details>

<details>
<summary><b>Configure and Manage Your Own Dedicated KeyCloak Server
</b></summary>
<br>


KeyCloak runs on JBoss quite happily in a Docker container with a PostgreSQL backend. If you really need features provided by KeyCloak and you want to integrate with BCSC, it's possible to run your own KeyCloak server and configure your connection to BCSC by setting up your own OIDC IDP.
</details>

<details>
<summary><b>Obtain a Dedicated KeyCloak Realm on the Pathfinder SSO service
</b></summary>
<br>

If the service gets to the point where there are "slots" to create new dedicated realms, a BCSC identity provider can be securely configured within a realm dedicated to your team. For now, we are unable to offer new realms while we work to reduce the number down to a manageable size.
</details>

<details>
<summary><b>Other?
</b></summary>
<br>

Things are always evolving and the BC Government Open Source community is constantly innovating and solving problems together. Don't be afraid to jump into the #SSO RocketChat channel and see what the community recommends if you have an unusual use case or an innovative idea. Thank you for your collaboration!


</details>


<p align="right">
  <img width="400" height="200" src="https://user-images.githubusercontent.com/87393930/133848225-13dfcb95-7a2e-46b4-ace7-edc436473905.png">
</p>

----------------------------