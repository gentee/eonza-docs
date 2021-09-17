---
title: Auto increment file name if it exists
desc: The command adds a suffix to the filename if a file with that name already exists.
img:
   auto-increment-filename: scripts/auto-increment-filename.png
html:
   auto-increment-filename: '<img src="%img.auto-increment-filename%" style="margin: 1em 1em;"/>'
---
# Auto Increment Filename

The **Auto Increment Filename** command checks if the specified file exists. If the file exists, a suffix *(index)* will be appended to it, where **index** is such a number that a file with this name does not exist. Otherwise, the specified file name will be written to the resulting variable. The index count starts at 1. The suffix is added to the file name before the first extension - *my data (7).tar.gz*. The command does not create any file, it only looks for the first free name with a suffix.

%html.auto-increment-filename%

**Filename**  
Specify the full or relative path to the file that you want to check for existence. If the specified file does not exist, then this name will be written to the resulting variable unchanged. Otherwise, a suffix will be added.

**Result Variable**  
Specify the name of the variable into which the name of the first non-existent file will be written.

Suppose there are the following files - */home/user/logs/data.log* and */home/user/logs/data (1).log*. You need to copy another *data.log* file there, but it must not overwrite the current files. If you specify **Filename** as */home/user/logs/data.log*, the resulting variable will be */home/user/logs/data (2).log*. Now you can copy a file with this
name there.
