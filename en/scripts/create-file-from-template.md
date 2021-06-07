---
title: Create file from template
desc: The command creates a file using a text template.
img:
   create-file-from-template: scripts/create-file-from-template.png
html:
   create-file-from-template: '<img src="%img.create-file-from-template%" style="margin: 1em 1em;"/>'
---
# Create File From Template

The **Create File From Template** command creates a file from a text template.

%html.create-file-from-template%

**Template**  
Specify the template from which you want to create the file. When writing to a file, all variables in the template will be replaced with their current values. You can store the template as a file. In this case, specify the path to the template file in angle brackets.

``` txt
User: #user#
Group: #usergroup#
Status: #status#
```

**Output file**  
Specify the full or relative path to the file you want to create. If the file exists, it will be overwritten.
