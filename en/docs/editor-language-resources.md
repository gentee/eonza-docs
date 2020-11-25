---
title: Language Resources page in Eonza editor
desc: Documentation for Language Resources page in Eonza editor.
img:
   editor-language-1: editor-language-1.png
   editor-language-2: editor-language-2.png
   editor-language-3: editor-language-3.png
   editor-language-4: editor-language-4.png
   editor-language-5: editor-language-5.png
   editor-language-6: editor-language-6.png
html:
   editor-language-1: '<img src="%img.editor-language-1%" style="margin: 1em 1em;"/>'
   editor-language-2: '<img src="%img.editor-language-2%" style="margin: 1em 1em;"/>'
   editor-language-3: '<img src="%img.editor-language-3%" style="margin: 1em 1em;"/>'
   editor-language-4: '<img src="%img.editor-language-4%" style="margin: 1em 1em;"/>'
   editor-language-5: '<img src="%img.editor-language-5%" style="margin: 1em 1em;"/>'
   editor-language-6: '<img src="%img.editor-language-6%" style="margin: 1em 1em;"/>'
---
# Language Resources

Language resources allow you to implement multi-language support for the script. Moreover, the automatic substitution of the required language will occur both in the program interface and during the script execution. This feature is useful if you plan to make your script available to the public. Note that if the Script tab is empty, you must give unique names to resources without the *_* prefix. For example, *yourscriptname.resname*. At the time of writing this article, Eonza supported only two languages - English and Russian. So for example, let's create a script that will also support these two languages.

**Step 1.** Let's define the name of the script and the text it will output in English. If the resource is not used during the script execution, you can start its name with the symbol **_**. In this case, the compiler will skip this line.

*_hello* - Script prints Hello  
*lng.hello* - Hello, world!

%html.editor-language-1%

**Step 2.** Switch to Russian and add translations for these language resources.

%html.editor-language-2%

**Step 3.** Specify the name of the script as **#_hello#** in Settings.

%html.editor-language-3%

**Step 4.** Add the Write to Console command with **#lng.hello#** text.

%html.editor-language-4%

Now let's run our script and see the text in the current interface language. If we change the interface language in the program settings and run the script again, we will see that the script language has also changed.

%html.editor-language-5%
%html.editor-language-6%
