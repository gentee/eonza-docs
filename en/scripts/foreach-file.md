---
title: Loop for each file or directory
desc: The command runs nested commands for each file or directory.
img:
   foreach-file: scripts/foreach-file.png
html:
   foreach-file: '<img src="%img.foreach-file%" style="margin: 1em 1em;"/>'
---
# Foreach File

The **Foreach File** command executes the nested commands for each file and directory that match the specified parameters.

%html.foreach-file%

**Path**  
Specify the full or relative path to the directory where the files are searched for.

**Recursive Search**  
Check this checkbox if you want to search for files in all subdirectories.

**Search Only for Files**  
Click this checkbox if you want to search only for files.

**Wildcard or RegExp**  
You can specify a wildcard or a regular expression to search for files. In this case, the file or directory will be processed only if its name matches the specified mask or regular expression.
The wildcard is a string using characters:

* '\*' - any sequence except the delimiter character
* '?' - any single character except the delimiter character

``` text
*.pdf  
??file.
```

If you want to use a regular expression, add the '/' character at the beginning and end.

``` text
/\d\d .*/
/\w*\.txt$/
```

**Variable Name**  
Specify the variable name where the name of the current file will be written. You can use this variable in nested commands. In addition, variables with the following suffixes will be created:

* **_size** - file size.
* **_dir** - full path of the directory where the file is located.

For example, if you have specified the variable name *myfile*, the following variables will be defined for the file */home/user/tmp/myfile.txt* with the size of 64 bytes:

``` go
myfile = "myfile.txt"
myfile_size = "64"
myfile_dir = "/home/user/tmp"
```
