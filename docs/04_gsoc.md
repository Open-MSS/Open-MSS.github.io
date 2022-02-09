---
layout: page
title: GSOC ideas
permalink: /develop/GSOC/ideas
exclude: false
---

# In Preparation

# Contacting the MSS team
If you want to contribute to Mission Support System, 
please consider joining our Slack channel [https://mss-devel.slack.com](https://mss-devel.slack.com), 
where we discuss everything related to the development of the project and we can answer 
all your questions related to the project. You can join the channel by sending us an 
email at <mss-info@fz-juelich.de>.

# Questions 
If you have any question please feel free to ask any of the mentors on our #gsoc slack channel.

# Initial good first issues
We have labled small sized issues as "good first issue" on <https://github.com/Open-MSS/MSS/issues>.

# Getting Started
 - You can quickly setup MSS on your machine by following the steps given in our [setup instructions](/develop/Setup-Instructions). If you want to use Docker you can follow the steps in our [docker setup guide](/develop/docker_images). For more details, you can read [Mission Support System’s Documentation](https://mss.readthedocs.io/en/stable)
 - You can go through the issues labelled as [good first issue](https://github.com/Open-MSS/MSS/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22) on our github repository and pick an issue you feel you can take up. Please write a comment on the issue you're taking up so multiple people don't work on the same issue. If you have any doubts related to the issue feel free to ask us on the Slack channel. You can also report any new issue you find on the Slack channel itself.
 - Once you've found the issue you want to work on you need to create a new branch on your local clone of the project and start working on it. As a general rule of thumb, bug fixes go to the `stable` branch while enhancements and other new features go to the `develop` branch. Generally it is mentioned in the issue itself which branch the fix needs to go. Otherwise you can always ask us on Slack.
 - To start working, create a new git branch, write your code, commit it and push this branch to your fork. Now create a pull request to the Master Repo's `develop` or `stable` branch. All pull requests must pass the test pipeline before they are merged.


# Project Ideas

## Difficulty level: Hard
 * [wms: Update Geographical Plotting Routines](/develop/GSOC/update_geographical_plotting_routines)
 * [wms: Support Of Simple Trajectory Calculations](/develop/GSOC/support_of_simple_trajectory_calculations)
 * [msc: MQTT over Websocket](/develop/GSOC/mqtt_over_websocket)
 * [msui: Overlay Measured Data](/develop/GSOC/overlay_measured_data)

## Difficulty level: Medium
 * [msui: Catalogue Service For The Web (CSW)](/develop/GSOC/catalogue_service_for_the_web)
 * [cli: Advanced CLI Plotting](/develop/GSOC/automated_plotting)
 * [msui: Modernize fs_filepicker](/develop/GSOC/modernize_fs_filepicker)
 * [cli: Improve Tutorials](/develop/GSOC/improve_tutorials)
 * [wms: Plot Gallery integrated](/develop/GSOC/integrated_plot_gallery)
 * [msui/wms: UI and server improvements](/develop/GSOC/ui_server_improvements)
 * [msui/msc: View Layout and Restoring](/develop/GSOC/view_restoring)
 


## Your own idea

The above projects are just suggestions --- it is also very good to suggest a project idea of your own if you have
something in mind that you want to do. Ask people on the 
[mailing list](https://lists.fz-juelich.de/mailman/listinfo/mss-info) for suggestions in this case.




## Writing your GSoC application

Please follow the [Instructions](/develop/GSOC/instructions) filing your application

We recommend getting your final proposal reviewed by the mentors of that project before the 
proposal submission deadline so you can make changes in time.

You can take a look at the following projects from previous years to get help for your proposal.

### GSoC'21 Projects

- [Hrithik Kumar Verma: Generating a tool chain tutorial for the MSUI user interface by automation operations : GSoC 2021](https://github.com/Open-MSS/MSS/wiki/Generating-a-tool-chain-tutorial-for-the-MSUI-user-interface-by-automation-operations-:-GSoC---2021)

- [Aravind Murali: MSUI: UI Redesign GSOC 2021](https://github.com/Open-MSS/MSS/wiki/MSUI:-UI-Redesign---GSOC-2021)

### GSoC'20 Projects

- [Aryan Gupta: Mission Support System : Enhance KML Support](https://github.com/Open-MSS/MSS/wiki/KML:-Enhance-KML-Support---GSoC-2020)

- [Tanish Grover: Mission Support System: Mission Support Collaboration Improvements](https://github.com/Open-MSS/MSS/wiki/Mscolab:-Mission-Support-Collaboration-Improvements---GSoC-2020)

### GSoC'19 Projects

- [Anveshan Lal: Updating Geographical Plotting Routines](https://github.com/Open-MSS/MSS/wiki/Cartopy:-Updating-Geographical-Plotting-Routines----GSoC-2019)

- [Shivashis Padhi: Collaborative editing of flight path in real-time](https://github.com/Open-MSS/MSS/wiki/Mscolab:-Collaborative-editing-of-flight-path-in-real-time---GSoC19)
