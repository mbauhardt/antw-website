---
layout: documentation
title: Usage Ant
---
{% include JB/setup %}

## Usage

### Apache-Ant
It is not recommended but when you want to try the antw loggers without to install *antw* you can integrate the loggers manually to your ant build.
Goto the [downloads](/downloads) page and download the *antw-logger-0.6.1-fat.jar* and add this jar file to the cmd line when execute ant.

    ant -lib antw-logger-0.6.1-fat.jar -logger antw.logger.AntwLogger <command>

You should see the same logging like when you use the antw app itself. But strongly recommended is to install the whole app.


