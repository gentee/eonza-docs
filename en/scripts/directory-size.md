---
title: Get the size of the directory
desc: The script returns the size of the directory and the number of files in it.
img:
   directory-size: scripts/directory-size.png
html:
   directory-size: '<img src="%img.directory-size%" style="margin: 1em 1em;"/>'
---
# Directory Size

The **Directory Size** command gets the size and number of files in the specified directory. All files in subdirectories are counted.

%html.directory-size%

**Path**.  
Specify the full or relative path to the directory about which you want to get information.

**Result Variable**  
Specify the name of the variable where the total size of files in the directory will be written. In addition, a variable object with the same name with the following fields will be created:

* **size** - size of all files in the directory.
* **files** - number of files in the directory.
* **dirs** - number of subdirectories in the directory.

For example, if you specified the variable name *di*, you can get such values:

``` txt
#di# = "134594040"
#di.size# = "134594040"
#di.files# = "253"
#di.dirs# = "12"
```
