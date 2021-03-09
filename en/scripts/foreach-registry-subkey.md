---
title: Perform action for each Registry subkey
desc: The command executes nested commands for each Windows Registry subkey.
img:
   foreach-registry-subkey: scripts/foreach-registry-subkey.png
html:
   foreach-registry-subkey: '<img src="%img.foreach-registry-subkey%" style="margin: 1em 1em;"/>'
---
# Foreach Registry Subkey

The **Foreach Registry Subkey** command enumerates all subkeys of the specified subkey and executes the nested commands for each subkey.

%html.foreach-registry-subkey%

**Root Key**  
Specify the Registry root key.

**Subkey**  
Specify the name of the Registry subkey in which you want to iterate over all the subkeys.

``` txt
Software\My Application
```

**Variable Name**  
Specify the name of the variable to which the name of the next subkey will be written. You can use this variable in nested commands.

**Access**  
Access for keys of 32-bit or 64-bit applications.

* *---* - default access.
* *WOW64_32KEY* - access to the Registry keys for 32-bit applications.
* *WOW64_64KEY* - access to the Registry keys for 64-bit applications.
