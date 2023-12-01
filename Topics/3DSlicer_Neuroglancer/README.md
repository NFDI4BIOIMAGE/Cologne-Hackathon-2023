# 3D Slicer / Neuroglancer

Worked on by Julia Thönnißen and Torsten Stöter 


## Introduction / Summary

* There is a very simple 3D volume viewer FPBioimage for OMERO https://omero-guides.readthedocs.io/en/latest/fpbioimage/docs/fpbioimage.html
* Can we have better 3D volume visualization accessible from OMERO?

* 3D Slicer integration with OMERO is an external project funded by UoC
** generally more powerful and better volume visualization
** bringing slicer to the web is more tricky
https://discourse.slicer.org/t/how-to-run-slicer-on-the-cloud-and-access-in-a-web-browser/16401
https://discourse.slicer.org/t/run-slicer-in-your-web-browser-as-a-jupyter-notebook-or-as-a-full-application/11569
https://mybinder.org/v2/gh/Slicer/SlicerNotebooks/master?filepath=SlicerWeb.ipynb

* Neuroglancer on the other hand is already a web based visualization tool for very large volume data
* Before and at the Hackathon we looked at bringing images from OMERO in zarr format to Neuroglancer for visualization
* This seemed simpler and doable within a few days of a Hackathon

* Prerequisites: Current Debian machine (11 or 12) with Git, Python, Docker installed
* To avoid issued with CORS and HTTP/HTTPS everything is to run on local machine


## Installing and configuring OMERO

* `git clone https://github.com/ome/docker-example-omero`
* follow instructions in README

```bash
cd docker-example-omero/
docker compose pull
docker compose up -d
docker compose logs -f
```

* Testing via login to `http://localhost:4080` using credentials `root` / `omero`

* Upload some sample images to OMERO via e.g. Insight
** 8 bit channels worked well
** 16 bit signed channels did not work out of the box
** the rendering shader in Neuroglancer will need adaption for this
* Install omero-web-zarr inside with omero-web Docker container, following instruction at https://pypi.org/project/omero-web-zarr/

```bash
docker exec -u 0 -it <omero-web container id> bash
source /opt/omero/web/venv3/bin/activate
pip install omero-web-zarr
```

* Commit changes to Docker image and omero-web to new version in `docker-compose.yml`
* Make images in OMERO publically accessible, so that login on Neuroglancer site is not necessary to fetch the images
* Also allow for CORS (Cross Origin Resource Sharing), so that accessing another website from the current one is not blocked
* Based on https://docs.openmicroscopy.org/omero/5.4.0/sysadmins/public.html add the following lines in `docker-compose.yml` under omero-web ENVIRONMENT

```yaml
CONFIG_omero_web_public_enabled: true
CONFIG_omero_web_public_user: user-1
CONFIG_omero_web_public_password: 'ome'
CONFIG_omero_web_public_url__filter: '/*'
CONFIG_omero_web_apps: '["omero_figure", "omero_iviewer", "omero_mapr", "omero_parade", "omero_web_zarr", "corsheaders"]'
CONFIG_omero_web_middleware: '[{"index": 1, "class": "django.middleware.common.BrokenLinkEmailsMiddleware"}, {"index": 2, "class": "django.middleware.common.CommonMiddleware"}, {"index": 3, "class": "django.contrib.sessions.middleware.SessionMiddleware"}, {"index": 4, "class": "django.middleware.csrf.CsrfViewMiddleware"}, {"index": 5, "class": "django.contrib.messages.middleware.MessageMiddleware"}, {"index": 6, "class": "django.middleware.clickjacking.XFrameOptionsMiddleware"}, {"index": 0, "class": "whitenoise.middleware.WhiteNoiseMiddleware"}, {"index": 0.5, "class": "corsheaders.middleware.CorsMiddleware"}, {"index": 10, "class": "corsheaders.middleware.CorsPostCsrfMiddleware"}]'
CONFIG_omero_web_cors__origin__allow__all: true
```

* OMERO web now exports an image [ID] in zarr publically at the following URL:
`http://localhost:4080/zarr/v0.4/image/[ID].zarr`


## Installing Neuroglancer

* The quickest way to install Neuroglancer seems to be as pre-built Python package from https://pypi.org/project/neuroglancer/

```bash
# install
python3 -m venv neuroglancer-env
source neuroglancer-env/bin/activate
pip3 install neuroglancer

# testing it works
git clone https://github.com/google/neuroglancer
cd neuroglancer/python/examples
python -i example.py
```

* For testing run Neuroglancer in the browser from the provided URL printed at the Python prompt
* For our zarr export URL of image ID=63 this script runs the Neuroglancer server (adapted from Neuroglancer tutorial below)

```python
import neuroglancer

ip = 'localhost' #or public IP of the machine for sharable display
port = 9999 #change to an unused port number
neuroglancer.set_server_bind_address(bind_address=ip,bind_port=port)

viewer = neuroglancer.Viewer()

with viewer.txn() as s:
    s.layers['image'] = neuroglancer.ImageLayer(source='zarr://http://localhost:4080/zarr/v0.4/image/63.zarr/')

print(viewer)
```

* Neuroglancer tutorial: https://connectomics.readthedocs.io/en/latest/external/neuroglancer.html


## Results and image of the workflow session

* We sucessfully could connect OMERO with Neuroglancer and show a proof of concept
* Technical challenges were all related to access images in omero from external web
** Login necessary and OMERO cookies not available to Neuroglancer
** Solution was to grant public access to all routes (NOT RECOMMENDED in production!)
** HTTP/HTTPS, when using an online version of Neuroglancer with HTTPS, providing an HTTP URL of your local omero-web installation, this unsafe access is blocked
** Solution was to run OMERO and Neuroglancer both locally and using only HTTP
** CORS needs to be enabled on OMERO site, when running Neuroglancer and OMERO from different web servers
** Solution in future can be to run both behind the same webserver, e.g. an nginx reverse proxy each with their own route
** Another solution would be to build an omero-web plugin for Neuroglancer, possibly right away into omero-web-zarr or as a separate plugin


## [Report](./Report/)

Please note, if you prefer using the GerbiCloud or your file size is beyond the GitHub limit for this repository, your final report can also be placed in this directory: https://cloud.gerbi-gmb.de/s/FAoqDYwKi4MTBcy

[Here](https://docs.google.com/presentation/d/1IdXq3YQe4353zJJnBvxBr7GwvG0_j1lj9sEx0Cbs7Rs/edit?usp=sharing) is the template for the talk.

:warning: This directory might be publicly accessible (read mode) if we set this repository to public and everybody with this link can see the content of this directory.


## Outlook

* Next steps are to get a production ready installation
* Automate starting the Neuroglancer web server for any image ID
* Improve shaders for 16bit and mutli channel images and include sliders (documented in tutorial)
* Add an "Open in Neuroglancer" button or context menu to images in OMERO
* Test the reverse proxy approach, are logins and cookies preserved?
* Compile a separate OMERO plugin for the Neuroglancer integration

