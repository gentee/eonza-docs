---
title: Get file list
desc: Get the list of files into a variable object.
img:
   file-list: scripts/file-list.png
   file-list-sample: scripts/file-list-sample.png
html:
   file-list: '<img src="%img.file-list%" style="margin: 1em 1em;"/>'
   file-list-sample: '<img src="%img.file-list-sample%" style="margin: 1em 1em;"/>'
---
# File List

The **File List** command gets an array of files that match the specified parameters. It saves this array to a variable object.

%html.file-list%

**Path**  
**Recursive search**  
**Wildcard or regular expression**  
These parameters are described in the [Foreach File](foreach-file.html) command.

**Result Variable**  
Specify the name of the variable where the resulting list will be saved. The variable is an array of objects with fields *name, size, time, dir*, etc. Later, you can use this variable in other commands (e.g. [Foreach](foreach.html)) to process this file list.

[%dwnsample%](/samples/file-list-sample.yaml)

%scriptresult%

%html.file-list-sample%
