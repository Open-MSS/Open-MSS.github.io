---
layout: post
title:  "MSS 9.0.0 All Components of MSS"
date:   2024-05-22 17:10:11 +0100
categories: MSS update release
---

## All Components of MSS

With installing MSS you get all components described in our docs. Everything is included in the package.
https://mss.readthedocs.io/en/stable/components.html
You can setup your own WMS servers and provide your own plotting methods. Also you can setup your own collaboration server. 
And of course you can use our MSUI.



## Using MSUI
Our userinterface has majored and this is a short introduction how you can use it.

> ![image](/assets/msui-9.0.0_after_login.png)
> 
> The left side shows the connection to an mscolab server and the right side how it looks like after a login

The UI can be used with our or others WMS servers

> ![image](/assets/msui-9.0.0_public_eccharts.png)
> 
> Showing a parameter by using the https://confluence.ecmwf.int/display/CKB/WMS+for+CAMS+Global+and+European+air+quality+products

Our WMS server in difference of the common OGC WMS Servers is able to provide data for a side or linear view.
These views are needed for planning athmospheric research aircraft missions.


> ![image](/assets/msui-9.0.0_linear_sideview.png)
>
> Showing a linearview of BrONO2 and a sideview from campaigns 2019 data along a flightpath. 

For more examples please watch some of our tutorial movies on https://mss.readthedocs.io/en/stable/tutorial.html


## Major Contributions: 

* **9.0.0** Nilupul Manodya (@nilupulmanodya ) implemented SAML 2.0 (Security Assertion Markup Language) 
Authentication in Google Summer of Code 2023. MSColab can now be configured with an existing IdP or multiple IdPs.
In this way, a user can authenticate themselves in one system and gain access to another system
by providing proof of authentication. In our documentation in the Components section you find a detailed description.
Matthias Riße (@matrss ) refactored the test suite and optimized and accelerated our CI test runs.
All tests run in parallel now and are not retried upon failure, and most tests are also executed in a randomized order, instilling more confidence in the results.
Quite a bit of duplicated code was unified, mostly using pytest fixtures.
Additionally, CI test runs now also happen on x86_64- and ARM-based macOS.
Jörn Ungermann (@joernu76 ) refactored various parts of MSColab for faster processing with fewer requests.
Reimar Bauer (@ReimarBauer ) refactored the tutorials and the documentation shows now mp4 files embedded in html5.

* **8.0.0** Sreelakshmi Jayarajan (@swsrkty) created a new CLI module for automated plotting by an user
and refactored existing plotting and QT based classes modules in Google Summer of Code 2022
These classes can be used for plotting purposes without
involving QT-based GUI and Interactive functionalities.
Users can retrieve a set of plots for several flights or hundreds of time-steps
during post-campaign analysis or when compiling an overview over flights of a campaign
for a daily briefing.
This allows users to retrieve similar plots of the same parameters
such as map section, level etc., on a daily basis. 
Jatin Jain (@Jatin2020-24) did UI and server improvements in his Google Summer of Code 2022 project.
Users can now, compare and plot multiple flightpaths on topview.
This feature can be used for flightpathes or MSColab operations. A fligthpath style width can be changed.
Timestamps are dislayed below each message in MSColab. Mscolab Operations in use for more than 30 days, move to an inactive list.
The initial idea for multiple flightpaths on topview stems from bkirbus.
GSoC mentors were Reimar Bauer, Jörn Ungermann, Sonja Gisinger

* **7.0.0** was a refactoring release for consistent nameings. The individual components got more appropriate names.
The new naming scheme was used in the publication:
Bauer, R., Grooß, J.-U., Ungermann, J., Bär, M., Geldenhuys, M., and Hoffmann, L.: The Mission Support System (MSS v7.0.4) and its use in planning for the SouthTRAC aircraft campaign, Geosci. Model Dev., 15, 8983-8997, https://doi.org/10.5194/gmd-15-8983-2022, 2022.

* **6.0.0** Aravind Murali (@aravindm711) redesigned in Google Summer of Code 2021 the MSUI interface.
This now connects in a user-friendly way the editing of flight paths locally
or remotely with other users. In addition, Aravind Murali has improved a configuration editor for our json mss_settings file
and made this user-friendly. 
Hrithik Kumar Verma (@risehr) developed a toolchain for the automatic creation of tutorials
in the Google Summer of Code 2021. May Bär (@Marilyth) introduced an all in one installation script for MSS and all dependencies.
Jörn Ungermann (@joernu76) improved kml visualizing the same way as of a flightpath. Reimar Bauer (@ReimarBauer) improved permissions, projects and signalling for mscolab.

* **5.0.0** May Bär (@Marilyth) added a gallery of view graphics which a server can provide. Have a look at
our documentation on https://mss.readthedocs.io/en/stable/gallery/index.html for this feature. 
May Bär introducd a new docking widget for topview for integrating airbase data by openaip.net and ourairports.com

* **4.0.0** May Bär (@Marilyth) added a new view mode of 1-D samples along the flight path.
A lot of UI improvements, e.g. import and export filters, topview history and home button implemented
for stereographic projections

* **3.0.0** May Bär (@Marilyth) implemented multilayer support for the Server and Client. By this
Layers have a selectable priority in which they will be displayed.

* **2.0.0** Shivashis Padhi (@plant99) created the fundament for a collaboration server in the MSS project in Google Summer of Code 2019.
Tanish Grover (@Tanish0019) continued this work in the Google Summer of Code 2020 and overworked our user interface. 
The KML docking widget was improved in Google Summer of Code 2020 by Aryan Gupta (@withoutwaxaryan).
Vaibhav Mehra (@veb7vmehra) has integrated an editor for the MSS setting file. 
After 2.0.0 we use semantic versioning.

* **1.1.0** First Open Source public release on June 28, 2016. Installation recipes based on conda. Documentation on http://mss.rtfd.io

For further details look into our releases.