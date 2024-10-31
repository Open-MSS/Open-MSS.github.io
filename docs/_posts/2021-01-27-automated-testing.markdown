---
layout: post
title:  "Automated Testing and Docker"
date:   2021-01-27 15:25:30 +0100
categories: MSS testing docker
---

The [GitHub repository of MSS](https://github.com/Open-MSS/MSS) now features automatic testing on pushes and pull requests.
Implementing automatic testing required multiple steps to be done effectively.

Not wanting tests to fail due to updated packages or similar environmental issues, 
the first step was to create a docker image in which MSS is guaranteed to run.
Dockerfiles were created over at the [Open-MSS/dockerhub](https://github.com/Open-MSS/dockerhub) repository on GitHub.
One image for testing, one image of the develop branch of MSS and one image containing the latest stable release of MSS.
All of these images can be found publicly on the [openmss](https://hub.docker.com/u/openmss) dockerhub account.

The second step was to automatically build and test each of these images every day, to make sure they are all up-to-date and working.
This was realised through GitHub Actions. Via a scheduled Action, every image is getting built using their respective Dockerfile. 
Afterward, MSS is getting tested on them through pytest, and finally, if there were no errors during this process, the images get uploaded to dockerhub.

The final step was to use the docker images for automated testing on each push and pull request on the Open-MSS/MSS repository.
This was also done through GitHub Actions. Every push and every pull request triggers an Action to run.
This Action pulls the latest testing image from [openmss/testing-develop](https://hub.docker.com/r/openmss/testing-develop) and
runs the changed code through pytest. 

In the end three things were accomplished:
1. There is always a working docker image for MSS over at https://hub.docker.com/u/openmss
2. If environmental changes, like package updates, break MSS, this will be visible at the [scheduled test at](https://github.com/Open-MSS/MSS/actions/workflows/testing-scheduled.yml)
3. Every push and pull request gets tested, and if the test fails, it is a clear sign of issues in the code, not in the environment



### Update 2024-10-31
- Urls to DockerHub updated
- Url for scheduled test updated
- Typos corrected
