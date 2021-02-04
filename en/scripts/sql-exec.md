---
title: Execute SQL statements
desc: The command executes SQL statements.
img:
   sql-exec: scripts/sql-exec.png
html:
   sql-exec: '<img src="%img.sql-exec%" style="margin: 1em 1em;"/>'
---
# SQL Exec

Command **SQL Exec** executes SQL statements.

%html.sql-exec%

**SQL Connection**  
Provide a variable name with the SQL connection identifier. This variable must be defined in the [SQL Connection](sql-connection.html) command.

**SQL Statements**  
Specify the SQL statements to be executed. If you want to specify several SQL statements, separate them with comments starting with *#* or *--*.

``` sql
DROP TABLE IF EXISTS `#dbtable#`;
-- comment
CREATE TABLE #dbtable# ( id INT PRIMARY KEY AUTO_INCREMENT, 
     name VARCHAR(255), count INT, flag BOOLEAN);
```

**Parameters**  
It is recommended to use parameters when using values in a SQL query. If you have more than one SQL query specified, the parameters will be applied to the last SQL query.

For example, you need to add two parameters when using any of these queries. You can use variable substitution *#varname#* in parameters.

``` sql
INSERT INTO `#dbtable#` (name, count, flag) VALUES(?, ?, TRUE); # mysql 
INSERT INTO "#dbtable#" (id, name, count, flag) VALUES(1, $1, $2, TRUE); # postgresql
```

``` txt
#name# (#id#)
#icount#
```
