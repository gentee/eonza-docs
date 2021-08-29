---
title: Replace Variables in DOCX Template
desc: The command replaces the variables in the DOCX template.
img:
   docx-template: scripts/docx-template.png
html:
   docx-template: '<img src="%img.docx-template%" style="margin: 1em 1em;"/>'
---
# Docx Template

The **Docx Template** command replaces variables in the Docx template (Microsoft Word). Since the script makes all replacements in the document itself, it does not require MS Office installed. If the command does not replace some variables in the template, you need to copy them separately (*#varname#*) from a regular text editor and paste them into the document. This is because Microsoft Word can split the variable name into invisible fragments, which the script cannot process as a whole.

%html.docx-template%

**Template (.docx)**  
Specify a *docx* file that contains variables of the form *#varname#*. This script will replace all variables and
save a new document with the name below.

**Output file**  
Specify the full or relative path to the document you want to create. If the file exists, it will be overwritten.
