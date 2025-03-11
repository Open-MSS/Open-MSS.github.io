---
layout: page
title: Install
permalink: /install/
---


![image](https://img.shields.io/badge/Install%20with-conda-green.svg?style=flat-square)


## Install by pixi


The Mission Support System (MSS) including a Web Map Service (MSWMS), a Collaboration Server (MSColab)
and a Graphical User Interface (MSUI) is available as a [conda-forge](https://anaconda.org/conda-forge/mss) package.

This channel conda-forge has builds for linux-64, osx-64, win-64, osx-arm64

The conda-forge [github organization](https://conda-forge.github.io/) uses various automated
continuous integration build processes.

In 2024, the workflow that has packages co-installed from Anaconda's channel and conda-forge is no longer supported.
We recommend since version 10.0.0 of MSS to use [pixi](https://pixi.sh/latest/) for an installation.
Get **pixi** from https://pixi.sh/latest/ for your operation system.

You can now decide if you want to install **mss** as global or a project.

### Global Installation

You can install **mss** globally without defining a project first.
This method is practical when you are interested in starting the client and don't need server configurations.

```sh
pixi global install mss
```

#### Usage

```sh
msui
mswms -h
mscolab -h
mssautoplot -h
```

#### Updating

```sh
pixi global update mss
```

### Project Installation

Initialize a new project and navigate to the project directory:

```sh
pixi init MSS
cd MSS
```

Use the shell command to activate the environment and start a new shell in there.

```sh
pixi shell
```

Add the **mss** dependencies from conda-forge.

```sh
(MSS) pixi add mss
```

#### Usage

Always, when you want to start **mss** programs after its installation,
you have to activate the environment by `pixi shell` in the project dir.
On the very first start of **msui**, it takes a bit longer because it setup fonts.

```sh
cd MSS
pixi shell
```

```sh
(MSS) msui
(MSS) mswms -h
(MSS) mscolab -h
(MSS) mssautoplot -h
```

#### Upgrading

```sh
cd MSS
pixi shell
(MSS) pixi upgrade mss
```


## Usage

We describe the global installation.

### GUI
To start the MSS UI you have to use a terminal.

```sh
$ msui
```

> ![image](/assets/msui.png)

The configuration is described in the section 
[mss-configuration](https://mss.readthedocs.io/en/stable/usage.html#mss-configuration) 

### mswms server
To try out the setup you can use demo data. Read about a [server based installation](https://mss.readthedocs.io/en/stable/deployment.html). 

```sh
    $ mswms_demodata --seed
    $ mswms
```

This data is then available on localhost:8081.
The capabilities can be read on a [web browser](http://localhost:8081/?service=WMS&request=GetCapabilities&version=1.1.1) too. 



### mscolab server
To tryout the setup you can use demo data. Read about a [server based installation](https://mss.readthedocs.io/en/stable/mscolab.html).

```sh
    $ mscolab db --seed
    $ mscolab start
```

The service is than availale on localhost:8083 and can be verified by the [server status](http://127.0.0.1:8083/status) 

## Further information about installation options
Please read details on <http://mss.rtfd.io>
