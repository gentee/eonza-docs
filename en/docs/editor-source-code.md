---
title: Source Code page in Eonza editor
desc: Documentation for Source Code page in Eonza editor.
img:
   editor-source-code: editor-source-code.png
   editor-source-1: editor-source-1.png
   editor-source-2: editor-source-2.png
html:
   editor-source-code: '<img src="%img.editor-source-code%" style="margin: 1em 1em;"/>'
   editor-source-1: '<img src="%img.editor-source-1%" style="margin: 1em 1em;"/>'
   editor-source-2: '<img src="%img.editor-source-2%" style="margin: 1em 1em;"/>'
---
# Source Code

The easiest way to create a script is to add the necessary commands to the [Script tab](editor-script.html), but you can also use the [Gentee script language](https://docs.gentee.org/) to implement more complex calculations and actions. Here you can use both language constructions and all functions of its standard library. If you have specified [parameters](editor-parameters.html) for the script, you can use variables with the same names and corresponding types. Note that you cannot define types, constants, functions, etc. here. Anything you specify here will be inserted into the body of the script function. This code will be executed before executing the commands that are defined in the *Script* tab.

%html.editor-source-code%

Let's consider an example of a simple script to output a string to the console.

**Step 1.** Let's define a parameter with the name *text* and type *Single line text*. This parameter will have the *str* type in the source code. Thus, we can immediately use it in the standard *Println* function.

%html.editor-source-1%

**Step 2.** Insert the *Println* call into the Source code.

``` go
Println( text )
```

**Step 3.** Specify the script name in the Settings and save it under the name *My Console*. After that, we can use this script in other scripts.

%html.editor-source-2%
