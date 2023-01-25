---
layout: page 
title: GSOC Idea
permalink: /develop/GSOC/saml_for_mscolab
exclude: true
---
## mscolab: Implement a SAML 2.0 service provider (SP) into mscolab

* **Project description**:

  MSS has a collaboration server. For using this server we can create local users.
  We want to use existing identity providers by SAML 2.0.
  The project needs to implement a service provider (SP) on the server site into the existing
  WSGI application and an authentification into the QT client application. On the QT client a login 
  will trigger a browser for the login process. By exchanging an one time token the QT client user can 
  afterwards authenticate.
  For testing a local identity provider (IdP) gets configured and a few tests become added.

* **Duration**: 175h - 350h
* **Skills**: Python, SAML2.0, QT, UI programming, Git
* **Difficulty level**: Medium
* **Related Readings/Links**:
  * https://kushaldas.in/learningsaml/chapter_1.html
  * https://idpy.org/
  * https://mss.readthedocs.io/en/stable/mscolab.html
* **Potential mentors**: rb.proj@gmail.com, j.ungermann@fz-juelich.de
