---
title: Get values from INI file
desc: The command retrieves one or more values from an INI file.
img:
   read-ini-values: scripts/read-ini-values.png
html:
   read-ini-values: '<img src="%img.read-ini-values%" style="margin: 1em 1em;"/>'
---
# Read INI Values

The command **Read INI Values** retrieves one or more values from the specified section of the INI file.

%html.read-ini-values%

**Filename**  
Full or relative name of the INI file.

**Section**  
Section name.

## Keys

Specify the keys whose values you want to read.

**Key Name**  
The name of the key to be retrieved.

**Variable Name**  
The name of the variable that will be assigned a value.

**Default Value**  
By default, if the specified key does not exist, an error is returned. If you specify the *Default Value* parameter, in this case there will be no error and the specified string will be assigned to the variable.
