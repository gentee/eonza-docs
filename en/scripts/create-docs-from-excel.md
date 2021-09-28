---
title: Create documents for each Excel row
desc: The command creates documents from templates for each row in the XLSX file.
img:
   create-docs-from-excel: scripts/create-docs-from-excel.png
html:
   create-docs-from-excel: '<img src="%img.create-docs-from-excel%" style="margin: 1em 1em;"/>'
---
# Create Documents From Excel

The **Create Docs from Excel** command creates documents from templates for each row in the specified XLSX file. The document templates can be DOCX, ODS, ODT, XLSX files.

%html.create-docs-from-excel%

**Filename**  
Specify the full or relative path to the XLSX file in which you want to read each row and create documents for it. By default, the script goes through the rows in the first sheet.

**Variable Name**  
Specify the name of the variable in which the array of values of the next row will be written. The numbering starts from zero. You can use this variable object in document templates. For example, if you specified the variable name *usr*, the value *#usr[0]#* will be equal to the value of the cell in the current row in column *A*. *#usr[1]#* will be equal to the value in column *B*, etc.

**Columns**  
By default, the fields of each row are written to an array variable. But you can specify a name for each column. The names are separated by commas. In this case, the column values will be written to an associative array. If you don't specify a name for a column, it will not be available. For example, suppose we have a variable *usr* and the value of this parameter is *id,name,company*.  In this case, *#usr.id#* equals the value in column *A*, *#usr.name#* equals the value in column *B*, *#usr.company#* equals the value in column *C*. If you specify *id,name,* in this parameter only *#usr.name#* and *#usr.id#* will be defined.

**Output Directory**  
Specify the directory where the created documents will be saved. If the folder does not exist, it will be created automatically.

## Templates

You can specify one or more document templates where the variable values will be replaced and documents will be created for each record in the Excel file.

**Document Template**  
Specify the document template file in which you want to replace variables and save to the output directory. You can specify templates with DOCX, XLSX, ODT, ODS extensions. If XLSX or ODS spreadsheets are specified as a template, variables will be replaced on all sheets.

**Filename Pattern**  
Specify a template for a document name without an extension. Here, among other things, you can specify values from an Excel spreadsheet. For example, let the variable name to get the value is *usr* and a column named *name* is defined. In this case, if you specify *#usr.name#* here, the name of the created document will be equal to the user name (John Doe.docx). If this parameter is not specified, all documents will be saved with the same name as the document template name. Note that in this case, as well as when a document with the same name already exists, a suffix will be added to the file name - *pattern (1).docx*, *pattern (2).docx* etc. Thus, in any case, all documents will be created for all rows in the Excel file.
