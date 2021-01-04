---
title: Move files to another directory
desc: The script moves files from one directory to another.
img:
   move-files: scripts/move-files.png
html:
   move-files: '<img src="%img.move-files%" style="margin: 1em 1em;"/>'
---
# Move Files

**v1.10.0**  
The **Move Files** command moves files from one directory to another one according to the specified masks and regular expressions. If no masks and regular expressions are specified, then all files will be moved.

%html.move-files%

**Path**  
Specify the directory with files to be moved.

**Destination Folder**  
The directory where the files will be moved. The hierarchy of subdirectories is preserved when moving.

**If File Exists**  
You can specify the action for when the file to be moved exists in the target directory. The options are described in the [Copy File](copy-file.html) command.

**Recursive Search**  
**Wildcard or RegExp**  
**Exclude Wildcard or RegExp**  
These parameters are described in the [Foreach File](foreach-file.html) command.
