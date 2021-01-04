---
title: Changelog for 2020
desc: Eonza Program Changelog for 2020
---
# Changelog for 2020

## Developer version
<!--## Beta version 1.8.0-->

* Added the [Move Files](/scripts/move-files.html) command.
* Added the [Download File](/scripts/download-file.html) command.
* Added the [Foreach Line in File](/scripts/foreach-line-file.html) command.
* Added Hash function to **Set Variable** command.
* Added *If File Exists* parameter to the **Move File** and **Rename File** commands.
* Added *Save a copy* to the *If File Exists* parameter in the **Copy File** command.
* Added *Save a copy* button in the **File Confirmation** command.
* Fixed some minor bugs.

## Version 1.9.0 - 2020/12/26

* Added *Hide Tray Icon* option in **Settings**.
* Add [Favorites](/docs/scripts.html) scripts.
* Added Favorite Scripts to the system tray icon.
* Added optional *onlyfiles* parameter to the *File List* command.
* Added the [Directory Size](/scripts/directory-size.html) command.
* Added the [Create Archive](/scripts/create-archive.html) command.
* Added the [Unpack ZIP](/scripts/unpack-zip.html) command.
* Added the [Unpack TAR.GZ](/scripts/unpack-targz.html) command.

## Version 1.8.0 - 2020/12/12

* Added tray icon with *Open in Browser* and *Shutdown* items (except MacOS).
* Added **Folder** parameter to script settings.
* Created *Standard library* folder for built-in scripts.
* If another Eonza instance is running with the same configuration file, a web page with the previously launched instance will open in the browser.
* Added *Title* parameter to **Settings**.
* Improved **Shutdown** page.

## Version 1.7.0 - 2020/12/06

* Added the [Return](/scripts/return.html) command.
* Added the [Assertions](/scripts/assertions.html) command.
* Added the [File Hash](/scripts/file-hash.html) command.
* Added the [Encrypt File](/scripts/encrypt-file.html) and [Decrypt File](/scripts/decrypt-file.html) commands.
* Added *Password* element to the [Form](/scripts/form.html) command.
* Added *Append Path*, *Filename* functions to the **Set Variable** command.

## Version 1.6.0 - 2020/11/23

* Added the [Copy Files](/scripts/copy-files.html) command.
* Added the [Delete Empty Folders](/scripts/delete-empty-folders.html) and [Delete Files](/scripts/delete-files.html) commands.
* Added the [File Confirmation](/scripts/file-confirmation.html) command.
* Added the *Exclude the mask* and *Search only the directories* parameters in the command **Foreach File**.
* Added *Split* function to the **Set Variable** command.
* Added selection of actions *If File exists* in the [Copy File](/scripts/copy-file.html) command.

## Version 1.5.0 - 2020/11/12

* Added the [Replace](/scripts/replace.html) command.
* Added the [Regex - Find](/scripts/regex-find.html) and [Regex - Replace](/scripts/regex-replace.html) commands.
* Added check of required fields in forms.
* A form for specifying parameters is shown when running a script with parameters.
* Added Length function to the command **Set Variable**.

## Version 1.4.0 - 2020/11/04

* Added work with objects in variables. You can access object fields and elements. For example, *#myobj.param#, #val[field]#, #val[#i#]#, #list[10].size#*.
* Added **File**(str) str, **SetVar**(str, obj), **GetVarObj**(str), **ResultVar**(str,obj) functions.
* Added substitution of file contents in values. For example, *&lt;/home/user/#mypath#/settings.json&gt;*.
* Added the [File List](/scripts/file-list.html), [Foreach](/scripts/foreach.html) and [Parse JSON](/scripts/parse-json.html) commands.
* Added [Split Text](/scripts/split-text.html), [Join Text](/scripts/join-text.html) commands.
* Added constants for line feed, carriage return, tab and space characters.
* Error processing on correct completion of the task has been removed.

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
