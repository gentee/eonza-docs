---
title: Write To Log
desc: The script writes a line to the log.
img:
   log-output: scripts/log-output.png
   sample-2: scripts/sample-2.png
html:
   log-output: '<img src="%img.log-output%" style="margin: 1em 1em;"/>'
   sample-2: '<img src="%img.sample-2%" style="margin: 1em 1em;"/>'
---
# Log Output

The **Log Output** command saves the specified line in the log.

%html.log-output%

**Log Level**  
Specify the type of value to be written. If the current log level is less than the specified one, then this command will be ignored and nothing will be logged. The log level can be changed using the [Set Log Level](set-log-level.html) command.

**Text**  
Specify the text to be written to the log.

* [%dwnsample%](/samples/sample-2.yaml)

%scriptresult%

%html.sample-2%
