---
title: Delete empty directories
desc: The script removes empty directories.
img:
   delete-empty-dirs: packages/delete-empty-dirs.png
   delete-empty-dirs-confirm: packages/delete-empty-dirs-confirm.png
html:
   delete-empty-dirs: '<img src="%img.delete-empty-dirs%" style="margin: 1em 1em;"/>'
   delete-empty-dirs-confirm: '<img src="%img.delete-empty-dirs-confirm%" style="margin: 1em 1em;"/>'
---
# Delete Empty Dirs

The **Delete Empty Directories** script looks for empty directories and removes them. If you wish, you can display a list of empty directories and mark directories for deletion manually.

%html.delete-empty-dirs%

**Path**  
Specify the directory in which you want to search for empty directories and delete them.

**Wildcard or RegExp**  
**Exclude Wildcard or RegExp**  
These parameters are described in command [Foreach File](/scripts/foreach-file.html).

**Confirm Deletion**  
Check this box if you want to choose which of the found directories to delete. In this case, you will see a list of found empty directories and the script will remove only the directories you marked.

%html.delete-empty-dirs-confirm%
