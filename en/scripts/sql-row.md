---
title: Execute an SQL query and get a record
desc: The command executes an SQL query and stores the first record in a variable.
img:
   sql-row: scripts/sql-row.png
html:
   sql-row: '<img src="%img.sql-row%" style="margin: 1em 1em;"/>'
---
# SQL Row

**1.12.0**  
The **SQL Row** command executes an SQL query to select data and writes the first record found to an object variable.

%html.sql-row%

**SQL Connection**  
Provide a variable name with the SQL connection identifier. This variable must be defined in the [SQL Connection](sql-connection.html) command.

**SELECT Statement**  
Specify an SQL SELECT query to retrieve a record from the database. If the query finds more than one record, the first record is returned. If the query finds no records, an error will be returned.

``` sql
select * from #dbtable# where id=1
```

**Parameters**.  
It is recommended to use parameters when using values ​​in an SQL query.

For example, you need to add one parameter when using this query. You can use *#varname#* variable substitution in parameter values.

``` sql
select * from #dbtable# where iduser = ?
```

``` txt
#iduser#
```

**Result Variable**  
Specify the name of the variable to which the resulting associative array with column values ​​will be saved.

``` txt
#item.name#
#myrec.count#
```
