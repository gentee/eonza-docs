---
title: Execute actions for each row in the XLSX file
desc: The command executes nested commands for each row in the XLSX file.
img:
   foreach-xlsx: scripts/foreach-xlsx.png
html:
   foreach-xlsx: '<img src="%img.foreach-xlsx%" style="margin: 1em 1em;"/>'
---
# Foreach Row in XLSX

The **Foreach Row in XLSX** command executes nested commands for each row in the specified XLSX file.

%html.foreach-xlsx%

**File Name**  
Specify the full or relative path to the XLSX file in which you want to read each row and execute nested commands.

**Variable Name**  
Specify the name of the variable in which the array of values of the next row will be written. Numbering starts at zero. You can use this variable object in nested commands. For example, if you specified the variable name *val*, the value *#val[0]#* will be equal to the cell value in the current row in *A* column. *#val[1]#* will be equal to the value in column *B*, etc.

**Columns**  
By default, the fields of each row are written to an array variable. But you can specify a name for each column. The names are separated by commas. In this case, the column values will be written to an associative array. If you don't specify a name for a column, it will not be available. For example, suppose we have the variable *val* and the value of this parameter is *name,company,id*. In this case, *#val.name#* equals the value in the *A* column, *#val.company#* equals the value in the *B* column, *#val.id#* equals the value in the *C* column. If you specify *name,,id* in this parameter then only *#val.name#* and *#val.id#* values will be defined.

**Sheet name**  
By default, the script goes through the rows in the first sheet. You can specify a different sheet name where you need
to perform actions for each row.
