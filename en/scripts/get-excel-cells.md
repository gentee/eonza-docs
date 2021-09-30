---
title: Get the value of Excel cells
desc: The command gets the value of the cells in the XLSX file.
img:
   get-excel-cells: scripts/get-excel-cells.png
html:
   get-excel-cells: '<img src="%img.get-excel-cells%" style="margin: 1em 1em;"/>'
---
# Get Excel Cells

The **Get Excel Cells** command gets the values of the specified cells in an Excel spreadsheet and assigns them to variables.

%html.get-excel-cells%

**Excel file (*.xlsx)**  
Specify the full or relative path to the XLSX file from which you want to retrieve the cell values.

## Cells

You can specify one or more Excel cells whose values you want to retrieve.

**Sheet**  
Specify the name of the sheet in the spreadsheet. If this parameter is not specified, the values will be taken from the first sheet.

**Cell**  
Provide a cell name in the spreadsheet. For example, *A10*, *C7*, *B1*.

**Variable Name**  
The name of the variable to which the value of the specified Excel cell will be assigned.
