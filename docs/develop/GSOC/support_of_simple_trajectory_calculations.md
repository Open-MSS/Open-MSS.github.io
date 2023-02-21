---
layout: page
title: GSOC Idea
permalink: /develop/GSOC/support_of_simple_trajectory_calculations
exclude: true
---
## Support of simple trajectory calculations

- **Project description**:
For flight planning or analysis after the campaign it is useful to perform simple trajectory calculations. 
The backend will offer the option to calculate trajectories from the waypoints of the flight path to a given time. 
These will be visualized using as a kml overlay feature or a dedicated plugin. 
This feature will greatly simplify the planning of self-match flights and allow better association between 
the visualized maps showing the atmospheric state at certain times with the air actually sampled during the flight. 
Another application of such trajectories is balloon flight planing i.e. calculation and visualization 
of a balloon trajectory/flight path from a selected start location to its estimated landing position 
with a given set of parameters like climbing rate and ceiling altitude.
The MSS server usually has already the data necessary for performing the calculations, but a simple trajectory 
module would need to be implemented/connected. Also, a WMS extension will need to be specified and implemented.

- **Duration**: 350h
- **Skills**: Python, QT, UI programming, Git
- **Difficulty level**: Hard
- **Related Readings/Links**:
    - https://www.msc-ep.uni-bremen.de/services/lectures/practicals/pr_trajectories_2019.pdf
    - https://predict.habhub.org/
- **Potential mentors**:
    j.ungermann@fz-juelich.de, c.rolf@fz-juelich.de
