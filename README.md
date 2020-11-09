
# Participative Fabrication


This project explores how the use of mobile AR technologies allows users to collaboratively build geometrically complex structures solely from instructions via a mobile interface.

![Participative_Fabrication](/docs/images/participative_building.jpg)


## Requirements

* Minimum OS: **Windows 10 Pro** or **Mac OS Sierra 10.12**
* [Rhinoceros 3D 6.0](https://www.rhino3d.com/)
* [Anaconda Python Distribution](https://www.anaconda.com/download/): 3.x
* Git: [official command-line client](https://git-scm.com/) and visual GUI (e.g. [Github Desktop](https://desktop.github.com/))
* [VS Code](https://code.visualstudio.com/) with the following `Extensions`:
  * `Python` (official extension)



## Getting started

### Compas Installation 
(via your Anaconda Terminal)
    
    (base)  conda config --add channels conda-forge
    (base)  conda create -n your_env_name python=3.8 compas_fab=0.13 --yes
    (base)  conda activate your_env_name
    (your_env_name) python -m compas_rhino.install -v 6.0 -p compas compas_ghpython compas_rhino
    
### Verify Installation

    (your_env_name) pip show compas_fab
    Name: compas-fab
    Version: 0.13.1
    Summary: Robotic fabrication package for the COMPAS Framework
    ...


## Installation and Dependencies - Geometry and Fabrication




Credits
-------------

[@augmentedfabricationlab](https://github.com/augmentedfabricationlab)
