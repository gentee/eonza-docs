---
title: Set the log level
desc: The command sets the script log level.
img:
   set-log-level: scripts/set-log-level.png
   sample-2: scripts/sample-2.png
html:
   set-log-level: '<img src="%img.set-log-level%" style="margin: 1em 1em;"/>'
   sample-2: '<img src="%img.sample-2%" style="margin: 1em 1em;"/>'
---
# Set Log Level

The **Set Log Level** command changes the current log level in the running script. For example, if the command [Log Output] (log-output.html) is called with a log level greater than the current level, then such record will be skipped.

%html.set-log-level%

**Log Level**  
Specify a new level for logging. All levels are listed below in ascending order.

* **Disabled**. Logging out is disabled.
* **Error**. Only error messages are logged.
* **Warning**. Only error messages and warnings are logged.
* **Form data**. Only error messages, warnings and values obtained from forms are saved in the log.
* **Information**. Errors, warnings, form data and information are saved in the log.
* **Debug**. All types of log records are logged. Also, all data about calls of command/script with their parameters are saved in the log.


[%dwnsample%](/samples/sample-2.yaml).

%scriptresult%

%html.sample-2%
