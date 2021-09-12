---
title: The script fills in the form fields on the web page
desc: The command fills in form fields on a web page when launched from a browser extension.
img:
   fill-in-form: scripts/fill-in-form.png
   silent-ext: scripts/silent-ext.png
html:
   fill-in-form: '<img src="%img.fill-in-form%" style="margin: 1em 1em;"/>'
   silent-ext: '<img src="%img.silent-ext%" style="margin: 1em 1em;"/>'
---
# Fill in Form

The **Fill in Form** command assigns the specified values to HTML elements according to their **id** identifier or **name** attribute. You can use this command in scripts, which run in [Eonza extension](/docs/chrome-extension.html) for the Chrome browser. If your script uses this command, run it in the extension in hidden mode so that the browser does not switch to a new tab.

%html.silent-ext%

**URL**  
Specify the URL where you want the form to be filled out. If the address ends with an '*', then the forms will fill in on all web pages that begin with the specified line. Otherwise, the form will fill out only on the specified page.

Because this command is executed only on specific pages, you can add many such commands to one script for different web pages. In this case, when you run your script in a browser extension, the script will compare the address of the current web page with all **Fill in Form** commands and substitute values that match the current URL.

%html.fill-in-form%

## List of input elements

Add to this list the IDs or names of the HTML controls you want to fill in.

**ID or name of HTML element**  
Specify the name of the **id** identifier or **name** attribute of the HTML element in which you want to substitute a value. If the web page has several elements with the specified **name** attribute, the value will be pasted into the first element found.

**Value**  
Specify the value that you want to assign to this HTML element. If you want to insert passwords and other secret information, it is recommended to use the [secure storage](/docs/pro-storage.html) of Pro version.
