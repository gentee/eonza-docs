---
title: Exit script
desc: The command stops running the script
img:
   exit: scripts/exit.png
html:
   exit: '<img src="%img.exit%" style="margin: 1em 1em;"/>'
---
# Exit

The **Exit**  command exits the script. When this command is invoked, the script exits gracefully regardless of the return code value. Note that this command terminates the script that was run. For example, if the *Exit* command is called in the *A* script, and you run the *B*  script and called *A* there, then the *B* script will complete its work with this command.

%html.exit%

**Exit code**  
You can specify a numeric code that the program will return when it stops working. The default value is **0**.

**Timeout (msec)**  
If you want to pause before the script exits, specify the desired timeout in milliseconds. This can be useful if you need to wait for console output or a report in the browser.
