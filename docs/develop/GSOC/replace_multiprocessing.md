---
layout: page
title: GSOC Idea
permalink: /develop/GSOC/replace_multiprocessing
exclude: true
---
# Replace multiprocessing usage in test fixtures with subprocess

- **Project description**:
We want to use our tests on all supported platforms. This means we have to remove*/replace the multiprocessing fork method by subprocess.
A server process during tests should start in its own python process. This separation enables options for testing with e.g. basic_auth or different wsgi servers.


- **Duration**: 175-350h
- **Skills**: Python, (flask), (socketIO), pytest, Git, AI-Assistant
- **Difficulty level**: Medium
- **Related Readings/Links**:
- **Potential mentors**:
  m.risse@fz-juelich.de, rb.proj@gmail.de
