---
title: Remove empty folders 
desc: The command removes the empty subdirectories in the specified directory.
img:
   delete-empty-folders: scripts/delete-empty-folders.png
html:
   delete-empty-folders: '<img src="%img.delete-empty-folders%" style="margin: 1em 1em;"/>'
---
# Delete Empty Folders

The **Delete Empty Folders** command removes all empty subdirectories in the specified directory. **Beware of using this script!** Note that if there is a *A* subdirectory with only an empty *B* directory, then after deleting the *B* directory, the *A* folder will become empty and will also be deleted.

%html.delete-empty-folders%

**Path**  
Specify the full or relative path to the directory where you want to delete the empty folders. It is recommended to specify the absolute path to make sure that the correct directory is specified. The specified initial directory will not be deleted even if it is empty.
