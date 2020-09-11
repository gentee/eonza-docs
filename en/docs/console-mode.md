---
title: Running scripts from the console
desc: How to run Eonza scripts in the terminal.
img:
   console-mode: console-mode.png
html:
   console-mode: '<img src="%img.console-mode%" style="margin: 1em 1em;"/>'
---
# How to run scripts from the console

Although you need a browser to work with Eonza, you can run scripts directly from the console. In this case, all console input and output will also be in the current console. If the script uses [Forms](/scripts/form.html) or [Messages](/scripts/message.html), they will be displayed in the browser. Note that even if you run the script from the console, you can view its status and log in [Task manager](task-manager.html) at any time. The following is a sequence of steps to enable the console mode.

## Step 1: Copy the executable file

Copy the Eonza executable file to any directory that is specified in the **PATH** environment variable. In this case you will not need to specify the path to the Eonza program. For example, for *Linux* this could be the directory **/usr/local/bin**.

## Step 2: Rename the copied file

You should now rename the copied file so that its name starts with **ez**. You can simply rename it to *ez*. For checking, run this file in any directory. You should get the message like this *Usage: ez &lt;scriptname&gt;*.

## Step 3. Run the script

If you have changed the default port in the [configuration file](config.html) then you also need to add the global environment variable **EZPORT** and assign it the appropriate port.

``` txt
EZPORT="3300"
```

To run the script you need to specify the name of this script as a parameter, which is defined in the field [Settings - Name](editor-settings.html). It is also necessary that the Eonza program is running at that moment.

%html.console-mode%
