---
title: Append text to the variable value
desc: The script adds text to the value of the specified variable.
img:
   append-to-variable: scripts/append-to-variable.png
html:
   append-to-variable: '<img src="%img.append-to-variable%" style="margin: 1em 1em;"/>'
---
# Append To Variable

The **Append to Variable** command adds text to the value of the variable. If the specified variable does not exist, it will be created.

%html.append-to-variable%

**Variable Name**  
Specify the name of the variable to which you want to add text.

**Delimiter**  
You can specify a delimiter to be added before the added text. The delimiter is not added if the variable does not exist, it is equal to the empty string, or the current value ends with this separator.

```txt
#.r##.n# - the \r\n (0xD 0xA) delimiter.
#.s# - a space delimiter.
```

**Value**  
Specify the value to be appended. It may be multiline. 

**Substitute Variable Values**  
The values of this parameter are described in the [Set Variable](set-variable.html) command.
