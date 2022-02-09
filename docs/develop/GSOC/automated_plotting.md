---
layout: page
title: GSOC Idea 
permalink: /develop/GSOC/automated_plotting
exclude: true
---
## Advanced CLI Plotting

* **Project description**: 
  The MSS UI tool is currently designed for interactive use and showing of layers in a UI.
  For post-campaign analysis, retrieving a standardized set of layers for hundreds of time-steps is
  desired, which cannot be accomplished in an efficient manner using the current UI. 
  In this project, a prototype CLI tool for downloading images in an automated fashion shall be extended,
  tested and documented and enhanced by a GUI to configure the set of layers and time-steps to be downloaded. 
  If feasible, the tool shall be integrated into the standard MSS UI.
  Another option could be to describe an API to be used in a notebook in jupyterlab.
* **Duration**: 350h
* **Skills**: Python Git, OGC WMS Standard
* **Difficulty level**: Medium
* **Related Readings/Links**:
  * <https://mss.readthedocs.io/en/stable/usage.html?highlight=retriever#automation-using-the-wms-api>
  * https://github.com/Open-MSS/MSS/issues/514
* **Potential mentors**: rb.proj@gmail.com, j.ungermann@fz-juelich.de, c.rolf@fz-juelich.de