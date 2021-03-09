---
title: Get Windows Registry values
desc: The command retrieves one or more Windows registry values.
img:
   get-registry-value: scripts/get-registry-value.png
html:
   get-registry-value: '<img src="%img.get-registry-value%" style="margin: 1em 1em;"/>'
---
# Get Registry Value

**v1.14.0**  
The **Get Registry Value** command retrieves the Windows Registry values ​​in the specified subkey and assigns these values ​​to variables.

%html.get-registry-value%

**Root Key**  
Specify the Registry root key.

**Subkey**  
Specify the name of the Registry key where the retrieved values are located.

``` txt
Software\My Application\Data
```

## Values

Enter the values ​​you want to get here. The current version supports the following types of Registry values: **SZ, EXPAND_SZ, DWORD**.

**Value Name**  
The name of the value to be retrieved. If an empty string is specified, then the default value will be obtained.

**Variable Name**  
The name of the variable to be assigned the value.

**Default Value**  
By default, if the value does not exist, an error is returned. If you specify the *Default Value* parameter, then there will be no error and the specified string will be assigned to the variable.

**Access**  
Access for keys of 32-bit or 64-bit applications.

* *---* - default access.
* *WOW64_32KEY* - access to the Registry keys for 32-bit applications.
* *WOW64_64KEY* - access to the Registry keys for 64-bit applications.
