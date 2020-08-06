---
title: Assign values to variables 
desc: The script assigns values to several variables.
img:
   set-variables: scripts/set-variables.png
   sample-1: scripts/sample-1.png
html:
   set-variables: '<img src="%img.set-variables%" style="margin: 1em 1em;"/>'
   sample-1: '<img src="%img.sample-1%" style="margin: 1em 1em;"/>'
---
# Set Variables

The **Set Variables** command can assign values to several variables. Add a separate entry to the table for each variable. If some variable does not exist, then it will be created. To substitute the value of a variable, use **#varname#**, where *varname* is the name of the variable.

%html.set-variables%

**Variable name**  
Specify the name of the variable to which you want to assign the value.

**Value**  
Specify the value to be assigned to the variable. It can be multi-line.

* [%dwnsample%](/samples/sample-1.yaml)

%scriptresult%

%html.sample-1%
