---
title: Parse filename
desc: The script parses the filename and gets the directory, filename and extension.
img:
   parse-filename: scripts/parse-filename.png
html:
   parse-filename: '<img src="%img.parse-filename%" style="margin: 1em 1em;"/>'
---
# Parse Filename

The **Parse Filename** command gets the directory, filename and extension from the specified filename. The script does not check if the specified file exists. Also, the operation of the script depends on the operating system. For example, the command will not determine the directory for *c:\my folder\myfile.txt* on Linux.

%html.parse-filename%

**Filename**  
Specify the name of the file you want to parse.

**Variable name**  
Specify a variable name where the directory, file name and extension will be written. This variable is an object that contains the following fields:

* **dir** - directory;
* **filename** - filename without path;
* **ext** - extension of the file;
* **fileonly** - file name without path or extension.

For example, if you specified the variable name *fi* and the file name is *C:\Data\my folder\mydata.txt*, then after calling the script, the output of this text to the console

``` txt
Dir = #fi.dir#
Filename = #fi.filename#
Ext = #fi.ext#
Fileonly = #fi.fileonly#
```

will give the following result

``` txt
Dir = C:\Data\my folder
Filename = mydata.txt
Ext = txt
Fileonly = mydata
```

In addition, an ordinary variable will be created with a name equal to *Variable Name*, which is equal to the *Filename* parameter.
