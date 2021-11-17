---
layout: page
title: GSOC021 Idea
permalink: /develop/GSOC/modernize_fs_filepicker
exclude: true
---


# Modernize fs_filepicker

-   **Project description**:
   The fs_filepicker is a GUI which we use when we select in the mss_settings.json a configuration option `{ "filepicker_default": "fs" }`
   Currently the fs_filepicker implements only a basic set of navigation elements for selecting a file and returns the fs url for accessing it.
In the future we want to have it in a modern look and feel. 
It should also be able to use [Non - Essential Methods of Pyfilesystem](https://docs.pyfilesystem.org/en/latest/implementers.html#non-essential-methods).
Because of the common API of all Pyfilesystem Modules also a directory view can be implemented as tree where folders or files can point to different storages. Tests should cover new source lines.

-   **Skills**: Python, QT, UI programming, Git, pytest

-   **Difficulty level**: Medium

-   **Related Readings/Links**:
    -   https://docs.pyfilesystem.org/en/latest/implementers.html 
    -   https://github.com/Open-MSS/fs_filepicker
 
-   **Potential mentors**:
    rb.proj@gmail.com, m.baer@fz-juelich.de