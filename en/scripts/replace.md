---
title: Replace substrings in the text
desc: The command replaces substrings in the text and assigns the result to a variable.
img:
   replace: scripts/replace.png
html:
   replace: '<img src="%img.replace%" style="margin: 1em 1em;"/>'
---
# Replace

The command **Replace** takes the value of the variable and sequentially replaces the specified substrings with new  values.

%html.replace%

**Variable name**  
Specify the name of the variable in which substrings will be replaced. By default, the new value will be assigned to the same variable. If you do not want to change the value of the variable, specify the parameter *Result Variable*.

**Substitute Variable Values**  
Click this checkbox if you want to substitute the values ​​of variables like *#varname#* everywhere.

## What to find and replace

You can add multiple substrings for search and replacement.

**What to find**  
A substring to be replaced.

**Replace with**  
The string to be inserted instead of the found substring.

**Result Variable**  
By default, the result of substring replacement is written to the initial variable. If you want to assign the result to another variable, specify its name here.
