---
title: Copy file to another directory
desc: The command copies the file to another directory.
img:
   copy-file: scripts/copy-file.png
html:
   copy-file: '<img src="%img.copy-file%" style="margin: 1em 1em;"/>'
---
# Copy File

The **Copy** command copies the specified file to another directory.

%html.copy-file%

**Source File**  
Specify the full or relative path of the file to be copied.

**Destination Folder**  
Specify the full or relative path to the directory where the file should be copied.

**If File exists**  
You can specify what to do if a file already exists in the target directory.

* *Overwrite* - overwrite the existing file.
* *Overwrite if newer* - overwrite the existing file, if the file being written is newer. Otherwise, the file will be skipped.
* *Skip* - do not write the file.
* *Ask* - ask the user for permission to overwrite this file.
* *Ask if newer* - ask the user for permission to overwrite the file only if it is newer. Otherwise, the file will be skipped.
* *Save a copy* - the file will be saved as a copy with a name like *filename (1).ext*.

**Save File Time**  
Check this checkbox if you want to save the time of the copied file.

## Optional Parameters

**Hide Apply to All**  
The confirmation form has a checkbox *Apply the action to all files*. If **hideapply** is *true*, then this checkbox will not be shown. Otherwise, it will be displayed. By default, **hideapply** is *true* and the checkbox is hidden.

``` txt
hideapply: false
```

**Result Variable**  
You can specify the name of the resulting variable in **resultvar** parameter to get the information what the user has clicked in the [File Confirmation](/scripts/file-confirmation.html) form. If the form was not shown, the object variable will contain empty strings.

``` txt
resultvar: action
```
