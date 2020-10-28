---
title: Changelog for 2020
desc: Eonza Program Changelog for 2020
---
# Changelog for 2020

## Beta version 1.4.0

* Added work with objects in variables. You can access object fields and elements. For example, *#myobj.param#, #val[field]#, #val[#i#]#, #list[10].size#*.
* Added **File**(str) str, **SetVar**(str, obj), **GetVarObj**(str), **ResultVar**(str,obj) functions.
* Added substitution of file contents in values. For example, *</home/user/#mypath#/settings.json>*.
* Added the [File List](/scripts/file-list.html) and [Foreach](/scripts/foreach.html) commands.

## Version 1.3.0 - 2020/10/27

* Added the [Set Environment](/scripts/set-environment.html) script to set the environment variables.
* Added comparisons *Environment Exists* and *RegEx Match* in **If Statement** and **While Statement** commands.
* Ask to save the modified script at Run, Export and Compile in the Editor.
* Added functions (Absolute Path, Append, Upper case, Lower case, Substring, Current Time, Get Environment Variable) to the [Set Variable](/scripts/set-variable.html) command.
* Added progress bar when copying large files in the command **Copy File**.

## Version 1.2.0 - 2020/10/08

* Added command line parameter -install.
* Added a whitelist of IP addresses to the configuration file.
* Added a limit on the number of simultaneously running scripts in Playground mode.
* Added IP check when accessing a running task in a browser.
* Added the [Create directory](/scripts/create-dir.html) script.
* Added comparison *File Exists* in [If Statement](/scripts/if-statement.html) and [While Statement](/scripts/while-statement.html).

## Version 1.1.0 - 2020/09/28

* Added the [Get Web Page](/scripts/get-webpage.html) script.
* Added **host** parameter to config file.
* Added [Playground](playground.html) mode.
* The option **develop** in the configuration file has been replaced by **mode** (default, develop, playground).
* Fixed HTML output in the Console tab.
* Fixed a bug with the checkbox element type in the Form command.

## Version 1.0.0 - 2020/09/18

First release.