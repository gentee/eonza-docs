---
title: Go through the elements of the object variable
desc: The command launches nested commands for each element of the object variable.
img:
   foreach: scripts/foreach.png
   foreach-sample: scripts/file-list-sample.png
html:
   foreach: '<img src="%img.foreach%" style="margin: 1em 1em;"/>'
   foreach-sample: '<img src="%img.foreach-sample%" style="margin: 1em 1em;"/>'
---
# Foreach

The **Foreach** command executes nested commands for each element of the specified object variable.

%html.foreach%

**Variable Name**  
Specify a variable name. This variable must be an object of an array or an associative array (map) type. Nested commands will be executed for each of its elements.

**Variable Item**  
Specify the name of the variable into which the next element will be written. This variable will also be an object.

**Variable Index**  
You can specify a variable name to get the index of the item. For arrays it is counted from 0, for associative arrays, the corresponding key will be written to the variable.

[%dwnsample%](/samples/file-list-sample.yaml)

%scriptresult%

%html.foreach-sample%
