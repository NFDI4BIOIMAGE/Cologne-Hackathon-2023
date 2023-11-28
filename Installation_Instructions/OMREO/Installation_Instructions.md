# Installation and instructions

You can use this file to provide useful links on installation or other background useful for OMERO here.



## OMERO installation in Ubuntu using Docker


### Install Docker using snap 

Link : https://snapcraft.io/install/docker/ubuntu

sudo apt update
sudo apt install snapd
sudo snap install docker


### Install OMERO locally


git clone https://github.com/ome/docker-example-omero.git
cd docker-example-omero/
sudo docker compose pull
sudo docker compose up -d
sudo docker compose logs -f


Click on : (http://localhost:4080/)
user: root
password : omero
