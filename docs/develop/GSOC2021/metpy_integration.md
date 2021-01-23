---
layout: page
title: GSOC021 Idea
permalink: /develop/GSOC2021/metpy_integration
exclude: true
---

## metpy Integration
- **Project description**:

    The MSS application is currently only barely knowledgeable about what type of data it is plotting. Different models store data such as pressure in different units and the visualisation may require even different units.

    Currently, MSS expects the data to be delivered in the "expected" units, which vary from plot to plot. Using the metpy package and the contained unit-conversion routines, this can be fully automated.

    This project shall include the metpy package to that purpose. The plotting framework shall be adapted to include the units and automatically convert these. Having metpy available, one can also discard several functions calculating meteorogical quantities by the ones contained in metpy. The unit tests need to be updated and the existing server infrastructure shall be updated to the new scheme as well.

-    **Skills**: Python, Git, pytest

-    **Difficulty level**: Easy

-    **Related Readings/Links**:

        https://unidata.github.io/MetPy/latest/index.html


-    **Potential mentors**:
    rb.proj@gmail.com, j.ungermann@fz-juelich.de
    