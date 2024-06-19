# Python(Django)-Push in Docker and Deploy in Azure cloud
Create a simple website (Django) and Push this Django to Docker .Created a images on Docker. Deploy Containers on Azure , In Azure you have to create a Container registry and container instance. Container instance we can create in Azure portal or Az Cloud Shell (Bash)

1. Download and install Docker and try to do a simple hello world with busybox
https://docs.docker.com/desktop/install/windows-install/
2. Try to create a simple django website via your docker container and se if you can get it working to actually see your webpage locally.
3. Do a dockerfile and run it locally and when you are why not try it in the cloud.
4. Try to deploy a django application connected to Azure SQL using Docker and Azure App service. (Optional but its good practice)

 # Watch this course before doing the labs if this is new info for you:
    https://www.youtube.com/watch?v=pTFZFxd4hOI

# follow this vedio
    https://youtu.be/PaGBm9a3bHw?si=xyE-DXorsr18dIpD

# After creating ACR(Container registry) and you Have to create a ACI(Conatiner instance). If you can go to terminal Vcode and go to terminal Azure Cloud Shell. there you have to write a code like
az container create \
  --resource-group Demoregister \
  --name demoinstance \ # you can you new name here
  --image demoregister01.azurecr.io/project-web:latest \
  --dns-name-label mydockerapp \ # you can give new name here
  --ports 8000 \
  --registry-login-server demoregister01.azurecr.io \
  --registry-username Demoregister01 \
  --registry-password # copy password from Azure cloud paste here
