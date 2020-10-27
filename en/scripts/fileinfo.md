---
title: Get information about the file
desc: The script gets information about the file.
img:
   fileinfo: scripts/fileinfo.png
html:
   fileinfo: '<img src="%img.fileinfo%" style="margin: 1em 1em;"/>'
---
# File Info

The **File Info** command retrieves information about the specified file.

%html.fileinfo%

**File Name**  
Specify the full or relative path to the file you want to get information about.

**Variable Name**  
Specify the variable name where the full file name will be written. In addition, variables with the following suffixes will be created:

* **.exist** - equals *true*, if the file exists and *false*, otherwise.
* **.isdir** - equals *true* if the specified file is a directory. Otherwise, it equals *false*.
* **.size** - file size.
* **.time** - time of last modification of the file in *YYYY-MM-DD HH:mm:ss* format.
* **.stime** - time of last modification of the file in *YYYYMMDDHHmmss* format.

For example, if you have specified the variable name *fi*, then for the file *myfile.txt* the variables with values similar to the following will be created:

``` go
fi = "/home/user/temp/myfile.txt"
fi.size = "4523"
fi.exist = "true"
fi.isdir = "false"
fi.time = "2020-09-16 11:20:34"
```
