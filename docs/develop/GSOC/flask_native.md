---
layout: page
title: GSOC Idea
permalink: /develop/GSOC/flask_native
exclude: true
---

# use flask-native global configuration

- **Project description**:
Every Flask app has a .config attribute to store configuration. Additionally, for MSColab/MSWMS we have mscolab_settings/mswms_settings. This is redundant, we could just use app.config for everything that should be made globally available in the application in a key-value fashion.

- **Duration**: 175-350h
- **Skills**: Python, flask, pytest Git, AI-Assistant
- **Difficulty level**: Medium
- **Related Readings/Links**:
  - https://github.com/Open-MSS/MSS/issues/2506
  - https://github.com/Open-MSS/MSS/issues/2442
  - https://flask.palletsprojects.com/en/3.0.x/patterns/appfactories/
- **Potential mentors**:
  m.risse@fz-juelich.de, rb.proj@gmail.com

