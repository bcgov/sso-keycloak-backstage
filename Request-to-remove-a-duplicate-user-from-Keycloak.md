## Step 0
**Are you the Keycloak Realm Admin?**

Not sure --> log in to the [Keycloak Custom Realm Registry](https://realm-registry.apps.silver.devops.gov.bc.ca/) and if you see your realm, go to STEP 1. If you don't see it, ask the product owner to submit this request or go to STEP 2

Yes--> go to STEP 1

No --> you will need to ask one of the admin user in your realm to make this request instead.


## STEP 1
Log in to our [Keycloak Custom Realm Registry](https://realm-registry.apps.silver.devops.gov.bc.ca/) and select the DUPLICATE USER tab
- Type the IDIR of the user who is having issue with the account. See the message per environment for the specified user
- If you see the button to delete --> this will remove the duplicate account. Note you will only be able to delete the user if the user is not associated with other products realms
- If you still have issues --> go to STEP 2


## STEP 2
A.  Provide some background on the user account issue in a discussion with us either on [rocketchat](https://chat.developer.gov.bc.ca/channel/sso) or [github discussions](https://github.com/bcgov/sso-keycloak/discussions/new?category=delete-duplicate-user-from-custom-realm). Please include
- What is the issue with the user account?
- What result of debugging have you obtained that lead you to request an account removal?

Note: Deleting the user account from Keycloak will also remove records with any other application using Keycloak that the user has logged into. So before proceeding with this request, make sure the user is aware of the consequences!

* Confirmation that user is ready to have the account removed from Keycloak
* Username to be removed: 
* Realm ID where user is having problem login: 
* Environment in which you are facing issue: 
