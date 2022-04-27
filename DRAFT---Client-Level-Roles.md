You've asked and we've listened, our latest **MVP** has the ability for you to create roles for your SSO integration.

[View a quick video of how to create Roles](https://user-images.githubusercontent.com/56739669/165629842-7f303725-fd0a-45bf-ab79-3751dbd1ca8a.mp4), or continue reading the instructions below.

### How to create a Role:
1. First, create your integration
1. Once your integration status becomes “Completed”, you can “Create a New Role” for each of your environments, under Role Management
1. Next, you can add users to your various roles, under Assign Users to Roles
1. Finally, configure our app to make use of these roles that are passed via the access token/payload
### A couple of notes:
1. A Role can **only** be created once the integration status is “completed
1. You have the ability create different roles for each of the different environment(s) in your integration
1. A Role list is auto loaded if the environment has more than 20 roles (I’m not sure the user needs to know this?)
1. When you select a role, the right hand side will show users assigned to that role
1. By deleting a role, you are also removing the role from the users assigned to the role....it’s on our backlog to allow to delete one user at a time
1. Any Team Members within your integration can create OR delete roles
1. Any Team Members within your integration can see all users assigned to role

