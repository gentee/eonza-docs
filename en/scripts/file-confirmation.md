---
title: Ask confirmation about file replacement
desc: The script asks the user to replace an existing file.
img:
   file-confirmation: scripts/file-confirmation.png
   file-confirmation-1: scripts/file-confirmation-1.png
html:
   file-confirmation: '<img src="%img.file-confirmation%" style="margin: 1em 1em;"/>'
   file-confirmation-1: '<img src="%img.file-confirmation-1%" style="margin: 1em 1em;"/>'
---
# File Confirmation

The **File Confirmation** command can be used when the script is going to overwrite an existing file. This command shows a form with information about the existing and new file and waits for user actions.

%html.file-confirmation%

**Existing File**  
Specify the name of an existing file. If there is no such file, the script will terminate with an error.

**New File Information**  
Specify the size and modification time of the new file, separated by comma.

``` txt
34567,2020-11-17 15:13:25
#fi.size#,#fi.time#
```

**Result Variable**  
Specify the name of the object variable to get information from the user. This variable will be assigned an object with the following fields:

* **all** - equals *true*, if the selected action should be applied to all files. Otherwise, it is *false*.
* **btn** - the selected action. Can be one of the following values:
    * *overwrite* - replace the file.
    * *skip* - skip the file.

%html.file-confirmation-1%

## Optional Parameters

**Hide Apply to All**  
The confirmation form has a checkbox *Apply the action to all files*. If **hideapply** is *true*, then this checkbox will not be shown. Otherwise, it will be displayed. By default, **hideapply** is *true* and the checkbox is hidden.

``` txt
hideapply: false
```
