# Installation and instructions

You can use this file to provide useful links on installation or other background useful for OMERO here.

<br /><br />

For **linux (Ubuntu) installation instructions** please see below.
First, here are some resources useful for newbies to OMERO: 

## Useful resources
1) The [first talk is from Tom Boissonnet](https://www.youtube.com/watch?v=BNZKMiuK7kg&t=306s) and listed first as he gave it directly after our Hackathon on December, 1st, 2023.   
(Suggestion: start below and come back to this nice talk thereafter. However, in this video, there is a nice introduction by Christian Schmidt in the beginning highlighting available teaching material listed below.)

2) The second link is a [publication on OMERO traininig material](https://zenodo.org/records/8323588) pointed to in the video above.
   
3) Number three is an extensive set of [introductory videos to OMERO](https://www.youtube.com/playlist?list=PL2k-L-zWPoR7SHjG1HhDIwLZj0MB_stlU) also highlighted in the introduction of Christian Schmidt.

Likely there is way more material matching to the different needs of users which can not all be covered here. Appologies for the non-OMERO users that this sections is only added after the Hackathon by a person coming from the ARC side of the OMERO-ARCiversum. Therefore, please feel free to add more which is valuable for newbies to OMERO :smile:

<br/>

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

<br/>

## Server during Hackathon
Access to the OMERO Test server at University of Cologne was provided during the event
