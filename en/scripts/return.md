---
title: Return from the current script
desc: The command returns control from the current script.
img:
   return: scripts/return.png
html:
   return: '<img src="%img.return%" style="margin: 1em 1em;"/>'
---
# Return

The **Return** command returns control from the current script to the parent script.

%html.return%

**Result Variable**  
You can specify the name of the resulting variable that will be returned to the parent script. In this case, it is recommended to get the name of the resulting variable in the script parameters. Otherwise, you can break the parent script if you change the value of the variable with the same name there.

**Value**  
The value for the resulting variable.
