---
layout: page
title: Setup Instructions
permalink: /develop/Setup-Instructions
exclude: true
---

## Environment Setup

### Install distributed version by conda

Install Anaconda on your system.

[Anaconda](https://www.continuum.io/why-anaconda) provides an
enterprise-ready data analytics platform that empowers companies to
adopt a modern open data science analytics architecture.

MSS is available as anaconda package on the channel.

[conda-forge/mss](https://anaconda.org/conda-forge/mss)

The conda-forge packages are based on defaults and other conda-forge
packages. This channel conda-forge has builds for osx-64, linux-64,
win-64

### conda-forge channel

Please add the channel conda-forge to your defaults:

    $ conda config --add channels conda-forge
    $ conda config --add channels defaults

The last channel added gets on top of the list. This gives the order:
First search in default packages then in conda-forge.

You must install mss into a new environment to ensure the most recent
versions for dependencies (On the Anaconda Prompt on Windows, you have
to leave out the 'source' here and below). :

    $ conda create -n mssdev python=3 mamba
    $ conda activate mssdev
    (mssdev) $ mamba install mss --only-deps

Afterwards reactivate the environment, this sets all env variables needed.

    (mssdev) $ conda deactivate
    $ conda activate mssdev

### Installing development specific packages

For testing and building docs you need to install the these packages by running the following command:

    (mssdev) $ mamba install --file MSS/requirements.d/development.txt

## Running The Application

MSS has 3 main components. These are MSUI (GUI), MSWMS (web map server) and MSCOLAB (collaboration server). You can run all 3 components individually on your system. (Before running any of the commands make sure you have activated your conda environment.)

You need to first add the main mss folder which will be created in your home directory to your python path. Go into the cloned repo and update your python path:

    $ cd MSS
    $ export PYTHONPATH="`pwd`:$HOME/mss"

To start the MSS PyQT application:

    (mssdev) $ python mslib/msui/mss_pyui.py

When running MSWMS for the first time. Use the following command to create some dummy data:

    (mssdev) $ python mslib/mswms/demodata.py --create

To start MSWMS:

    (mssdev) $ python mslib/mswms/mswms.py

When running MSCOLAB for the first time you need to initialize your database (SQLite by default):

    (mssdev) $ python mslib/mscolab/mscolab db --init

If you want to seed your MSCOLAB database you can run:

    (mssdev) $ python mslib/mscolab/mscolab.py db --seed

To start MSCOLAB server:

    (mssdev) $ python mslib/mscolab/mscolab.py start

## Running Tests

On linux install the conda package pyvirtualdisplay and xvfb from your linux package manager. This is used to run tests on a virtual display. If you don’t want tests redirected to the xvfb display just setup an environment variable:

    $ export TESTS_VISIBLE=TRUE

To run the tests:

    (mssdev) $ pytest --cov mslib
