# Workshop: Introduction to Open Source Spatial Optimisation @Aalto University, Oct 16, 2023

## Setup

### Step 1: Download the workshop material

If you are comfortable with GitHub and `git`, the command-line program, you can download the workshop materials by cloning my repository:

```sh
git clone https://github.com/qszhao/Aalto2023-spopt.git
cd Aalto2023-spopt
```

If you are not comfortable with GitHub, download the repository to your computer as a zip file from the workshop website. To do this, go to <https://github.com/qszhao/Aalto2023-spopt>, click on the green button labelled "< > Code <i class="fa-regular fa-angle-down"></i>", then click the "<i class="fa-regular fa-file-zipper"></i> Download Zip" option. 

### Step 2: Install the required Python packages

To follow along with the workshop material, it is best if you install Anaconda, a scientific python computing environment. If you do not yet have Anaconda installed, you can install miniconda
(<https://conda.io/miniconda.html>) or the (larger) Anaconda distribution (<https://www.anaconda.com/download/>). 

Option 1: 
Using the `conda` program from your command line or within the anaconda prompt, we recommend using the following terminal commands to set up your environment: 

```bash
# we want to use only the community-distributed packages on "conda-forge" 
conda config --add channels conda-forge
conda config --set channel_priority strict
# and, we want to use the faster implementation of conda, called "mamba"
conda install mamba
# Then, we want to create our actual environment
mamba env create --file environment.yml
# and finally, activate the environment
conda activate spatialopt
```
Option 2:
Alternatively, you can use conda to set up the environment as well.

```bash

#Check current conda channel priority

conda config --get channels

# Switch your default conda channel to conda-forge and set it as the highest priority
# we want to use only the community-distributed packages on "conda-forge" 

conda config --add channels conda-forge 
conda config --set channel_priority strict

#Create new environment

conda create --name spatialopt python=3.11

#Check existing conda environment

conda info --envs

#Make sure that you are going to work in newly created environment

conda activate spatialopt

# Install packages
conda install -c conda-forge jupyterlab
conda install -c conda-forge geopandas
conda install -c conda-forge matplotlib
conda install -c conda-forge shapely
conda install -c conda-forge pyogrio
conda install -c conda-forge libpysal
conda install -c conda-forge spopt
conda install -c conda-forge pulp

#Alternatively run the installation in one line

conda install -c conda-forge jupyterlab geopandas matplotlib shapely pyogrio libpysal spopt pulp  

#Start the  jupyter lab

jupyter lab

```

If you are using the "Anaconda Navigator" interface, you can import the workshop environment using [the steps described in its documentation.](https://docs.anaconda.com/free/navigator/tutorials/manage-environments/#importing-an-environment)

### Step 3: starting Jupyter Lab

To start your analysis environment locally, you first must activate the spatialopt environment if you have not done so: 
```bash
conda activate spatialopt
```

And then, you must start [Juptyer Lab](https://jupyterlab.readthedocs.io/en/stable/), the next-generation user interface for Project Jupyter. The workshop code is implemented in Jupyter Notebooks, a literate and interactive programming environment for scientific computing.

```bash
jupyter lab
```
