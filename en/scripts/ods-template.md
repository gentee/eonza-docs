---
title: Replace Variables in ODS Template
desc: The command replaces the variables in the ODS template.
img:
   ods-template: scripts/ods-template.png
html:
   ods-template: '<img src="%img.ods-template%" style="margin: 1em 1em;"/>'
---
# ODS Template

**v1.21.0**  
The **ODS Template** command replaces the variables in the Ods template (LibreOffice Calc). Since the script makes all replacements in the spreadsheet itself, it does not require Libre Office installed. Replacements are made on all sheets of the spreadsheet.

%html.ods-template%

**Template (.ods)**.  
Specify a *ods* file that contains variables of the form *#varname#*. This script will replace all variables and
save a new spreadsheet with the name below.

**Output file**  
Specify the full or relative path to the document you want to create. If the file exists, it will be overwritten.
