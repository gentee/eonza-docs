---
title: Execute SQL query and get data
desc: The command executes the SQL query and stores the received data into a variable.
img:
   sql-query: scripts/sql-query.png
html:
   sql-query: '<img src="%img.sql-query%" style="margin: 1em 1em;"/>'
---
# SQL Query

The **SQL Query** command executes an SQL query to select data and writes the received data to an object variable.

%html.sql-query%

**SQL Connection**  
Provide a variable name with the SQL connection identifier. This variable must be defined in the [SQL Connection](sql-connection.html) command.

**SELECT Statement**  
Specify an SQL SELECT query to retrieve records from the database.

``` sql
select * from #dbtable# order by id
```

**Parameters**.  
It is recommended to use parameters when using values in an SQL query.

For example, you need to add one parameter when using this query. You can use *#varname#* variable substitution in parameter values.

``` sql
select * from #dbtable# where iduser = ? order by id
```

``` txt
#iduser#
```

**Result Variable**.  
Specify the name of the variable in which the resulting array of records will be saved. A variable is an object in which each element of the array is an associative array with column values. Subsequently, you can use the [Foreach](foreach.html) command  to iterate over all the received records or substitute specific values.

``` txt.
#list[0].name#
#mylist[#index#].count#
```
