---
layout: page
title: GSOC Idea 
permalink: /develop/GSOC/ui_server_improvements 
exclude: true
---
# msui: UI and server improvements

* **Project description**: 
We want some new features in the MSS UI using or mscolab server. For each new or existing feature we also need pytest tests.
  * show development of flightpath versions. Currently a user can only show a older revision 
    when that revision is pushed as top revision. We want to be able to use this by the asynchronously work mode.
  * show more than one flightpath on a view We have campaigns with more than one aircraft. 
    Sometimes for example they should do in different altitudes the same pattern. 
    Therefore we need an option to add another flightpath on a view. 
    Also it should be possible to toggle the active state, so that it is possible to alter data. 
    On toggling a flightpath the datatable gets updated.
  * the server can use categories to filter existing flight pathes.
    After some defined time a flightpath should be moved to inactive state to have the UI showing
    only current flightpathes. There should be an option for the creator to reactivate an 
    inactive flightpath and also to inactivate one.
  * invite link to operations Besides that one creator can add others to an operation, 
    we want an option to get invited. by clicking on an invite link. For an creator we want that
    different links for different roles can be created and inactivation of links should be possible.
  * one server We have currently two servers which can be individual configured. 
    We want one server which can be configured. Configuration can be done by python scripts and 
    additional by yaml files. It should be possible to disable services
* **Duration**: 175h - 350h
* **Skills**: Python, Qt, Git
* **Difficulty level**: Medium - Hard
* **Related Readings/Links**:
* **Potential mentors**: rb.proj@gmail.com, J.Ungermann@fz-juelich.de