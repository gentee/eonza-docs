---
title: Run script
desc: The command runs the script as a separate process and continues the current script.
img:
   run-script: scripts/run-script.png
html:
   run-script: '<img src="%img.run-script%" style="margin: 1em 1em;"/>'
---
# Run Script

The **Run Script** command runs the specified script as a separate process and continues running the current script.

%html.run-script%

**Script**  
Specify the system name of the script you want to run.

**Attached Data**  
You can specify any text that will be assigned to the **data** predefined constant in the running script.

``` yaml
str: Test message
val: 12345
path: /home/user/eonza
```

**Run Silently**  
Check this checkbox if you do not want to open the running script in the browser.
