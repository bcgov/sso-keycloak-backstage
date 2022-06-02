# Draft June 2 1045am

### Please reach out to the Pathfinder SSO team if you would like to configure any of the following "advanced" settings

**Access Token Lifespan** - This setting is for the max time before an access token is expired. TH value is recommended to be short relative to the SSO timeout
**Client Session Idle** - this setting is the time a client session is allowed to be idle before it expires. Tokens are invalidated when a client session is expired. If not set it uses the standard SSO session idle value.
**Client Session Max** - this setting is the max time for a client session before it expires. Tokens are invalidated when a client session is expired. If not set it uses the standard SSO session max value.
**Client Offline Session Idle** - this setting is the time that client offline session is allowed to be idle before it expires. Offline tokens are invalidated when a client offline session is expired. If not set it uses the offline session idle value
**Client Offline Session Max** - this setting is the max time before a client offline session is expired. Offline tokens are invalidate when a client offline session is expired. If not set, it uses the offline session max value.


More information can be found [here](https://access.redhat.com/documentation/en-us/red_hat_single_sign-on/7.5/html/server_administration_guide/managing_user_sessions#timeouts)