---
title: Merge text or lines
desc: The command combines array elements and assigns the result to a variable.
img:
   join-text: scripts/join-text.png
html:
   join-text: '<img src="%img.join-text%" style="margin: 1em 1em;"/>'
---
# Join Text

The **Join Text** command joins all elements of the array into one text and assigns the result to the variable.

%html.join-text%

**Variable Name**  
Specify the object variable name. This object must be an array. The command converts each element of the array to a string and concatenates them into one string.

**Delimiter**  
You can specify a string to be inserted between the elements in the resulting line. For a line feed, specify *#.n#*, for a space, specify *#.s#*.

**Result Variable**  
Specify the name of the variable to which the result will be assigned.
