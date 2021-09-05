---
title: Append item to hash array
desc: The script adds an item to the associative array.
img:
   append-to-map: scripts/append-to-map.png
html:
   append-to-map: '<img src="%img.append-to-map%" style="margin: 1em 1em;"/>'
---
# Append To Map

The **Append To Map** command adds an item to a variable object. The object must be an associative array.
If the specified variable does not exist, then it will be created.

%html.append-to-map%

**Variable Name**  
Specify the name of the variable that is an associative array or that you want to create. You can specify
the name of the hash array in an existing object.

```txt
mymap
options.params
mymap[0].settings.sub
```

**Key**  
Specify the key to which the value will be assigned.

**Value**  
Specify the value to be added. It can be multiline. By default, an object with this string will be added to the associative array. Also, you can specify the name of another object. The script checks if an object with the specified name exists, in which case that object will be added to the hash array.

**Substitute Variable Values**  
The values of this parameter are described in the [Set Variable](set-variable.html) command.
