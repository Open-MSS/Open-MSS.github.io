---
layout: page
title: Setup Instructions
permalink: /develop/Setup-Instructions
exclude: true
---

## Environment Setup

### Install distributed version by mamba

Install miniforge on your system.

[Miniforge](https://github.com/conda-forge/miniforge#download) provides the minimal installers 
for Conda and Mamba specific to conda-forge. The packages of the base are from the conda-forge channel.
conda-forge is the default and only channel configured.

MSS is available as a package on the channel conda-forge.

[conda-forge/mss](https://anaconda.org/conda-forge/mss)

This channel conda-forge has builds for osx-64, linux-64, win-64

You must install mss into a new environment to ensure the most recent
versions for dependencies. :

    $ mamba create -n mssdev mss --only-deps
    $ mamba activate mssdev
    (mssdev) $ 

Afterwards reactivate the environment, this sets all env variables needed.

    (mssdev) $ mamba deactivate
    $ mamba activate mssdev

### Installing development specific packages

Between the released and the develop version we have differences in used packages:

    git diff stable develop -- localbuild/meta.yaml
    
Update accordingly of the output.

For testing and building docs you need to install the these packages by running the following command:

    (mssdev) $ mamba install --file MSS/requirements.d/development.txt

## Running The Application

MSS has 3 main components. These are MSUI (GUI), MSWMS (web map server) and MSCOLAB (collaboration server). You can run all 3 components individually on your system. 
(Before running any of the commands make sure you have activated your environment.)

You need to first add the main mss folder which will be created in your home directory to your python path. Go into the cloned repo and update your python path:

    $ cd MSS
    $ export PYTHONPATH="`pwd`:$HOME/mss"

To start the MSS PyQT application:

    (mssdev) $ python mslib/msui/msui.py

When running MSWMS for the first time. Use the following command to create some dummy data:

    (mssdev) $ python mslib/mswms/demodata.py --seed

To start MSWMS:

    (mssdev) $ python mslib/mswms/mswms.py

When running MSCOLAB for the first time you need to initialize your database (SQLite by default):

    (mssdev) $ python mslib/mscolab/mscolab.py db --init

If you want to seed your MSCOLAB database you can run:

    (mssdev) $ python mslib/mscolab/mscolab.py db --seed

To start MSCOLAB server:

    (mssdev) $ python mslib/mscolab/mscolab.py start

## Running Tests

On linux install the conda package pyvirtualdisplay and xvfb from your linux package manager. This is used to run tests on a virtual display. If you don’t want tests redirected to the xvfb display just setup an environment variable:

    $ export TESTS_VISIBLE=TRUE

To run the tests:

    (mssdev) $ pytest --cov mslib
