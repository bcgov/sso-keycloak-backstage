# Method one docker ( avoid docker desktop)

## Pre-req
1. Either run docker through your linux or wsl (windows subsystem for linux) https://code.visualstudio.com/docs/remote/wsl 
2. test that you can get a hello world or getting started app running in docker https://docs.docker.com/get-started/02_our_app/


side notes:
* running docker may require you to be in admin mode
* localhost/0.0.0. http://localhost:3000/
* WSL & Visual Studio ``` Remote-WSL: New Window```
* docker infor
* docker image ls
* docker container ls
* docker container stop <container name>
* service docker start
* if you get redirect issue, look at the very powerful url via https://www.urldecoder.org/ AND make sure your redirects match
* docker-compose up vs docker-compose down


## urls/steps
1. review the readme https://github.com/bcgov/keycloak-example-apps/blob/dev/README.md
2. clone github repo to your local https://github.com/bcgov/keycloak-example-apps
3.  create CSS Integration OR create a client in your custom keycloak realm !!!make sure  http://localhost:3000  is valid redirect uri!!!

# Edits for Confidential-express
1. need to have the keycloak json file with the **secret**
{
    "confidential-port": 0,
    "auth-server-url": "some text",
    "realm": "some text",
    "ssl-required": "some text",
    "resource": "someteext",
    "credentials": {
      "secret": "some secret"
    }
  }

# Edits for public-fastAPI
0. good candidate to decommission? -- repo was written to give a rough example of code rather than providing a comple app in terms of the time we had
1. make sure the docker-compose file has the right end point 
    GOLD: - WELL_KNOWN_ENDPOINT=https://dev.loginproxy.gov.bc.ca/auth/realms/standard/.well-known/openid-configuration
      SILVER - WELL_KNOWN_ENDPOINT=https://dev.oidc.gov.bc.ca/auth/realms/onestopauth/.well-known/openid-configuration

# Method 2 next js
1. install nextjs so it can run in your ide
* https://nextjs.org/docs/getting-started
* npx create-next-app@latest

2. Use the gihub repo for public-nextjs
Notes: 
a. ensure you have the latest version of node and express pulled in

**
b. modify backend/config.js to use port 3000

c. include the node modules

**
d. npm run dev 

# json installation file screenshots of custom keycloak realm
when you create a client in keycloak, you obtain the json file from the installation tab of client
7.4.9 
![image](https://user-images.githubusercontent.com/56739669/172299300-fbd69c5d-4212-4bf1-a96e-1ba3456fc71b.png)
7.5 
![image](https://user-images.githubusercontent.com/56739669/172299426-08bebea9-f4a1-4bdd-a3c3-d530c663245c.png)

![image](https://user-images.githubusercontent.com/56739669/173156242-d988bfca-5bc7-4342-a6e0-9acc3551fbcb.png)
