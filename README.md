
# Participative Fabrication


In this project we will explore how the use of mobile AR technologies allows users to collaboratively build geometrically complex structures solely from instructions via a mobile interface. We will further look into the design of human-machine interfaces and develop interactive and real-time visual building instructions for users to build a larger structure collaboratively. 


<img src="/docs/images/participative_building.jpg" width="300">


## Requirements

* Minimum OS: **Windows 10 Pro** or **Mac OS Sierra 10.12**
* [Rhinoceros 3D 6.0](https://www.rhino3d.com/)
* [Anaconda 3](https://www.anaconda.com/products/individual)
* Git: [official command-line client](https://git-scm.com/) and visual GUI (e.g. [Github Desktop](https://desktop.github.com/))
* [VS Code](https://code.visualstudio.com/) with the following `Extensions`:
  * `Python` (official extension)



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

### Install on Rhino

    (afab20) python -m compas_rhino.install

## Installation and Dependencies - Geometry and Fabrication

### Installation participative_fabrication:

* Clone the [participative_fabrication](https://github.com/augmentedfabricationlab/participative_fabrication) repository into your project workspace.

### Installation assembly_information_model:

* Clone the [assembly_information_model](https://github.com/augmentedfabricationlab/assembly_information_model) repository into your project workspace.

* Change to the directory of the repository and use pip install to copy the repository to your Anaconda environment site packages: 

`(afab20) pip install -e your_filepath_to_assembly_information_model`    

* And make the projects accessible from Rhino 

`(afab20) invoke add-to-rhino`

### Setting up Docker for the communication between the incon app and Rhino:

* Start the __Docker ROS incon_communication __, by going to VS code and start the docker containers by:
  * __Only once__: If you do this the first time, you have to build the local [Dockerfile](docker\docker-images\Dockerfile) via 
    * right-click `Build` and tag your Docker Image as: augmentedfabricationlab/incon_communication:latest or 
    * in the Terminal (cd to folder) via<br/> `docker build --rm -f Dockerfile -t augmentedfabricationlab/incon_communication .` 
    * (Building without cache:<br/> `docker build --no-cache --rm -f Dockerfile -t augmentedfabricationlab/incon_communication .`)
  * __Always__: Run the docker image [`incon_communication/docker-compose.yml`](docker/ros-systems/incon_communication/docker-compose.yml) via 
    * right-click on the file `Compose-up` or 
    * type `docker-compose up -d` in the Terminal (cd to folder) to start it.
    * when ending, don't forget to stop the image via `docker-compose down -d`
* Open the file [rhino/ex3_assembly_load_to_app.ghx](rhino/ex3_assembly_load_to_app.ghx) and __connect to the ROS client via the rosbridge__ You can now communicate with the incon app via Rhino.

## Example files

Various example files are located in the rhino folder.

## Credits

[@augmentedfabricationlab](https://github.com/augmentedfabricationlab)
