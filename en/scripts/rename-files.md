---
title: Rename files
desc: The script renames the file according to a regular expression.
img:
   rename-files: scripts/rename-files.png
html:
   rename-files: '<img src="%img.rename-files%" style="margin: 1em 1em;"/>'
---
# Rename Files

The **Rename Files** command renames files according to the specified regular expression.

%html.rename-files%

**Path**  
Specify the directory with the files to be renamed.

**Regular Expression**  
Specify a regular expression to be used to rename files. Files that do not match this regular expression will be skipped.

**New Filename**.  
Specify a new file name. You only need to specify the part that will be replaced with the found fragment for the specified regular expression. You can specify *$i* or *${i}* in this parameter to substitute the i-th subexpression.

``` txt
Original Name: myfile (1).txt
Regular Expression: \s\(\d\)\.
New Filename: .
Result Filename: myfile.txt

Original Name: myfile (1).txt
Regular Expression: \((\d+)\)
New Filename: [${1}
Result filename: myfile [1].txt
```

**If File Exists**  
You can specify an action if a file with the new name exists. The options are described in the [Copy File](copy-file.html) command.

**Recursive Search**  
**Exclude Wildcard or RegExp**  
These parameters are described in the [Foreach File](foreach-file.html) command.
