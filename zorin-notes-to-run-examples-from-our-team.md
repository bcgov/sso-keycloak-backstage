# Method one docker ( avoid docker desktop)

## Pre-req
1. Either run docker through your linux or wsl (windows subsystem for linux) https://code.visualstudio.com/docs/remote/wsl 
2. test that you can get a hello world or getting started app running in docker https://docs.docker.com/get-started/02_our_app/


side notes:
running docker may require you to be in admin mode
localhost/0.0.0. http://localhost:3000/
WSL & Visual Studio ``` Remote-WSL: New Window```
docker infor
docker image ls
docker container ls
docker container stop <container name>


## urls/steps
1. review the readme https://github.com/bcgov/keycloak-example-apps/blob/dev/README.md
2. clone github repo to your local https://github.com/bcgov/keycloak-example-apps
3.  create CSS Integration OR create a client in your custom keycloak realm !!!make sure  http://localhost:3000  is valid redirect uri!!!


# Method 2


go to the nextjs folder
https://nextjs.org/docs/getting-started

npx create-next-app@latest

# json installation file screenshots of custom keycloak realm
when you create a client in keycloak, you obtain the json file from the installation tab of client
7.4.9 
![image](https://user-images.githubusercontent.com/56739669/172299300-fbd69c5d-4212-4bf1-a96e-1ba3456fc71b.png)
7.5 
![image](https://user-images.githubusercontent.com/56739669/172299426-08bebea9-f4a1-4bdd-a3c3-d530c663245c.png)

