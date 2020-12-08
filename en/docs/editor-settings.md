---
title: Settings page in Eonza editor
desc: Documentation for Settings page in Eonza editor.
img:
   editor-settings: editor-settings.png
html:
   editor-settings: '<img src="%img.editor-settings%" style="margin: 1em 1em;"/>'
---
# Settings

Let's consider the general settings of the script.

%html.editor-settings%

* **Name** - the system name of the script. It cannot be changed if the script is already used in other scripts.
* **Title** - script name, which will be displayed everywhere, where the script will be used.
* **Description** - a short description of what the script does.
* **Folder** - you can specify a folder name for the script. The folders will be automatically displayed in the general list of scripts. You can specify any nesting of folders using the **/** separator. For example, *My Folder*, *Work/Archive*.
* **Log Level** - log level, which is set by default when launching the script. If you specify *Information*, the call of this script with parameters will be automatically displayed in the log, if the log level allows it.
* **Unrunnable Script** - if you check this checkbox, the script cannot be launched. In this case it can only be called from other scripts.
