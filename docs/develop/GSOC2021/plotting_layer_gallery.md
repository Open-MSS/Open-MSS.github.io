---
layout: page
title: GSOC021 Idea
permalink: /develop/GSOC2021/plotting_layer_gallery
exclude: true
---
## Plotting Layer Gallery

- **Project description**

    The MSS software currently offers a wide range of plotting layers that were historically added. Several of these have not been tested for some time and they are difficult to impossible to find and use for new users of the software.
 
    This project has thus three major task to remedy the situation.

    First, the automatically generated test data set needs to be extended such that all available layers can be tested in an automated fashion. 

    Second, the documentation shall be extended such that all plotting layers are documented with an example plot and a usage example (similar to https://matplotlib.org/gallery/index.html). The gallery must be generated automatically such that it is easy to update after adding new plots.

    Third, the plotting classes need to be moved from their current position in the core of MSS to the sample code section in the documentation.


-   **Skills**: Python, Git, ReST

-   **Difficulty level**: Easy

-   **Related Readings/Links**:
     - https://github.com/Open-MSS/MSS/issues/521/add-a-gallery-for-available-layers
     - https://github.com/Open-MSS/MSS/issues/290/remove-class-instantiation-for-hv
     - https://matplotlib.org/gallery/index.html
     - https://www.sphinx-doc.org/en/2.0/usage/restructuredtext/basics.html


-   **Potential mentors**:
     j.ungermann@fz-juelich.de, c.rolf@fz-juelich.de
     