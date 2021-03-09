---
title: Set Windows Registry values
desc: The command sets one or more Windows registry values.
img:
   set-registry-value: scripts/set-registry-value.png
html:
   set-registry-value: '<img src="%img.set-registry-value%" style="margin: 1em 1em;"/>'
---
# Set Registry Value

The **Set Registry Value** command creates or modifies the Windows Registry values ​​in the specified subkey.

%html.set-registry-value%

**Root Key**  
Specify the Registry root key.

**Subkey**  
Specify the name of the Registry key that contains the values ​​to be set.

``` txt
Software\My Application\Data
```

## Values

Specify the parameters that you want to create or modify here.

**Value Name**  
The name of the value to be created or modified. If an empty string is specified, then the default value will be changed.

**Value Type**  
Specify the type of the value. The current version supports the following Registry value types: **SZ, EXPAND_SZ, DWORD**.

**Value**  
Specify the string that will be assigned to this value.

**Access**  
Access for keys of 32-bit or 64-bit applications.

* *---* - default access.
* *WOW64_32KEY* - access to the Registry keys for 32-bit applications.
* *WOW64_64KEY* - access to the Registry keys for 64-bit applications.
