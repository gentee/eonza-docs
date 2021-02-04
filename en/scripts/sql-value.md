---
title: Execute an SQL query and get the value of the column
desc: The command executes an SQL query and stores the column value in a variable.
img:
   sql-value: scripts/sql-value.png
html:
   sql-value: '<img src="%img.sql-value%" style="margin: 1em 1em;"/>'
---
# SQL Value

**1.12.0**  
The **SQL Value** command executes an SQL query to select data and writes the value of the first column of the first record found into a variable.

%html.sql-value%

**SQL connection**  
Specify the name of the variable with the SQL connection identifier. This variable must be defined in [SQL Connection](sql-connection.html) command.

**SELECT Statement**  
Specify an SQL SELECT query to retrieve a column from the database. If the query finds multiple records, the value of the first column of the first record will be returned. If the query finds no records, an error will be returned.

``` sql
select count(*) from #dbtable#
```

**Parameters**.  
It is recommended to use parameters when using values ​​in an SQL query.

For example, you need to add one parameter when using this query. You can use *#varname#* variable substitution in parameter values.

``` sql
select company from #dbtable# where code = ?
```

``` txt
#code#
```

**Resulting variable**.  
Specify the name of the variable to which the resulting value will be assigned. If the query returns a record with multiple columns, the value of the first column will be returned.

``` txt
#myname#
```
