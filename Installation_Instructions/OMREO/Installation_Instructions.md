# Installation and instructions

You can use this file to provide useful links on installation or other background useful for OMERO here.

<br /><br />

## OMERO installation in Ubuntu using Docker

<br />

### Install Docker using snap  

<br />

Link : https://snapcraft.io/install/docker/ubuntu  <br /> 

sudo apt update <br />

sudo apt install snapd <br />

sudo snap install docker <br />


<br />

### Install OMERO locally

<br />

git clone https://github.com/ome/docker-example-omero.git  <br />

cd docker-example-omero/    <br />

sudo docker compose pull    <br />

sudo docker compose up -d   <br />

sudo docker compose logs -f  <br />


<br />

### Login to OMERO

<br />

Click on : http://localhost:4080/    <br />

user     : root  <br />
password : omero <br />
