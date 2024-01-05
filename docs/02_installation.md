---
layout: page
title: Install
permalink: /install/
---


![image](https://img.shields.io/badge/Install%20with-conda-green.svg?style=flat-square)


## Install distributed version by conda


We are based on [miniforge](https://github.com/conda-forge/miniforge#download)   
miniforge provides the minimal installers for Conda and Mamba specific to conda-forge. The packages of the base are from the conda-forge channel.
conda-forge is the default and only channel configured.
MSS is available as a conda package on the channel.

[conda-forge/mss](https://anaconda.org/conda-forge/mss)

This channel conda-forge has builds for osx-64, linux-64, win-64.

The conda-forge [github organization](https://conda-forge.github.io/)
uses various automated continuous integration build processes.


You must install mss into a new environment to ensure the most recent
versions for dependencies:

    $ mamba create -n mssenv mss
    $ mamba activate mssenv
    (mssenv) $ mss -h

Afterwards reactivate the environment, this sets all env variables needed.

    (mssenv) $ mamba deactivate
    $ mamba activate mssenv

For updating an existing MSS installation to the current version, it is
best to install it into a new environment. If an existing environment
shall be updated, it is important to update all packages in this
environment. 

    $ mamba activate mssenv
    (mssenv) $ mamba update mss
    (mssenv) $ mamba update --all

## Usage
### GUI
To start the MSS UI you can lookup for "mss" on your desktop program manager or use a terminal  

    (mssenv) $ mss

> ![image](/assets/msui.png)

The configuration is described in the section 
[mss-configuration](https://mss.readthedocs.io/en/stable/usage.html#mss-configuration) 

### mswms server
To try out the setup you can use demo data. Read about a [server based installation](https://mss.readthedocs.io/en/stable/deployment.html). 

    (mssenv) $ mswms_demodata --seed
    (mssenv) $ mswms

This data is then available on localhost:8081.
The capabilities can be read on a [web browser](http://localhost:8081/?service=WMS&request=GetCapabilities&version=1.1.1) too. 



### mscolab server
To tryout the setup you can use demo data. Read about a [server based installation](https://mss.readthedocs.io/en/stable/mscolab.html).

    (mssenv) $ mscolab db --init
    (mssenv) $ mscolab db --seed
    (mssenv) $ mscolab start

The service is than availale on localhost:8083 and can be verified by the [server status](http://127.0.0.1:8083/status) 

## Further information about installation options
Please read details on <http://mss.rtfd.io>
