The SSO CSS API let's you interact with CSS Application in a RESTful way for both user and role management. To get the access to this API, an admin from a team needs to request CSS API Account through CSS Application.

## How to request a CSS API Account:

1. Login to CSS Application and select `My Dashboard` tab
1. Navigate to `My Teams` tab and select a team
1. Select `CSS API Account` tab and click on `+ Request CSS API Account` to request for an API Account
1. The request shall be approved within 20 minutes and you shall be provided with the options to `copy` or `download` your CSS API Account credentials

## How to use CSS API:

1. CSS API is protected by OAuth2 client credentials flow, so a token is mandatory to make requests to CSS API
1. You can acquire a bearer token using your CSS API Account credentials
1. Add this token in the `Authorization` header in the form of `Bearer <access_token>` and make a request to the API
1. The OpenAPI Spec of the CSS API can be accessed at `https://api.loginproxy.gov.bc.ca/openapi/swagger`

## How to delete CSS API Account:

1. Login to CSS Application and select `My Dashboard` tab
1. Navigate to `My Teams` tab and select a team
1. Under `CSS API Account` tab, you can find delete icon to delete your CSS API Account for that team

## FAQs
### How many CSS API Accounts are permitted per team?
- Only one CSS API Account is permitted per team

### Can I use my CSS API Account to manage other team's integrations?
- No, your CSS API Account is used only to manage your team's integrations

### Can I use my CSS API Account to manage all my team's integrations in silver and gold clusters?
- No, your CSS API Account is used only to manage your team's gold integrations

### Do I need to delete CSS API Account before deleting a team?
- When the team is deleted, the associated CSS API Account gets deleted automatically

### Do I need to create an integration before requesting CSS API Account?
- You can request CSS API Account even if there are no integrations associated with your team 