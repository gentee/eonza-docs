---
title: Find duplicate files
desc: The script finds the same files and executes nested commands for them.
img:
   find-duplicate-files: packages/find-duplicate-files.png
html:
   find-duplicate-files: '<img src="%img.find-duplicate-files%" style="margin: 1em 1em;"/>'
---
# Find Duplicate Files

The **Find Duplicate Files** script searches for duplicate files in the specified directory and all subdirectories. It invokes nested commands for each set of the same files found. Files are considered identical if they have the same size and **MD5** hash. 

%html.find-duplicate-files%

**Path**  
Specify the directory in which you want to search for duplicate files. Duplicate files will be searched in all subdirectories.

**Wildcard or RegExp**  
**Exclude Wildcard or RegExp**  
These parameters are described in command [Foreach File](/scripts/foreach-file.html).

**Variable name**  
Specify the name of a variable, which will be assigned an associative array-object with the following fields.

* **size** - size of the same files;
* **md5** - MD5 hash of the same files;
* **list** - array of full names of found duplicate files.

Nested commands are executed for each set of identical files. You can use this variable in nested commands to perform the necessary actions.
