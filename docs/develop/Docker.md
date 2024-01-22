---
layout: page
title: Try With Docker
permalink: /develop/docker_images
exclude: true
---

For stable and develop branch of MSS we provide docker images on <https://hub.docker.com/u/openmss>


A complete setup of the mswms server with demodata and the mscolab server with an empty database and the
mss ui can be started by a command.


## released version
 runs mswms with demodata, mscolab and the msui

    $ xhost +local:docker
    $ docker run   --net=host -ti --rm -e DISPLAY=$DISPLAY -v /tmp/.X11-unix/:/tmp/.X11-unix openmss/mss MSS

You can afterwards load data from the wms servers into the msui or create an account on the mscolab server in the container.

> ![image](/assets/run_mss_docker.png)


## Running pytest inside the docker container testing-develop
We mount the MSS workdir into the docker container and use an env
var to access the directory for running pytest on that dir.

    ~/workspace/MSS$ docker pull openmss/testing-develop  # get recent version
    ~/workspace/MSS$ docker run -it --mount src=`pwd`,target=`pwd`,type=bind -e MSSDIR=`pwd` openmss/testing-develop  # mount dir into container, create env var MSSDIR with dir
    (base) root@78f42ac9ded7:/# cd $MSSDIR  # change directory to the mounted dir
    (base) root@78f42ac9ded7:/# conda activate mss-develop-env  # activate env
    (mss-develop-env) root@78f42ac9ded7:/# xvfb-run pytest -vv -n 6 --dist loadfile tests  # run pytest







