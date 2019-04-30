# jupyterhub configuration

This repository contains scripts for building and deploying jupyterhub instances in the cloud.
This functionality will be used for giving demonstrations of icepack through the browser, which saves students from having to install firedrake first.


### Building and testing

To build the docker image:

    docker build -t icepack/jhub:latest

To instantiate a container from this image and run it locally, execute the following:

    docker run --interactive --tty --publish 8888:8888 icepack/jhub:latest

Make a note of the token printed out to the terminal; you'll need this to log in to the hub itself.


### Sources

* [Zero to JupyterHub with Kubernetes](https://zero-to-jupyterhub.readthedocs.io/en/latest/) for most of the configuration
* [Extra hacks](https://github.com/dham/jhub-firedrake) around virtual environments and ipykernel for Firedrake
