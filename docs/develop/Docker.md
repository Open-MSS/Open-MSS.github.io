---
layout: page
title: Try With Docker
permalink: /develop/docker_images
exclude: true
---

For stable and develop branch of MSS we provide docker images on <https://hub.docker.com/orgs/openmss/>


A complete setup of the mswms server with demodata and the mscolab server with an empty database and the
mss ui can be started by a command.


## stable
 runs mswms with demodata, mscolab and the msui

    $ xhost +local:docker
    $ docker run   --net=host -ti --rm -e DISPLAY=$DISPLAY -v /tmp/.X11-unix/:/tmp/.X11-unix yourmss/stable MSS



## develop

 runs mswms with demodata, mscolab and the msui

    $ xhost +local:docker
    $ docker run   --net=host -ti --rm -e DISPLAY=$DISPLAY -v /tmp/.X11-unix/:/tmp/.X11-unix yourmss/develop MSS



You can afterwards load data from the both servers into the msui.

> ![image](/assets/run_mss_docker.png)
