---
layout: page
title: Contributing
permalink: /contributing/
---

## Getting Started

If you want to contribute to Mission Support System, please consider joining our Slack channel [https://mss-devel.slack.com](https://mss-devel.slack.com), where we discuss everything related to the development of the project and we can answer all your questions related to the project. You can join the channel by sending us an email at <mss-info@fz-juelich.de>.

Once you have joined the Slack channel you can head over to our repository - [https://github.com/Open-MSS/MSS](https://github.com/Open-MSS/MSS) on github and create a fork to start contributing.

## Tech Stack

MSS is completely written in Python. The GUI is built using [PyQT5](https://www.riverbankcomputing.com/software/pyqt/) and the backend servers use Python's [Flask](https://flask.palletsprojects.com/en/1.1.x/) framework.

## Setup Instructions

You can quickly setup MSS on your machine by following the steps given in our [setup instructions](/develop/Setup-Instructions). If you want to use Docker you can follow the steps in our [docker setup guide](/develop/docker_images). For more details, you can read [Mission Support System’s Documentation](https://mss.readthedocs.io/en/stable)

## Finding Issues

To get started, you can go through issues labelled as [good first issue](https://github.com/Open-MSS/MSS/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22) on our github repository and pick an issue you feel you can take up. Please write a comment on the issue you're taking up so multiple people don't work on the same issue. If you have any doubts related to the issue feel free to ask us on the Slack channel. You can also report any new issue you find on the Slack channel itself.

## Writing Code and Making Pull Requests

Once you've found the issue you want to work on you need to create a new branch on your local clone of the project and start working on it. As a general rule of thumb, bug fixes go to the `stable` branch while enhancements and other new features go to the `develop` branch. Generally it is mentioned in the issue itself which branch the fix needs to go. Otherwise you can always ask us on Slack.

To start working, create a new git branch, write your code, commit it and push this branch to your fork. Now create a pull request to the Master Repo's `develop` or `stable` branch. All pull requests must pass the test pipeline before they are merged.

## GSoC Participants

MSS takes part in Google Summer of Code as a sub-organization of Python Software Foundation(PSF). If you're willing to participate in GSoC with us, please join the `#gsoc` channel on Slack. For proposal ideas you can view the [GSoC'21 project ideas list](/develop/GSOC2021/ideas).

We recommend getting your final proposal reviewed by the mentors of that project before the proposal submission deadline so you can make changes in time.

You can take a look at the following projects from previous years to get help for you proposal.

### GSoC'20 Projects

- [Aryan Gupta: Mission Support System : Enhance KML Support](https://github.com/Open-MSS/MSS/wiki/KML:-Enhance-KML-Support---GSoC-2020)

- [Tanish Grover: Mission Support System: Mission Support Collaboration Improvements](https://github.com/Open-MSS/MSS/wiki/Mscolab:-Mission-Support-Collaboration-Improvements---GSoC-2020)

### GSoC'19 Projects

- [Anveshan Lal: Updating Geographical Plotting Routines](https://github.com/Open-MSS/MSS/wiki/Cartopy:-Updating-Geographical-Plotting-Routines----GSoC-2019)

- [Shivashis Padhi: Collaborative editing of flight path in real-time](https://github.com/Open-MSS/MSS/wiki/Mscolab:-Collaborative-editing-of-flight-path-in-real-time---GSoC19)
