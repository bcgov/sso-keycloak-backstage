
You've asked and we've listened, our latest **MVP** has the ability for you to create roles for your SSO integration.

[View a quick video of how to create Roles](https://user-images.githubusercontent.com/56739669/167518486-89f03e3c-f7e4-4788-89d8-25729e107406.mp4), or continue reading the instructions below.

### How to create a Role:
1. First, create your integration
1. Once your integration status becomes “Completed”, you can “Create a New Role” for each of your environments, under Role Management
1. Next, you can add users to your various roles, under Assign Users to Roles
1. Finally, configure your app to make use of these roles that are passed via the access token/payload

### Once you have your **JSON** Details and created a **Role**
1. Once your integration is in "completed" status, you will have your json details AND you have created at least one Role
1. Make sure you assign at least one person to this role under the "Assign Users to Role" section
1. Log in to your Application
1. Look for the the Role you created in the client_roles attribute  View this [video at 2:00](https://user-images.githubusercontent.com/56739669/167518486-89f03e3c-f7e4-4788-89d8-25729e107406.mp4)


### A couple of notes:
1. A Role can **only** be created once the integration status is “completed"
1. You have the ability to create different roles for each of the different environment(s) in your integration
1. When you select a role, the right hand side will show users assigned to that role
1. By deleting a role, you are also removing the role from the users assigned to the role....it’s on our backlog to allow to delete one user at a time
1. Any Team Member within your integration can create OR delete roles * 
1. Any Team Member within your integration can see all users assigned to role * 

( * ) we've got it in our backlog to configure team admins to handle role management( create/delete roles) and team members to handle user assignment (add/remove users to roles)


## Service Account Role Management
TBD
