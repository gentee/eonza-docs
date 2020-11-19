---
title: Copy files to another directory
desc: The script copies files from the directory to another one.
img:
   copy-files: scripts/copy-files.png
html:
   copy-files: '<img src="%img.copy-files%" style="margin: 1em 1em;"/>'
---
# Copy Files

The **Copy files** command copies files from the directory to another one according to the specified masks and regular expressions. If no masks and regular expressions are specified, all files will be copied.

%html.copy-files%

**Path**  
Specify the directory with the files to be copied.

**Destination Folder**  
The directory where the files will be copied. When copying, the hierarchy of subdirectories is preserved.

**If File Exists**  
You can specify an action for the case when the copied file exists in the target directory. The options are described in the [Copy File](copy-file.html) command.

**Recursive Search**  
**Wildcard or RegExp**  
**Exclude Wildcard or RegExp**  
These parameters are described in the [Foreach File](foreach-file.html) command.
