---
title: Settings tab - Eonza documentation
desc: Documentation for Settings of Eonza automation software.
img:
   settings-scripts: settings-scripts.png
   settings-personal: settings-personal.png
   settings-constants: settings-constants.png
   settings-security: settings-security.png
   settings-general: settings-general.png
   settings-general-2: settings-general-2.png
   logout: logout.png
html:
   settings-scripts: '<img src="%img.settings-scripts%" style="margin: 1em 1em;"/>'
   settings-personal: '<img src="%img.settings-personal%" style="margin: 1em 1em;"/>'
   settings-constants: '<img src="%img.settings-constants%" style="margin: 1em 1em;"/>'
   settings-security: '<img src="%img.settings-security%" style="margin: 1em 1em;"/>'
   settings-general: '<img src="%img.settings-general%" style="margin: 1em 1em;"/>'
   settings-general-2: '<img src="%img.settings-general-2%" style="margin: 1em 1em;"/>'
   logout: '<img src="%img.logout%" style="margin: 1em 1em;"/>'
---
# Settings

Here you can specify various settings for more comfortable work with the Eonza program. For the changes to the settings to take effect, you need to click on the Save button.

## General

**Title**  
You can provide your own title for the Eonza program. This can be useful if you use more than one Eonza installation.

%html.settings-general%

**Hide Tray Icon**  
This option is available if your version of Eonza supports displaying a menu icon in the system tray. Check this checkbox if you want to disable the creation of a system tray icon.

**Automatic check for updates**  
You can specify the frequency with which you want to check for new versions of the program. You will be notified if a new version is found. Also, you can check for updates at any time in the *Help* tab.

### Task Manager

Task Manager settings. The program periodically deletes old tasks. Here you can specify
parameters for automatic deletion. Eonza does not delete locked tasks.

**Remove automatically after X days**  
Specify the number of days after which a completed task can be deleted.

**Maximum number of tasks**  
Specify the maximum number of tasks to be stored.

**Hide duplicate tasks**  
Check this checkbox if you want to hide duplicate tasks in the Task Manager. In this case, if there are several tasks with the same script name, status and user, then only the most recent completed task will be shown in the list. Locked and unfinished tasks are always shown. 

%html.settings-general-2%

## Scripts

**Include Source Code**  
When running the script, the program generates a program in the [Gentee script programming language](https://docs.gentee.org/) from the script and compiles it into bytecode. After that, it sends this bytecode for execution. If you want to be able to see the generated Gentee source code, please check this checkbox. In this case, the source code will be available both at runtime and after the script is finished. This feature may be useful in case errors occur during the script execution.

**Log Level**  
Specify the default log level for all running scripts.

%html.settings-scripts%

## Personal

The page with personal settings.

**Language**  
You can specify your preferred language of the program interface and the scripts being executed.

**Forms Alignment**  
By default, all forms in scripts are aligned to the left edge. Here you can specify that forms are aligned to the center of the window in the browser.

%html.settings-personal%

## Global Constants

You can define global constants that can be used in all scripts. Values ​​are substituted like variables, but a dot is added to the left of the constant name. For example, if you want to insert the value of the constant *myconst* in some script, then specify *#.myconst#*. Do not use names for constants that have already been used for [predefined constants](constants.html).

%html.settings-constants%

## Security

Here you can find the settings that will help protect against unauthorized access to the program. You can set a password to connect to Eonza. The program does not explicitly store the password, so a lost password cannot be recovered. In this case, you can [reset password](restore-password.html) using the command line parameter.

**Current password**  
If you want to set a new password, then you need to specify the current password. If there is no password, then this field is hidden.

**Password**  
Specify a password to access the program. If you want to disable login by password, specify *Current password*, and leave this option blank.

**Don't ask for password on startup**.  
By default, when starting the program, the user must re-enter the password in the browser. Click this checkbox if you do not want to enter the password after each launch. Note that if you check this checkbox, you will still have to enter the password once at the next launch.

%html.settings-security%

To log out the program, select *Log Out* in the drop-down menu in the upper right corner. In this case, the logout will be performed for all connected devices and browsers.

%html.logout%
