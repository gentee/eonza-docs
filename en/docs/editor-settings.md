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
* **Log Level** - [log level](logging.html), which is set by default the script is run. The current logging level will be restored after the script ends. For example, if you specify *Information*, the log will automatically record execution of nested scripts.
* **Unrunnable Script** - if you check this checkbox, the script cannot be launched. In this case it can only be called from other scripts.
