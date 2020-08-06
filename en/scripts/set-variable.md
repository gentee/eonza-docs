---
title: Assign a value to a variable
desc: The script assigns the specified value to the variable.
img:
   set-variable: scripts/set-variable.png
   sample-1: scripts/sample-1.png
html:
   set-variable: '<img src="%img.set-variable%" style="margin: 1em 1em;"/>'
   sample-1: '<img src="%img.sample-1%" style="margin: 1em 1em;"/>'
---
# Set Variable

The **Set Variable** command assigns the specified value to the variable. If the variable does not exist, it will be created. To substitute the value of a variable, use **#varname#**, where *varname* is the name of the variable.

%html.set-variable%

**Variable name**  
Specify the name of the variable to which you want to assign the value.

**Value**  
Specify the value to be assigned to the variable. It can be multi-line.

* [%dwnsample%](/samples/sample-1.yaml)

%scriptresult%

%html.sample-1%
