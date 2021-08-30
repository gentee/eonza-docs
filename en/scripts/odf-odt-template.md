---
title: Replace Variables in ODF/ODT Template
desc: The command replaces the variables in the ODF/ODT template.
img:
   odf-odt-template: scripts/odf-odt-template.png
html:
   odf-odt-template: '<img src="%img.odf-odt-template%" style="margin: 1em 1em;"/>'
---
# ODT Template

The **ODT Template** command replaces variables in the Odt template (LibreOffice Writer). Since the script makes all replacements in the document itself, it does not require Libre Office installed. If the command does not replace some variables in the template, you need to copy them separately (*#varname#*) from a regular text editor and paste them into the document. This is because LibreOffice Writer can split the variable name into invisible fragments, which the script cannot process as a whole.

%html.odf-odt-template%

**Template (.odt)**  
Specify a *odt* file that contains variables of the form *#varname#*. This script will replace all variables and
save a new document with the name below.

**Output file**  
Specify the full or relative path to the document you want to create. If the file exists, it will be overwritten.
