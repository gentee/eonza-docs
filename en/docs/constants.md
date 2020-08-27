---
title: Predefined constants in scripts
desc: Constants defined when running the script 
img:
   constants: constants.png
html:
   constants: '<img src="%img.constants%" style="margin: 1em 1em;"/>'
---
# Predefined constants

When you run the script, the following constants are automatically created.

Name | Description
------------|------------
**apppath** | The directory where the Eonza program is located.
**os** | Operating system. For example *linux, windows, darwin*.
**temppath** | Directory for temporary files.

In addition, the following constants are created:

* All [language resources](https://github.com/gentee/eonza-assets/blob/master/languages/en.yaml) of the Eonza program.
* [Global constants](settings.html), which are specified in the program settings.

When accessing the constants, you have to put a dot before the name.

``` txt
Eonza Path = #.apppath#
Temp Path = #.temppath#
Eonza Language Resource (cancel) = #.cancel#  
OS = #.os#
My Global Constant (myname) = #.myname#
```

%html.constants%
