---
title: Script for handling empty directories
desc: The script executes commands for each empty folder found.
img:
   foreach-empty-dir: packages/foreach-empty-dir.png
html:
   foreach-empty-dir: '<img src="%img.foreach-empty-dir%" style="margin: 1em 1em;"/>'
---
# Foreach Empty Dir

The **Foreach Empty Directory** script searches for empty directories and executes nested commands for each empty folder found.

%html.foreach-empty-dir%

**Path**  
Specify the directory in which you want to search for empty directories.

**Wildcard or RegExp**  
**Exclude Wildcard or RegExp**  
These parameters are described in command [Foreach File](/scripts/foreach-file.html).

**Variable name**  
Specify the name of the variable that will be assigned the full path of the found empty directory. You can use this variable in nested commands.
