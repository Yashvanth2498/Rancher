# Rancher

#Downloads and runs a script that installs Docker version 18.09 on the host machine. Docker is required to run the Rancher server in a container
curl 
https://releases.rancher.com/install-docker/18.09.sh | sh

#Starts a new Docker container running the latest version of the Rancher server image
sudo docker run -d --restart=unless-stopped -p 80:80 -p 443:443 --privileged rancher/rancher:latest

#For setting up the Rancher password
docker ps
docker logs container-id 2>&1 | grep "Bootstrap Password:"
