---
title: Delete file or empty directory
desc: The command removes a file or an empty directory.
img:
   delete-file: scripts/delete-file.png
html:
   delete-file: '<img src="%img.delete-file%" style="margin: 1em 1em;"/>'
---
# Delete File

The **Delete File** command deletes the specified file or empty directory.

%html.delete-file%

**Path**  
Specify the full or relative path to the directory or file to be deleted. If a directory is specified and it is not empty, an error will be generated.

**Skip if file does not exist**  
By default, an error is returned if the specified file does not exist. Check this checkbox if you want to skip non-existent files.
