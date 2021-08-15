# docker-install
if you need help installing docker please see this guide

docker restore installation notes

sudo apt-get install curl  (this is needed to curl and retreive files)
sudo apt-get install net-tools (this will let you run ifconfig to find host/vm ip address)
sudo apt-get install openssh-server (this is so you can ssh into your host/vm)

sudo apt-get update
sudo apt-get upgrade

there is MANY MANY WAYS to install docker personally I use a script that does everything for you. see bellow on how to


lets install docker

get docker
curl -fsSL https://get.docker.com -o get-docker.sh
sh get-docker.sh

add user to docker group
sudo usermod -aG docker ${USER}



now you will want docker compose

install docker compose
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

make docker compose executable
sudo chmod +x /usr/local/bin/docker-compose

reboot host

run command docker ps should return wiht no permission issues

In order to make life in docker land when it comes to editing easier you will want to get yourself a good editor. Personall I use vs studio

now you are ready to go down the docker rabit hole. enjoy
