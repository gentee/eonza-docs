---
title: Append item to array
desc: The script appends an item to the array.
img:
   append-to-array: scripts/append-to-array.png
html:
   append-to-array: '<img src="%img.append-to-array%" style="margin: 1em 1em;"/>'
---
# Append To Array

**v1.21.0**  
The **Append To Array** command appends an item to a variable object. The object must be an array.
If the specified variable does not exist, it will be created.

%html.append-to-array%

**Variable Name**  
Specify the name of the variable that is an array or that you want to create. You can specify
the name of the array in an existing object.

```txt
mylist
options.list
my[0].dir.sub
```

**Value**  
Specify the value to be added. It can be multiline. By default, an object with this string will be added to the array. Also, you can specify the name of another object. The script checks if there is an object with the specified name, in which case, this object will be added to the array.

**Substitute Variable Values**  
The values of this parameter are described in the [Set Variable](set-variable.html) command.
