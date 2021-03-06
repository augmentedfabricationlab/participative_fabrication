
# Participative Fabrication


In this project we will explore how the use of mobile AR technologies allows users to collaboratively build geometrically complex structures solely from instructions via a mobile interface. We will further look into the design of human-machine interfaces and develop interactive and real-time visual building instructions for users to build a larger structure collaboratively. 


<img src="/docs/images/participative_building.jpg" width="500">


## Requirements

* Minimum OS: **Windows 10 Pro** or **Mac OS Sierra 10.12**
* [Rhinoceros 3D 6.0](https://www.rhino3d.com/)
* [Anaconda 3](https://www.anaconda.com/products/individual)
* Git: [official command-line client](https://git-scm.com/) and visual GUI (e.g. [Github Desktop](https://desktop.github.com/))
* [Docker Desktop](https://www.docker.com/products/docker-desktop)
* [VS Code](https://code.visualstudio.com/) with the following `Extensions`:
  * `Python`  
  *Official extension to add support for Python programming, including debugging, auto-complete, formatting, etc.)*
  * `Docker`  
  *Add support for Dockerfile and docker-compose.yml files to VS Code.*



## Getting started

### Compas Installation 
(via your Anaconda Terminal)
    
    (base) conda config --add channels conda-forge

#### Windows
    (base) conda create -n afab20 python=3.8 compas_fab=0.13 --yes
    (base) conda activate afab20

#### Mac
    (base) conda create -n afab20 python=3.8 compas_fab=0.13 python.app --yes
    (base) conda activate afab20

#### Install on Rhino
    (afab20) python -m compas_rhino.install


### Installation of Dependencies

#### Install Assembly Information Model library

    (afab20) conda install git
    (afab20) python -m pip install git+https://github.com/augmentedfabricationlab/assembly_information_model@master#egg=assembly_information_model
    (afab20) python -m compas_rhino.install -p assembly_information_model

#### Installation participative_fabrication:

* Clone the [participative_fabrication](https://github.com/augmentedfabricationlab/participative_fabrication) repository into your project workspace.


### Docker Set-up:

* [Docker Desktop](https://www.docker.com/products/docker-desktop) Docker Toolbox would also work but it's a bit more annoying. After installation on Windows, it is required to enable "Virtualization" on the BIOS of the computer.

* Start the __Docker ROS incon_communication__, by going to __VS code__ and start the docker containers by:
  * __Only once__: If you do this the first time, you have to build the local [Dockerfile](docker\docker-images\Dockerfile) via 
    * right-click `Build` and tag your Docker Image as: augmentedfabricationlab/incon_communication:latest or 
  * __Always__: Run the docker image [`incon_communication/docker-compose.yml`](docker/ros-systems/incon_communication/docker-compose.yml) via 
    * right-click on the file `Compose-up`
* Open the file [rhino/ex3_assembly_load_to_app.ghx](rhino/ex3_assembly_load_to_app.ghx) and __connect to the ROS client__ via the __rosbridge__. You can now communicate with the incon app via Rhino.

## Example files

Various example files are located in the rhino folder.

## Credits

[@augmentedfabricationlab](https://github.com/augmentedfabricationlab)
