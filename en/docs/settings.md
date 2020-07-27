---
title: Settings tab - Eonza documentation
desc: Documentation for Settings of Eonza automation software.
img:
   settings-scripts: settings-scripts.png
   settings-personal: settings-personal.png
   settings-constants: settings-constants.png
html:
   settings-scripts: '<img src="%img.settings-scripts%" style="margin: 1em 1em;"/>'
   settings-personal: '<img src="%img.settings-personal%" style="margin: 1em 1em;"/>'
   settings-constants: '<img src="%img.settings-constants%" style="margin: 1em 1em;"/>'
---
# Settings

Here you can specify various settings for more comfortable work with the Eonza program. For the changes to the settings to take effect, you need to click on the Save button.

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

%html.settings-personal%

## Global Constants

You can define global constants that can be used in all scripts. Values ​​are substituted like variables, but a dot is added to the left of the constant name. For example, if you want to insert the value of the constant *myconst* in some script, then specify *#.myconst#*.

%html.settings-constants%
