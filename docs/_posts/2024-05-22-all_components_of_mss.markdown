---
layout: post
title:  "MSS 9.0.0 All Components of MSS"
date:   2024-05-22 17:10:11 +0100
categories: MSS update release
---

## All Components of MSS

With installing MSS you get all components described in our [docs](https://mss.readthedocs.io/en/stable/components.html). 
- MSUI (Mission Support User Interface): user interface to connect to WMS services and MSColab servers
- MSWMS/WMS: based Web Map Service 1.1.1/1.3.0 interface to provide forecast data from numerical weather predictions to the MSUI
- MSColab: collaborative environment for MSUI, with additional features such as chat-messages and keeping track of the made changes.

Everything is included in the [package](https://anaconda.org/conda-forge/mss).

You can setup your own WMS servers and provide your own plotting methods. Also you can setup your own MSColab collaboration server. 
And of course you can use our MSUI.



## MSUI
Our userinterface has majored and this is a short overview.

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


## Changelog of major versions: 

Version 9.0.0
-------------

Nilupul Manodya implemented SAML 2.0 (Security Assertion Markup
Language) Authentication. MSColab can now be configured with an existing
IdP or multiple IdPs. In this way, a user can authenticate themselves in
one system and gain access to another system by providing proof of
authentication. In our documentation in the Components section you find
a detailed description.

Matthias Riße refactored the test suite and optimized and accelerated
our CI test runs. All tests run in parallel now and are not retried upon
failure, and most tests are also executed in a randomized order,
instilling more confidence in the results. Quite a bit of duplicated
code was unified, mostly using pytest fixtures. Additionally, CI test
runs now also happen on x86_64- and ARM-based macOS.

Jörn Ungermann refactored various parts of MSColab for faster processing
with fewer requests.

Reimar Bauer refactored the tutorials and the documentation shows now
mp4 files embedded in html5.

#### HINT:

The syntax of the server configuration of MSColab and MSWMS has changed.
We removed the class definition. For MSColab we have added new
configuration options related to SAML2. The change on the MSColab server
also required changes on the MSUI handling the MSColab login. These
changes are not backwards compatible. MSColab Server and MSUI Client must use
versions >=9.0.0. We introduced a MSCOLAB_auth_user_name in the
users configuration which simplifies the login process.

All changes: <https://github.com/Open-MSS/MSS/milestone/93?closed=1>


Version 8.0.0
-------------

Sreelakshmi Jayarajan created a new CLI module for automated plotting by
an user and refactored existing plotting and QT based classes modules.
These classes can be used for plotting purposes without involving
QT-based GUI and Interactive functionalities. Users can retrieve a set
of plots for several flights or hundreds of time-steps during
post-campaign analysis or when compiling an overview over flights of a
campaign for a daily briefing. This allows users to retrieve similar
plots of the same parameters such as map section, level etc., on a daily
basis. The initial idea stems from Jörn Ungermann. GSoC mentors were
Reimar Bauer, Jörn Ungermann, Christian Rolf, Sonja Gisinger

Jatin Jain did UI and server improvements in his GSoC project. Users can
now, compare and plot multiple flightpaths on topview. This feature can
be used for flightpathes or MSColab operations. A fligthpath style width
can be changed. Timestamps are dislayed below each message in MSColab.
Mscolab Operations in use for more than 30 days, move to an inactive
list. The initial idea for multiple flightpaths on topview stems from
bkirbus. GSoC mentors were Reimar Bauer, Jörn Ungermann, Sonja Gisinger

With MSS 8.0.0 we base our installation on miniforge. This has mamba in
the base environment. Mambaforge is discouraged of September 2023.

All changes: <https://github.com/Open-MSS/MSS/milestone/81?closed=1>


Version 7.0.0
-------------

This is a refactoring release for consistent nameings. Over the last six
years MSS has grown and we created the Open-MSS organization with the
move to github in 2021. In this we have many repositories that support
our work on the Mission Support System. We use the term MSS for the
whole thing today. Therefore, we would like to give more appropriate
names to the individual components.

#### HINT:


We changed: 
- command mss was renamed to msui
- constants.MSS_CONFIG_PATH to constants.MSUI_CONFIG_PATH
- constants.MSS_SETTINGS to constants.MSUI_SETTINGS
- class MissionSupportSystemDefaultConfig to class MSUIDefaultConfig
- class MSS_AboutDialog to class class MSUI_AboutDialog
- class MSS_LV_Options_Dialog to class MSUI_LV_Options_Dialog
- class MSS_PerformanceSettingsWidget to class MSUI_PerformanceSettingsWidget
- class MSS_ShortcutsDialog to class MSUI_ShortcutsDialog
- class MSS_SV_OptionsDialog to class MSUI_SV_OptionsDialog
- class MSS_TV_MapAppearanceDialog to class MSUI_TV_MapAppearanceDialog
- class MSSLinearViewWindow to class MSUILinearViewWindow
- class MSSMainWindow to class MSUIMainWindow
- class MSSMplViewWindow to class MSUIMplViewWindow
- class MSSMscolab to class MSUIMscolab
- class MSSSideViewWindow to class MSUISideViewWindow
- class MSSTableViewWindow to class MSUITableViewWindow
- class MSSTopViewWindow to class MSUITopViewWindow
- class MSSWebMapService to class MSUIWebMapService

Configurations:
- Env var MSS_CONFIG_PATH to MSUI_CONFIG_PATH
- directory for msui_settings.json from ~/.config/mss to ~/.config/msui
- mss_settings.json to msui_settings.json
- mss_wms_settings.py to mswms_settings.py
- mss_wms_auth.py to mswms_auth.py
- mss_mscolab_auth.py to mscolab_auth.py

We moved:
- mslib.msui.mss_qt to mslib.utils.qt
- mslib.msui.mss_pyui to mslib.msui.msui


All changes: <https://github.com/Open-MSS/MSS/milestone/68?closed=1>


Version 6.0.0
-------------

Aravind Murali redesigned in google summer of code 2021 the MSUI
interface. This now connects in a user-friendly way the editing of
flight paths locally or remotely with other users. Many of Jörn
Ungermann\'s ideas were implemented. In addition, Aravind Murali has
improved a configuration editor for our json mss_settings file and made
this user-friendly. The initial idea of the new editor stems from Reimar
Bauer. GSoC mentors were Jörn Ungermann, May Bär, Reimar Bauer

Hrithik Kumar Verma developed a toolchain for the automatic creation of
tutorials in the Google Summer of Code 2021. This simplifies the
creation of video tutorials in a similar way to updating tests. Using
these tutorial scripts to create videos also increases test coverage.
The initial idea stems from Reimar Bauer. GSoC mentors were Reimar
Bauer, May Bär

Jörn Ungermann improved kml visualizing the same way as of a flightpath.

Reimar Bauer improved permissions, projects and signalling for mscolab.

All changes: <https://github.com/Open-MSS/MSS/milestone/50?closed=1>


Version 5.0.0
-------------

This release brings many improvements to the WMS Server along with new
features for the UI. May Bär implemented a gallery feature. On demand a
WMS server can show what kind of view graphics are provided. Optional
the source for creating the graphics can be published over the web
service too. By this any existing server shows examples how to create
graphics. Have a look on our documentation on
<https://mss.readthedocs.io/en/stable/gallery/index.html> for this
feature.

The linear styles got improved to work also on .ml files

We refactored some of our oldest code in thermolib and moved to the
famous metpy module. A new docking widget for topview was introduced for
integrating airbase data by openaip.net and ourairports.com

Newer versions than 5.0.0 can now use the built-in update feature on
command line or by the UI.

All changes: <https://github.com/Open-MSS/MSS/milestone/59?closed=1>


### Version 4.0.0

This release brings a new view mode of 1-D samples along the flight
path. Also in sideview waypoint symbols and corresponding vertical lines
can be switched off. A lot of UI improvements, e.g. import and export
filters, topview history and home button implemented for steorographic
projections

#### HINT:


For using the 1-D samples along the flight path you have to add a
configuration to your mss_wms_settings.py. Similiar as to the other
layers add:

``` {.python}
register_linear_layers = None
if mpl_lsec_styles is not None:
    register_linear_layers = [
        # ECMWF standard 1D section styles.
        (mpl_lsec_styles.LS_DefaultStyle, "air_temperature", ["ecmwf_EUR_LL015"]),
        (mpl_lsec_styles.LS_DefaultStyle, "divergence_of_wind", ["ecmwf_EUR_LL015"]),
    ]
```

All changes: <https://github.com/Open-MSS/MSS/milestone/52?closed=1>


### Version 3.0.0

May Bär implemented multilayer support for the Server and Client. By
this Layers have a selectable priority in which they will be displayed.
The multilayers are searchable and filterable. Layer parameters can be
synchronized. The used style of each layer is persistently stored. The
selection of layers is supported by favorization.

#### Hint:

With version 3.0.0 we change our default channel order. conda-forge is
now sorted before defaults.

All changes: <https://github.com/Open-MSS/MSS/milestone/3?closed=1>


### Version 2.0.0

Shivashis Padhi created the fundament for a collaboration server in the
MSS project in google summer of code 2019. Tanish Grover continued this
work in the google summer of code 2020 and overworked our user
interface. The initial idea of mscolab stems from Reimar Bauer. GSoC
mentors were Reimar Bauer and Jörn Ungermann. In addition to the mswms
server the project now has a mscolab server for editing a flight path.

Vaibhav Mehra has integrated an editor for the MSS setting file.

The KML docking widget was improved in google summer of code 2020 by
Aryan Gupta. GSoC mentors were Jörn Ungermann and Christian Rolf.
Initial idea of the project by Jörn Ungermann.

All changes: <https://github.com/Open-MSS/MSS/milestone/7>

With Version 2.0.0 we changed to semantic versioning scheme, for older changes read our
[CHANGES.rst](https://github.com/Open-MSS/MSS/blob/develop/CHANGES.rst)

