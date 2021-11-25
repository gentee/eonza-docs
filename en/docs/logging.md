---
title: Script Logging
desc: How logging occurs when the script is running
img:
   common-settings: common-settings.png
html:
   common-settings: '<img src="%img.common-settings%" style="margin: 1em 1em;"/>'
---
# Logging

You can log all the actions a script performs while it is running. At the start of the script a variable is created that defines the current logging level. By default, it is assigned the logging level defined in the *Log Level* field on the [Settings - Scripts](settings.html) page. All log entries are available during script execution (in the Log tab). If the task has already been completed, but you can view the log in the Task Manager. 

There are the following logging levels

* **DISABLE** - logging is disabled;
* **ERROR** - only errors are logged;
* **WARN** - logs errors and warnings;
* **FORM** - data specified in forms, errors and warnings are logged;
* **INFO** - logs information messages, form fields, errors and warnings;
* **DEBUG** - logs debug messages and **INFO** level messages;
* **INHERIT** - the logging level doesn't change. It is inherited from the parent script.

When you run a script, or it starts from another script, a record with the parameters is saved with the level **INFO**. If the current level is higher in the list of logging levels, this information will not go into the log. After that, the current logging level is saved and the logging level specified in [Script settings](editor-settings.html) is set before the script code is executed. If you select *Inherit* there, the log level is not changed. The previous logging level will be restored after this script ends.

If you want to specify a log level that differs from the current value in the script settings when you call the script, specify it in [Common Settings - Advanced settings](common-settings.html) with the field name **log**. For example, the script's log level is **WARN**. In this case you will not see what commands this script executes. Specify 

```yaml
log: INFO
```

and this information will be saved in the log. The name of the logging level can be specified in any case.

%html.common-settings%

As mentioned above, only script launch is automatically logged (with the **INFO** logging level). Use the [Log Output](/scripts/log-output.html) command to log something yourself. In addition, you can call the [Set Log Level](/scripts/set-log-level.html) command to change the log level.