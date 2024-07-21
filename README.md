<div style="display:block">
    <div style="width: 20%; display: inline-block; text-align: left;">
        <img src="./Source/mu_sigma_logo.png" style="height:75px; margin-left:0px" />
    </div>
    <div style="width: 59%; display: inline-block">
        <h1  style="text-align: center">Supervised Text Analysis using Transformers in Python</h1>
    </div>
</div>


# Table of Contents

1. [Introduction](#introduction)
1. [Requirements](#requirements)
1. [Installation](#installation-one-time-setup)
1. [Running the brick](#running-the-brick-do-this-everytime-you-run-the-notebook)
1. [Overview](#overview)
1. [Sample Visualization](#sample-visualization)
1. [Contributing](#contributing)
1. [Versioning](#versioning)
1. [Authors](#authors)
1. [Acknowledgments](#acknowledgments)

## Introduction

### Supervised Text Analysis using Transformers in Python

## Requirements

__NOTE: Please ensure you have Administrator access in the machine (Windows/Ubuntu/macOS)__

### The minimum hardware requirements for this project are:

* __RAM__ : Minimum 8 GB (16 GB recommended for optimum performance)
* __Disk space__ : Minimum of 100 MB free space needed to run the program

### The minimum software requirements for this project are:

| Software | How to Check the version available |
|:--------:|:-------------------------:|
| Python 3.9.7 | Open the terminal using `cmd`, type `python -V` and press enter |
| conda | Open the `Anaconda Prompt` terminal, type `conda -V` and press enter |

__NOTE__ : Support for the maintenance of Python 2.7 has officially stop since January, 2020. So it is imperative to use Python 3. If your system doesn't have Python 3, please get in touch with the IT team to install it.

## Installation (one time setup)

### Fast-forward setup:

 __On Windows, you can fast-forward the one time setup by running the following commands in your Anaconda Prompt__:

* Navigate into the project folder using `cd`. For example:

```
cd Documents/Labs/Brick_Supervised_Text_Analysis_using_Transformers_Python_Notebook/
```
* Type the following and press enter:

```
setup.bat
```
* After running this command, you should see the jupyter notebook page on the browser. You can start using the notebook, after changing the kernel to  `class_notebook`. Refer image below:

![Change Kernel](./Source/change_kernel.png)

* Once you are done using the notebook, you can close the browser and anaconda prompt window.
* To use the notebook from now on, simply refer to [Running the brick (do this everytime you run the notebook)](#running-the-brick-do-this-everytime-you-run-the-notebook) section. 

### Regular setup:

__Important: Proceed with the regular setup only if you have not followed the fast-forward setup__

To ensure that the Jupyter notebook for the brick runs smoothly, we will install dependencies (with the required version numbers). We will follow the following steps as __one time setup__:

#### 1. Set up python virtual environment

Proceed by running the following commands in your `Anaconda Prompt` for __Windows__ or `terminal` in __Ubuntu/macOS__:

__1.1 Install [virtualenv](https://virtualenv.pypa.io/en/latest/installation.html) python package__ (Only for Ubuntu/macOS):

```
pip install virtualenv
```

__1.2 Create a virtualenv__

Go to the directory where you downloaded the brick, and just outside the main folder, create a virtualenv called `class_notebook`. Remember this location, as we would need to activate the virtualenv __everytime we run the jupyter notebook__.

> __Windows__:
```
conda create -n <virtual-environment-name> python=3.9.7
```
or
```
conda create -n <virtual-environment-name> python=3.7.6
```

> __Ubunut/macOS__:
```
virtualenv text_analysis
```

__1.3 Activate virtualenv__

> __Windows__:
```
conda activate text_analysis
```

> __Ubuntu__/__macOS__:
```
source text_analysis/bin/activate
```

#### 2. Install dependencies (only for Windows)

```
conda install pip -y
conda config --add channels conda-forge
conda install -c conda-forge pystan -y
conda install -c anaconda ephem -y
```

#### 3. Install `ipykernel` and `jupyter` in the virtual environment

While the virtual environment is active, run these commands
```
pip install ipykernel
python -m ipykernel install --user --name class_notebook
pip install -U jupyter
```

#### 4. Install python packages

Now, we need to install the libraries mentioned in the `requirements.txt` located in the `Source` folder.

> __Windows__
```
cd <path where you downloaded and extracted the brick>
cd Source
pip install -r requirements.txt
```

> __Ubuntu__/__macOS__:
```
cd <path where you downloaded and extracted the brick>
cd Source
pip install -r requirements.txt
```

__NOTE:__ Your system might access Python 3 using `pip` instead of `pip3`. Check and do it accordingly.

#### 4. Enable `jupyter nbextensions` in the virtual environment

To ease the process of installing and enabling the jupyter extensions, we will install a package [jupyter contrib extensions](https://github.com/ipython-contrib/jupyter_contrib_nbextensions).

First, come out of the Source directory using the command `cd ..`.

Install jupyter extensions package

```
pip install jupyter_contrib_nbextensions
jupyter contrib nbextension install --sys-prefix
```

#### 5. Enable the required extensions

Table of contents
```
jupyter nbextension enable toc2/main --sys-prefix
```
Table beautifier
```
jupyter nbextension enable table_beautifier/main --sys-prefix
```
Spellchecker
```
jupyter nbextension enable spellchecker/main --sys-prefix
```

#### 6. Confirm installation of extensions

You can now confirm if all the extensions are enabled using the command
```
jupyter nbextension list
```

__Done__. 

#### 7. Launch the notebook

You may go ahead and run the Jupyter server to start the notebook by running the following command in the `Anaconda Prompt`:
```
jupyter notebook
```

## Running the brick (do this everytime you run the notebook)

### 1. Activate the virtual environment

> __Windows__:
```
conda activate text_analysis
```
> __Ubuntu__/__macOS__:
```
source text_analysis/bin/activate
```

### 2. Run the Jupyter server 

```
jupyter notebook
```

### 3. Set the kernel name to `text_analysis`

Once you see the notebook open in the browser, ensure that it is using the same kernel that was created above, namely ```text_analysis```

![Change Kernel](./Source/change_kernel.png)

Now you can start running the cells in the notebook

## Overview

This notebook covers:

1.  __Introduction to Transformers__:  
    Gives the user an understanding of transformers, its architecture, it's applications and how powerful it is compared to machine and deep learning models

2. __Evolution of Transformers__:
    In this section, user can understand how transformers have evolved over the years 

3. __Quick Peek of the Notebook__:
    This section provides a quick peek into the notebook to help the user understand the different parameters that can be tweaked as per the user’s requirements.
    
4.   __Import libraries__:  
    This section imports all the necessary libraries for data loading and processing as well as visualizations.
    1.  Importing libraries for data loading and processing
    2.  Importing libraries for charts and visualization
    3.  Importing libraries for transformers
    
5. __User Defined Functions__:
    In this section, we are creating some user defined functions that will be used in the notebook.
    We have created several user-defined functions for importing data, taking a quick peek of data, performing missing value analysis, etc.
    
6. __Supervised Text Analysis Use-cases__:  
    In this section, we are adding several use cases related to supervised text analysis
    1. Label Classification
    2. Sentiment Prediction
    3. Named Entity Recognition

7. __Downloads__:
    In this section, user can download any of the implemented models

8. __References__:
    In this section, we are mentioning any refrences that we have used across the brick.


## Sample Visualization


## Contributing

Please refer to [CONTRIBUTE.md](/CONTRIBUTE.md) to get a copy of the project up and running on your local machine.

# Versioning

The following versioning convention is maintained with every release. Given a version number `MAJOR.MINOR.PATCH`, increment the:

* __MAJOR__ version is the last two digits of the year of release
* __MINOR__ version is the last two digits of the month of release
* __PATCH__ version is the n-th release in that month

Every version release must be marked as a [milestone](https://mugitlab.mu-sigma.com/eoc_foundation/supervised-text-analysis-using-transformers/-/milestones) on the Git repository and relevant tags along with [issues](https://mugitlab.mu-sigma.com/eoc_foundation/supervised-text-analysis-using-transformers/-/issues) closed must be added to it.

## Authors
* Mu Sigma

## Acknowledgments

* Building Jupyter Notebook [official website](https://jupyter-notebook-beginner-guide.readthedocs.io/en/latest/)
