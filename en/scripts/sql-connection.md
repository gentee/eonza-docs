---
title: Establish a connection to the SQL server
desc: The command establishes a connection to the SQL server.
img:
   sql-connection: scripts/sql-connection.png
html:
   sql-connection: '<img src="%img.sql-connection%" style="margin: 1em 1em;"/>'
---
# SQL Connection

The **SQL Сonnection** command establishes a connection to the SQL server and saves the connection ID in a variable.

%html.sql-connection%

**SQL Server**  
Select the type of SQL server - *MySQL* or *PostgreSQL*.

**Host**  
Specify the host of SQL server you want to connect to. If not specified, *localhost* will be used.

``` txt
localhost
127.0.0.1
```

**Port**  
Specify the port for connecting to the SQL server. If not specified, then *3306* port for *MySQL* and *5432* port for *PostreSQL* will be used.

**User name**  
Provide a username to connect to the server.

**Password**  
Password to connect to the server. For security reasons, do not specify it explicitly.

**Database Name**  
Specify the database name.

**Result Variable**  
Specify the name of the variable to which the connection identifier will be assigned. Use this name in the **SQL connection** field in other commands for working with the database.
