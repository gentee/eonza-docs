---
title: Create a temporary file
desc: The command creates a temporary file.
img:
   create-temporary-file: scripts/create-temporary-file.png
html:
   create-temporary-file: '<img src="%img.create-temporary-file%" style="margin: 1em 1em;"/>'
---
# Temporary File

**v1.24**  
The **Temporary file** command creates a temporary file with a randomly generated name. In the future, it is advisable to delete the created file if it is no longer needed.

%html.create-temporary-file%

**Text**  
Specify the text that will be written to the created file.

**Filename Pattern**  
By default, a file with a name of random numbers is created. You can specify a prefix to be added at the beginning of the name. If you want a random number to be in the middle of the file name, then specify the `*` symbol in the required place.

```txt
my => my4604338
pref*.txt => pref1028002494.txt
```

**Result Variable**  
Specify the name of the variable that will contain the full name of the generated file.

## Optional Parameters

**path**  
By default, the file is created in the system temporary directory. You can specify any directory where you want to create a temporary file.

```txt
path: /home/user/tmp
```
