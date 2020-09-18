---
title: Editor tab - - Eonza documentation
desc: Documentation for Editor tab of Eonza automation software.
img:
   editor: editor.png
html:
   editor: '<img src="%img.editor%" style="margin: 1em 1em;"/>'
---
# Editor

The editor allows you to create and edit scripts. Each script has different parameters, which are divided into five tabs.

* [**Script**](editor-script.html) allows you to describe the sequence of commands that will be executed when the script is run. Each command is a call to another script with the necessary parameters.
* [**Settings**](editor-settings.html) are used to specify general information about the script.
* [**Parameters**](editor-parameters.html) allows you to define the list of input parameters, which can be defined when calling this script from other scripts.
* [**Language resources**](editor-language-resources.html) allows you to implement multilingual support when using a script.
* [**Source code**](editor-source-code.html) allows to use all features of [Gentee programming language](https://github.com/gentee/gentee/) for solving complex tasks.
* [**Compile**](editor-compile.html) - this tab is shown on request and allows you to view the generated code and compilation result without running the script.

## Top menu

Let's consider the items of the top menu.

%html.editor%

* **History** - allows you to quickly jump to scripts that were recently opened in the editor.
* **Save** - saves all changes made to the script.
* **Save as** - saves the script under a different system name. This item is available when you have changed the script name in its settings. For example, it can be useful for creating modified embedded scripts that cannot be changed.
* **Run** - starts the current script. If the script has not been saved, its previous version will be launched.

The following items are in the drop-down menu.

* **Import** - loads the script from the text *yaml* file.
* **Export** - saves the current script as a text *yaml* file.
* **Compile** - opens the corresponding tab with the generated Gentee code and the result of its compilation.
* **Run Silently** - starts the current script without opening a bookmark in the browser.
* **Delete** - deletes the current script. The script cannot be deleted if it is used in other scripts. Also, embedded scripts cannot be removed.
