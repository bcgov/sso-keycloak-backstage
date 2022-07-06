# Endpoint Definitions

Endpoints
The most important endpoint to understand is the well-known configuration endpoint. It lists endpoints and other configuration options relevant to the OpenID Connect implementation in Keycloak. The endpoint is:

/realms/{realm-name}/.well-known/openid-configuration
To obtain the full URL, add the base URL for Keycloak and replace {realm-name} with the name of your realm. For example:

http://localhost:8080/auth/realms/master/.well-known/openid-configuration

Some RP libraries retrieve all required endpoints from this endpoint, but for others you might need to list the endpoints individually.

Authorization Endpoint
/realms/{realm-name}/protocol/openid-connect/auth
The authorization endpoint performs authentication of the end-user. This is done by redirecting the user agent to this endpoint.

For more details see the [Authorization Endpoint](http://openid.net/specs/openid-connect-core-1_0.html#AuthorizationEndpoint) section in the OpenID Connect specification.

Token Endpoint
/realms/{realm-name}/protocol/openid-connect/token
The token endpoint is used to obtain tokens. Tokens can either be obtained by exchanging an authorization code or by supplying credentials directly depending on what flow is used. The token endpoint is also used to obtain new access tokens when they expire.

For more details see the [Token Endpoint](http://openid.net/specs/openid-connect-core-1_0.html#TokenEndpoint) section in the OpenID Connect specification.

Reference: https://wjw465150.gitbooks.io/keycloak-documentation/content/securing_apps/topics/oidc/oidc-generic.html