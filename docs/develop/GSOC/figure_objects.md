---
layout: page
title: GSOC Idea
permalink: /develop/GSOC/figure_objects
exclude: true
---

# API to use MSS figure objects in other python modules 

- **Project description**:
    The MSS tool is currently designed for interactive use and having an mssautoplot cli script for post-campaign analysis, retrieving a standardized set of layers for hundreds of time-steps an automated plotting feature was developed. The next step is to create based on the mssautoplot an API to be used in other python modules. 
    This should enable a user to add its own data to our figures used. This is especially interesting for data of the linearview. There a user can overlay on its own measured data. In addition scatter plots shall be enabled.
    The new API may be used in a Jupyter Notebook. This needs also a different solution to create a mssautoplot-json file. 
    
- **Duration**: 175h - 350h
  
- **Skills**: Python, Git, JupyterLab

- **Difficulty level**: Medium

- **Related Readings/Links**:
    - https://mss.readthedocs.io/en/stable/mssautoplot.html
    - https://mss.readthedocs.io/en/stable/tutorial.html

- **Potential mentors**:
    rb.proj@gmail.com, j.ungermann@fz-juelich.de, swsrkty@gmail.com 