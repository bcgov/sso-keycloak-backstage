You've asked and we've listened, our latest **MVP** has the ability for you to create roles for your SSO integration.

[View a quick video of how to create Roles](https://user-images.githubusercontent.com/56739669/165629842-7f303725-fd0a-45bf-ab79-3751dbd1ca8a.mp4), or continue reading the instructions below.

### How to create a Role:
1. First, create your integration
1. Once your integration status becomes “Completed”, you can “Create a New Role” for each of your environments, under Role Management
1. Next, you can add users to your various roles, under Assign Users to Roles
1. Finally, configure your app to make use of these roles that are passed via the access token/payload

### Once you have your **JSON** Details and created a **Role**
1. Once your integration is in "completed" status, you will have your json details AND you have created at least one Role
1. Make sure you assign atleast one person to this role under the "Assign Users to Role" section
1. Log in to your Application
1. Look for the the Role you created in the client_role attribute  <img src="https://user-images.githubusercontent.com/56739669/166322299-9791a90f-5502-4273-b1b2-a1eecfd9bcbb.png" width="100" height="100">
1. View this [video at 2:10](https://user-images.githubusercontent.com/56739669/165629842-7f303725-fd0a-45bf-ab79-3751dbd1ca8a.mp4)


### A couple of notes:
1. A Role can **only** be created once the integration status is “completed"
1. You have the ability create different roles for each of the different environment(s) in your integration
1. When you select a role, the right hand side will show users assigned to that role
1. By deleting a role, you are also removing the role from the users assigned to the role....it’s on our backlog to allow to delete one user at a time
1. Any Team Members within your integration can create OR delete roles
1. Any Team Members within your integration can see all users assigned to role

