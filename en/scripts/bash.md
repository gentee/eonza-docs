---
title: Execute bash script
desc: The command executes the specified bash script.
img:
   bash: scripts/bash.png
html:
   bash: '<img src="%img.bash%" style="margin: 1em 1em;"/>'
---
# Bash

The **Bash** command executes the specified bash script. You must specify the script text, not the path to the bash file. The next command will be executed after the script finishes.

%html.bash%

**Bash Script**  
Specify the Bash script code that you want to execute.

**sudo Password**  
You can provide a sudo password if you want to run the script as superuser. Do not explicitly enter your password. It is better to define the corresponding value in the Secure Storage of the Pro version and specify the value name here (for example, #@rootpsw#). You can also request a password using the [Form](form.html) command and specify the appropriate variable name here (for example, #rootpsw#). In this case, the password will not be available to third parties.
