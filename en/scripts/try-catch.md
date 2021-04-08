---
title: Catch the error that occurred while executing the script
desc: The command catches the encountered error and offers to repeat the actions or continue the script execution.
img:
   try-catch: scripts/try-catch.png
   try-catch-form: scripts/try-catch-form.png
html:
   try-catch: '<img src="%img.try-catch%" style="margin: 1em 1em;"/>'
   try-catch-form: '<img src="%img.try-catch-form%" style="margin: 1em 1em;"/>'
---
# Try / Catch

**v1.17.0**  
By default, the script terminates when an error occurs. If you want to repeat some actions or ignore the error, then use the **Try / Catch** command. If an error occurs in any of the nested commands, then you will see a message with the error text and you can choose one of three options:

* **Retry** - start repeated execution from the first nested script.
* **Abort** - abort the execution of the current script.
* **Ignore** - continue script execution from the command that follows the *Try / Catch* command. In this case, all nested commands below the command in which the error occurred will be skipped.

%html.try-catch%

**Title of Error Message**  
Specify the text to be displayed above the error text.

%html.try-catch-form%
