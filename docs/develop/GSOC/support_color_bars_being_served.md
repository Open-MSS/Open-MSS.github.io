---
layout: page 
title: GSOC Idea
permalink: /develop/GSOC/color_bars_served
exclude: true
---
## mswms: Properly implement and support color bars being served separately from the map

- **Project description**:

  The WMS standard supports delivering color bars as separate image. 
  This is supported in a very basic fashion by the MSUI, but not at all by the MSWMS. 
  In particular in combination with multi-layering, the colorbar must be displayed separately to remain 
  usable (currently all our colorbars are displayed at the same location).

This task entails

1. implementing support for this feature in the MSWMS backend
2. properly address "nice" displaying of the colorbar in the frontend for typical use-cases (i.e. less than 3 bars)
3. Revamping the existing plotting layers to use this feature.

- **Duration**: 175h
- **Skills**: Python, QT, UI programming, Git
- **Difficulty level**: Medium
- **Related Readings/Links**:
  - https://github.com/Open-MSS/MSS/issues/1375
  - https://www.ogc.org/standards/wms
- **Potential mentors**: rb.proj@gmail.com, j.ungermann@fz-juelich.de