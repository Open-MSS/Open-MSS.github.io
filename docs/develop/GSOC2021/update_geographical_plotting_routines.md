---
layout: page
title: GSOC021 Idea
permalink: /develop/GSOC2021/update_geographical_plotting_routines
exclude: true
---
## Update geographical plotting routines


-   **Project description**:

    The MSS project currently relies on the python basemap package for
    supplying non-cylindric projections and plotting of geographical
    features. This package has been deprecated and been supplanted in
    the community by the cartopy package.

    This project deals with first replacing the existing solution with
    the new software package. This requires keeping the performance
    of the plotting at similar levels and updating the documentation
    for installation.

    In a second step the new capabilities of cartopy shall be used
    to support more geographical projections as mandated by the
    Web Mapping Service standard.

    All steps of the project include maintaining or creating the
    necessary unit tests and updating the documentation.
    
    Improve cartopy

-   **Skills**: Python, Git

-   **Difficulty level**: Hard

-   **Related Readings/Links**:
    * https://github.com/Open-MSS/MSS/issues/620
    * https://scitools.org.uk/cartopy/docs/latest/

-   **Potential mentors**:
    rb.proj@gmail.com, j.ungermann@fz-juelich.de, c.rolf@fz-juelich.de