---
title: Perform an action for each line in the CSV file
desc: The command executes nested commands for each line in the CSV file.
img:
   foreach-line-csv: scripts/foreach-line-csv.png
html:
   foreach-line-csv: '<img src="%img.foreach-line-csv%" style="margin: 1em 1em;"/>'
---
# Foreach Line in CSV

The command **Foreach Line in CSV** executes nested commands for each line in the specified CSV file.

%html.foreach-line-csv%

**File Name**  
Specify the full or relative path to the CSV file in which you want to read each line and execute nested commands.

**Variable Name**  
Specify the name of a variable in which an array of values of the next line will be written. You can use this variable object in nested commands.

**Delimiter**  
By default, a comma is considered the separator between values in a record. You can specify another delimiter that is used in the specified CSV file. For example, **;**.

**Columns**  
By default, the fields of each row are written to an array variable. But you can specify a name for each column. The names are separated by commas. In this case, the column values ​​will be written to the associative array (map). If you do not specify a name for a column, then it will not be available. For example, let's say we have the *csvline* variable and the following CSV file:

``` txt
"Robert","Google",1200
"John Dow, "My Company, Inc.",3600
Alex 1,Private Company,4800
```

If the *Columns* field is empty the output of *#csvline[0]# = #csvline[2]#* value for each row will give the following result:

``` txt
Robert = 1200
John Dow = 3600
Alex 1 = 4800
```

If we define the *Columns* field as *name,,value*, we get the same result for the value *#csvline.name# = #csvline.value#*.
