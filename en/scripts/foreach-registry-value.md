---
title: Perform an action for each value of the Registry subkey
desc: The command executes nested commands for each value of the Windows Registry subkey.
img:
   foreach-registry-value: scripts/foreach-registry-value.png
html:
   foreach-registry-value: '<img src="%img.foreach-registry-value%" style="margin: 1em 1em;"/>'
---
# Foreach Registry Value

**v1.14.0**  
The **Foreach Registry Value** command executes nested commands for each value in the specified Windows Registry subkey.

%html.foreach-registry-value%

**Root Key**.  
Specify the Registry root key.

**Subkey**  
Specify the name of the Registry subkey in which you want to enumerate all values.

``` txt
Software\My Application
```

**Variable Name**  
Specify the name of the variable to which the name of the next value will be written. You can use this variable in nested commands. If a default value is specified for the subkey, then the variable will be an empty string.

**Access**  
Access for keys of 32-bit or 64-bit applications.

* *---* - default access.
* *WOW64_32KEY* - access to the Registry keys for 32-bit applications.
* *WOW64_64KEY* - access to the Registry keys for 64-bit applications.
