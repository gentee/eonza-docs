---
title: Write variable value to file
desc: The command writes the value of a variable to a file.
img:
   write-file: scripts/write-file.png
html:
   write-file: '<img src="%img.write-file%" style="margin: 1em 1em;"/>'
---
# Write To File

The **Write To File** command writes the value of the variable and/or text to the specified file.

%html.write-file%

**Variable Name**  
Specify the name of the variable whose value you want to write. If no variable name is specified, the text that is specified in the following field will be written.

**Text**  
Instead of the variable name, you can specify the text that you want to save to the file. If a variable name is specified, the text will be added after the variable value.

**Filename**  
Specify the full or relative path to the file where you want to write data. If the file does not exist, then it will be created.

**Append Data**  
By default, if the file exists, it will be overwritten. Check this checkbox if you want to append data to the end of the file.
