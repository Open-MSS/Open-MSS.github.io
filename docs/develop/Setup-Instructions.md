---
layout: page
title: Setup Instructions
permalink: /develop/Setup-Instructions
exclude: true
---

## Setup for development

Pixi is a package management tool for developers. It allows the developer to install libraries and
applications in a reproducible way. Use pixi cross-platform, on Windows, Mac and Linux.

Install pixi on your system.

[Pixi](https://pixi.sh) provides the minimal installers
specific to conda-forge. conda-forge is the default channel configured.

MSS is available as a package on the channel conda-forge.

[conda-forge/mss](https://anaconda.org/conda-forge/mss)

The conda-forge channel has builds for osx-64, osx-arm64, linux-64 and win-64.


#### Setup an environment for development

The dependencies necessary to get a working development environment for MSS are specified in pixi.toml and pixi.lock inside the repository.
This means you can get a shell with all required packages installed using

```sh
    pixi shell -e dev
```

Afterwards, a call to e.g.

```sh
    msui
```

will run the development version of msui.

You can also use pixi's "run" subcommand to directly run a command in the development environment, like so::

```sh
    pixi run -e dev msui
```


## Running The Application

MSS has 3 main components. These are MSUI (GUI), MSWMS (web map server) and MSCOLAB (collaboration server). You can run all 3 components individually on your system. 
(Before running any of the commands make sure you have activated your environment.)

You need to first add the mss folder where additional configurations can become provided.
There the mswms_demodata adds the mswms demo server configuration. 

```sh
    $ cd MSS
    $ pixi shell -e dev
    $ (MSS) export PYTHONPATH=$HOME/mss"
```

To start the MSS PyQT application:
```sh
    (MSS) $ msui
```
When running MSWMS for the first time. Use the following command to create some dummy data:
```sh
    (MSS) $ mswms_demodata --seed
```
To start MSWMS:
```sh
    (MSS) $ mswms
```
When running MSCOLAB for the first time you need to initialize your database (SQLite by default):

```sh
    (MSS) $ mscolab db --init
```
If you want to seed your MSCOLAB database you can run:

```sh
    (MSS) $ mscolab db --seed
```

To start MSCOLAB server:

```sh
    (MSS) $ mscolab start
```
## Running Tests

To run the tests:

```sh
    (MSS) $ pytest --cov mslib
```
