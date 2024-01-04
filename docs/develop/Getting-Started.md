---
layout: page
title: FAQ
permalink: /develop/FAQ
exclude: true
---

## FAQ How To Start

-   Where is the link to a setup guide for new developers?

    You do [setup your environment](/develop/New_Developer).

    Further [Informations](https://mss.readthedocs.io/en/stable/development.html) in our RTFD document.


-   Are there any unusual libraries/applications that need to be
    installed first?

    We are based on [miniforge](https://github.com/conda-forge/miniforge#download)  and [conda-forge](https://conda-forge.org/). 
    All development is done with python 3.

    On linux install `xvfb` and the conda package `pyvirtualdisplay`. This is used to run tests on a virtual display.  


-   How do I have to setup my environment?
      
    Dependent on the IDE there are differences, we try to describe this for anycase.
 
      * Verify by `pytest` in your MSS directory that tests are executed
      * `python workspace/MSS/mslib/mswms/demodata.py -h` (see output on screen)
      * `python workspace/MSS/mslib/mswms/mswms.py -h`
      * `python workspace/MSS/mslib/msui/msui.py -h`
      * `python workspace/MSS/mslib/mscolab/server.py -h`
    

-   What type of source control do you use? 
    * We use git on github
       <https://github.com/Open-MSS/MSS>
    * Git handbook:
       <https://guides.github.com/introduction/git-handbook/>
    * GitHub Guides
       <https://guides.github.com/>
    * MSS Development Guidelines
       <https://mss.readthedocs.io/en/stable/development.html>

    
-   Which branch have I to use?

    We have two branches in the project. 

      * stable is meant for bugfixes only of the current major release.
      * develop is for all kind of development. This is the branch which is used for new features and API changes. develop should always be in a functional state. If you work on something you make a new branch based on develop in your repository. Of course if you do a bug fix for a stable release this has to be done in a branch based of stable. In case of doubt ask one of the mentors.

    
-   What's the process for submitting your first bug fix?

    We like to have a fork of the project, creating a branch based on the develop/stable branch, 
    claiming an issue, working on that issue, talking about that, sending a pull request


-   Where should students look to find easy issues to try out?

    look for ["Good First Issue"](https://github.com/Open-MSS/MSS/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22) labeled Issues 
