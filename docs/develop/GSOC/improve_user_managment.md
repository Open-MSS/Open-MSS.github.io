---
layout: page
title: GSOC Idea
permalink: /develop/GSOC/improve_user_managment
exclude: true
---

# Improve User Managment

- **Project description**:
    Improve the existing MSColab Usermanagment on server and client.
    We use a role concept for the right managment.
    On server site the options what a role can do should become configurable.
          
    Currently any user of the MSColab Server can be added with a role to 
    each operation. 
    We can manage by the manage user interface which operations
    have which users in which role. 
    We use a category for filtering operations
    On server site we can interit users
    and theire roles from a group operation based on a category defined by the client. 
    This is not as comfortable as possible.
    
    We need an hierarchical structure based on the current category. 
    Instead of using it as attribute it should become a root element for its related operations.
    The new category root element needs members by roles. 
    These users with their roles are inherited to all operations 
    under this new category grouping element.
        
    Also creator should become renamed to owner, and there should be more than one user able
    to get this role, similiar to github/gitlab
    
    The admin ui interface needs to become adopted and the main UI view could get a tree like structure.    
    
    
- **Duration**: 175h - 350h

- **Skills**: Python, Qt, Git, experience with usermanagment (discord, github, gitlab), AI-Assistant

- **Difficulty level**: Medium

- **Related Readings/Links**:
  - https://mss.readthedocs.io/en/stable/mscolab.html#user-groups-for-operations
  - https://mss.readthedocs.io/en/stable/tutorials/tutorial_mscolab.html

- **Potential mentors**:
    rb.proj@gmail.com, j.ungermann@fz-juelich.de