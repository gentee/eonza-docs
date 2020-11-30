---
title: Assign a value to a variable
desc: The script assigns the specified value to the variable.
img:
   set-variable: scripts/set-variable.png
   sample-1: scripts/sample-1.png
html:
   set-variable: '<img src="%img.set-variable%" style="margin: 1em 1em;"/>'
   sample-1: '<img src="%img.sample-1%" style="margin: 1em 1em;"/>'
---
# Set Variable

The **Set Variable** command assigns the specified value to the variable. If the variable does not exist, it will be created. To substitute the value of a variable, use **#varname#**, where *varname* is the name of the variable.

%html.set-variable%

**Variable name**  
Specify the name of the variable to which you want to assign the value.

**Value**  
Specify the value to be assigned to the variable. It can be multi-line.

## Functions

You can specify a list of functions that will sequentially convert the current value. In this case, the *Value* field is the initial value. If the *Value* field is not specified, then the current value of the variable is taken as the initial value. You can add these functions in the order you need. The final result will be assigned to the variable.

* **Absolute Path**. If the value is a relative path to a file or a directory, then it is converted into an absolute path.
* **Append**. The value of the field *Parameter* will be appended to the current value.
* **Append Path**. The path or file name in the *Parameter* field will be added to the current value with a **/** or **\\** separator, depending on the OS.
* **Get Environment Variable**. Get the value of the environment variable specified in the *Parameter* field. If the parameter is not specified, then the variable name is taken from the current value.
* **Length**. The length of the current value is returned. If there is a variable with such name, the length of its value is returned. If there is an object variable, the number of elements in the array (map) or 0 is returned.
* **Lower case**. Convert the current string to lower case.
* **Upper case**. Convert the current line to upper case.
* **Split**. Split the value into substrings formed by the separator. In the *Parameter* field, specify the separator string. If you want to use a space as a separator, specify *#.s#*. This function will assign the first substring to the current value and create an object with the same name as the variable name that will contain an array of substrings.
* **Substring**. Take a substring from the current line. Specify the offset and length of the substring separated by a colon (offset:length) in the *Parameter* field. For example, *10:4*.
* **Current Time**. Get the current time in the format specified in the *Parameter* field. If it is not specified, the *YYYY/MM/DD HH:mm:ss* format will be used by default.

* [%dwnsample%](/samples/sample-1.yaml)

%scriptresult%

%html.sample-1%
