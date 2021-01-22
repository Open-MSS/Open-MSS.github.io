---
layout: page
title: New Developer
permalink: /develop/Newby
exclude: true
---


## Install distributed version by conda

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
    (mssdev)$ mamba install mss --only-deps

    
## Create a fork

You create below your github account a fork of [https://github.com/Open-MSS/MSS](https://github.com/Open-MSS/MSS)


## Development with your fork

Clone your fork to your system. Usualy you create branches for your own work and send pull requests for merging to the master repository.

Afterwards set the PYTHONPATH env variable to the path of the MSS source directory.


As developer you will have newer sources than the released version. 
That is the reason why we only use the dependent packages from the installed software.



## Install further development packages

For testing and building docs we provide a development requirements.
Dependent on development state there may be other requirements files available.

    (mssdev)$ mamba install --file MSS/requirements.d/development.txt
