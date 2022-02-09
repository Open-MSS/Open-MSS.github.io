---
layout: page
title: GSOC Idea 
permalink: /develop/GSOC/view_restoring 
exclude: true
---

## mscolab: View Layout and Restoring

* **Project description**:

  The PyQT Gui of the MSS client can currently handle different views by one flight path. 
  This means once a new flight path is loaded and activated all views change to this flight path. 
  Such a View configuration consists of many windows with a complex set of configuration options that 
  are tedious to re-create after shutting down the application.
  The mscolab UI should allow for storing and restoring the view configuration of  
  multiple windows for the user for an operation.

  A configuration should been selectable for another flightpath and operation. 
  There should also be a layout option given to any participant of the same flightpath,
  e.g. two topview connected to different wms servers. 
  A creator of an operation should be able to set the layout of all participants.

* **Duration**: 175h
* **Skills**: Python, QT, UI programming, Git
* **Difficulty level**: Medium
* **Related Readings/Links**:
  * Ticket
  * QT Cache
* **Potential mentors**: rb.proj@gmail.com, j.ungermann@fz-juelich.de