---
title: Replace Variables in XLSX Template
desc: The command replaces the variables in the XLSX template.
img:
   xlsx-template: scripts/xlsx-template.png
html:
   xlsx-template: '<img src="%img.xlsx-template%" style="margin: 1em 1em;"/>'
---
# XLSX Template

The **XLSX Template** command replaces the variables in the Xlsx template (Microsoft Excel). Since the script makes all replacements in the spreadsheet itself, it does not require Microsoft Office installed. Replacements are made on all sheets of the spreadsheet.

%html.xlsx-template%

**Template (.xlsx)**.  
Specify a *xlsx* file that contains variables of the form *#varname#*. This script will replace all variables and
save a new spreadsheet with the name below.

**Output file**  
Specify the full or relative path to the document you want to create. If the file exists, it will be overwritten.
