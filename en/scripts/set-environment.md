---
title: Set Environment Variables
desc: The script sets the environment variables.
img:
   set-environment: scripts/set-environment.png
   sample-environment: scripts/sample-environment.png
html:
   set-environment: '<img src="%img.set-environment%" style="margin: 1em 1em;"/>'
   sample-environment: '<img src="%img.sample-environment%" style="margin: 1em 1em;"/>'
---
# Set Environment

The **Set Environment** command assigns the specified values ​​to the environment variables. Add a separate entry to the table for each variable. If some environment variable does not exist, then it will be created.

%html.set-environment%

**Variable name**  
Specify the name of the environment variable you want to assign a value to.

**Value**  
Specify the value to be assigned. If no value is specified, then this environment variable will be unset.

* [%dwnsample%](/samples/sample-environment.yaml)

%scriptresult%

%html.sample-environment%
