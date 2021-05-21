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
You can specify a wildcard or a regular expression to search for files. In this case, the file or directory will be processed only if its name matches the specified mask or regular expression. You can specify multiple masks or regular expressions separated by commas. In this case, you can use both wildcards and regular expressions.

The wildcard is a string using characters:

* '\*' - any sequence except the delimiter character
* '?' - any single character except the delimiter character

``` text
*.pdf,*.docx  
??file.
```

If you want to use a regular expression, add the '/' character at the beginning and end.

``` text
/\d\d .*/,/^my/
/\w*\.txt$/
```

**Exclude Wildcard or RegExp**  
Similarly, you can specify masks and regular expressions to ignore such files and directories. Note that if a directory matches a specified mask or a regular expression, it is completely excluded from search with all its files.

``` text
.git,/^temp/
```

**Variable Name**  
Specify the variable name where the name of the current file will be written. You can use this variable in nested commands. In addition, variables with the following suffixes will be created:

* **.size** - file size.
* **.time** - the time the file was last modified.
* **.dir** - full path of the directory where the file is located.
* **.isdir** - equals *true* if the current item is a directory. Otherwise, it equals *false*.

For example, if you have specified the variable name *myfile*, the following variables will be defined for the file */home/user/tmp/myfile.txt* with the size of 64 bytes:

``` go
myfile = "myfile.txt"
myfile.size = "64"
myfile.dir = "/home/user/tmp"
myfile.isdir = "false"
```

## Optional Parameters

**Search only directories**  
If you want to search only directories, then specify **onlydirs** parameter equal to *true*.

``` txt
onlydirs: true
```
