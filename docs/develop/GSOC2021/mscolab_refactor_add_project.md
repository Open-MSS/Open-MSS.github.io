---
layout: page
title: GSOC021 Idea
permalink: /develop/GSOC2021/refactor_add_project
exclude: true
---
## mscolab refactor add project
-   **Project description**:
    Currently we have per flightpath a project. We want to have the ability to have many flight paths below a project.
    In short words: 
    - add project will become the master key (namespace, with a prefix) and could have several flight paths. This enables to have a separation of project users on the server site. So we have only projects in a list and belonging flight paths in an other list. Each flightpath can have something like labels or tags and can be sorted in the UI.
    - we will need a project description, project delete, project rename, project export, project import
        - project (export/import) will need filters, e.g. with users, with flightpath 
        - on flight path creation we need to distinguish to use for the chat the project namespace or a new flightpath related namespace
     

-   **Skills**: Python, QT, socketIO, UI programming, Git

-   **Difficulty level**: Medium

-   **Related Readings/Links**:
    -  https://mss.readthedocs.io/en/stable/mscolab.html
 
-   **Potential mentors**:
    rb.proj@gmail.com, j.ungermann@fz-juelich.de, tanish1908@gmail.com
