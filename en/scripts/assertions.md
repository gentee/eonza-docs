---
title: Check assertions for truth
desc: The command checks if the statements are true and displays an error if the value is false.
img:
   assertions: scripts/assertions.png
html:
   assertions: '<img src="%img.assertions%" style="margin: 1em 1em;"/>'
---
# Assertions

The **Assertions** command checks if the specified assertions are true. If at least one of the conditions is false, then the command terminates the script with an error. First of all, this script is intended for use in test scripts.

%html.assertions%

**Error message**  
You can provide your own error message that will be shown when any statement is false. By default, the error text is *Assertion failed*.

## Assertions

Specify a list of conditions to be checked. The parameters of the conditions are defined in the same way as in the [If Statement](/scripts/if-statement.html) command.
