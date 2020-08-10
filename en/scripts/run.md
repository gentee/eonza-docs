---
title: Run application with parameters
desc: The command starts the application with parameters and can wait for its completion.
img:
   run: scripts/run.png
html:
   run: '<img src="%img.run%" style="margin: 1em 1em;"/>'
---
# Run Application

The **Run Application** launches the specified application. The script allows you to pass the necessary parameters and wait for the running program to finish.

%html.run%

**File name**  
Specify the full or relative path to the program you want to run.

**Command line parameters**  
You can specify command line parameters for the program to be launched. You can specify parameters in several lines.

**Wait until application finishes**  
Check this checkbox if you want to wait until the running application finishes. Otherwise, the next command will be executed immediately after calling the program, without waiting for the end of its work.
