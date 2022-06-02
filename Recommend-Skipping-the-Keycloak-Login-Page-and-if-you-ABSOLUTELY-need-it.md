# Draft June 2 1045am

As you've read in our guidance in setting up a keycloak client do's and don'ts [here](https://github.com/bcgov/sso-keycloak/wiki/Using-Your-SSO-Client#dos-and-donts), our recommendation is to skip the [keycloak login page](https://github.com/bcgov/sso-keycloak/wiki/Using-Your-SSO-Client#do-skip-the-keycloak-login-page) ie 
`Do Skip the KeyCloak Login Page
In KeyCloak, if the realm that contains your client has more than one IDP configured, KeyCloak shows a page that prompts the user to select which IDP they want to log in with. Almost all teams have chosen to hide this page from their users by specifying the IDP as a query string parameter in the KeyCloak Authorization URI value behind their login button. The querystring is 'kc_idp_hint'. (The IDPs available will depend on the standard realm in which your client exists.) By specifying the IDP in this way, the user will be redirected directly to the login page for the identity provider and will not see the KeyCloak login choice page at all.

IDIR: kc_idp_hint=idir
BCeID Basic: kc_idp_hint=bceid-basic
BCeID Business: kc_idp_hint=bceid-business
BCeID Basic or Business: kc_idp_hint=bceid-basic-and-business
GitHub: kc_idp_hint=github (Available in DEV and TEST)
`

If you are a client of ours and have an absolute need to have a dedicated set of text for your login page, through [our app](https://bcgov.github.io/sso-requests), you can specify the text under the field setting **Keycloak Login Page Name**

Please reach out to us if you have more questions